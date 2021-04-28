# Steps to creating a Pull Request (PR)

## Step 1 . Create a pull request

- Go to upstream repository on GitHub web page. Click on `Pull Request Tab`. Now click on `New Pull Request` green button on right hand side.

  ![git branch console](/images/pull-request.gif)

- Add a title. Leave a comment describing what is in your PR

- Add reviewer. you add us as your reviewer.

- Click on the green button that says `Create pull request`

- Check PR

  ![git branch console](/images/pr-raised.png)

- Check your commits and modified files in the PR, by toggling through tabs.

- A successful PR will have no conflicts, if a PR has conflicts it needs to be resolved. Like in the below case, its a non sync conflict, as pull request is not in sync with master branch.

  ![git branch console](/images/resolve-conflict.png)

## Step 2\. Sync your local repository with upstream

Ensure that your local repository is up-to-date with the changes in upstream.

- Sync your branch with upstream `git fetch upstream`

- Pick commits from upstream `git rebase upstream/main`.

you would see:

```
  hnalla@workstation ~/Demo/intern-bootcamp-git (feature) $ git rebase upstream/main
  First, rewinding head to replay your work on top of it...
  Applying: added harshad
  Using index info to reconstruct a base tree...
  M    attendees.txt
  Falling back to patching base and 3-way merge...
  Auto-merging attendees.txt
  CONFLICT (content): Merge conflict in attendees.txt
  error: Failed to merge in the changes.
  Patch failed at 0001 added harshad
```

In case you get conficts, resolve the conflicts manually by going to the files having conflicts. Either accept the incoming changes from upstream or keep your local changes or both, you need to inspect and make the decision.

- open the conflicted file. `vim attendees.txt`

  ```
  Please enter your names and email ids below:
  <<<<<< upstream/main
  anish aasthana@redhat.com
  ======
  Harshad hnalla@redhat.com
  >>>>>> origin/feature
  ```

- Remove the <,>,= symbols, with keep the required texts/code and save the file.

- Add the file `git add .`

- Then do `git rebase --continue`

- Now look at `git log`, a new commit or few commits would have appeared below your commit.

- Push changes `git push origin feature`

  ```
  hnalla@workstation ~/Demo/intern-bootcamp-git (feature) $ git push origin feature
  To github.com:harshad16/intern-bootcamp-git.git
  ! [rejected]        feature -> feature (non-fast-forward)
  error: failed to push some refs to 'git@github.com:harshad16/intern-bootcamp-git.git'
  hint: Updates were rejected because the tip of your current branch is behind
  hint: its remote counterpart. Integrate the remote changes (e.g.
  hint: 'git pull ...') before pushing again.
  hint: See the 'Note about fast-forwards' in 'git push --help' for details.
  ```

- As we made changes and rebased with upstream main, the origin git history has changed in local, but the git history of origin in remote is falling disturb. Hence a force push is required.<br>
  `git push -f origin feature`

- Check back the PR you have raised: ![git branch console](/images/fix-conflicts.png)

### **NOTE**: The Best practice is to take a pull from upstream before push.
