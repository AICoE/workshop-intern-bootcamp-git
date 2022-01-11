# Steps for forking an upstream repository

## Step 1\. Fork the upstream repository in your GitHub account.

Consider our [workshop repository](https://github.com/anishasthana/intern-bootcamp-git) as the upstream repository you will be making a contribution to. Follow the screenshot to fork your upstream repository. If you have multiple account (e.g. in the picture), select an account

![Fork upstream repo](/images/fork-repo.gif)

- Forking in progress

## Step 2\. Clone the forked repo

- Clone the repo. Open your terminal. Go to the path where you want to have your repo on your local machine.

  `git clone <ssh-url>`

_Note_: You will be cloning the repository which is a fork of our repository also called upstream in this case.

```
hnalla@workstation ~/Demo $ git clone git@github.com:harshad16/intern-bootcamp-git.git
Cloning into 'intern-bootcamp-git'...
remote: Enumerating objects: 40, done.
remote: Counting objects: 100% (40/40), done.
remote: Compressing objects: 100% (32/32), done.
remote: Total 40 (delta 9), reused 33 (delta 5), pack-reused 0
Receiving objects: 100% (40/40), 414.84 KiB | 4.66 MiB/s, done.
Resolving deltas: 100% (9/9), done.
```

- Enter the clone repo, `cd intern-bootcamp`
- Check remote `git remote -v`.<br>
  You should see url of your repository. Something like<br>
  `https://github.com/<your_github_account_name>/<repository_name>.git`.

  ```
  hnalla@workstation ~/Demo/intern-bootcamp-git (main) $ git remote -v
  origin    git@github.com:harshad16/intern-bootcamp-git.git (fetch)
  origin    git@github.com:harshad16/intern-bootcamp-git.git (push)
  ```

- Add upstream to remote `git remote add upstream <upstream repo link>`<br>
  i.e `git remote add upstream git@github.com:anishasthana/intern-bootcamp-git.git`

- Check remote again `git remote -v`. Now you should see two remotes, namely `upstream` and `origin`. Verify if the urls are corect. `upstream` should be our repo url. `origin` should be your repo url.

  ```
  hnalla@workstation ~/Demo/intern-bootcamp-git (main) $ git remote -v
  origin    git@github.com:harshad16/intern-bootcamp-git.git (fetch)
  origin    git@github.com:harshad16/intern-bootcamp-git.git (push)
  upstream    git@github.com:anishasthana/intern-bootcamp-git.git (fetch)
  upstream    git@github.com:anishasthana/intern-bootcamp-git.git (push)
  ```

## Step 3\. Add new feature/code by creating a new branch, say feature

- Check current branch `git branch`

  `* main (END)`

- Add new branch `git checkout -b feature`

- Check the contents of the repo `ls`

- Open the file `attendees.txt` and add a your name and email id, `Harshad hnalla@redhat.com`

- Save the file.

- Add the file to stage for git to track `git add attendees.txt`

- Make a commit `git commit -m "My first upstream contribution"`

- Push the file `git push origin feature`

- Verify if the file was pushed by checking it on GitHub web page.
