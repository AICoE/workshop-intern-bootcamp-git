# Appendix

Extra tips and resources relating to concepts covered in the workshop.

Got more tips that you don't see here? Submit a pull request!

## Github tips

[Github Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet/)

### Files Worth adding to a repository

- .gitignore: Specifies intentionally untracked files to ignore [Comman gitignore files](https://github.com/github/gitignore)
- License: A software license tells others what they can and can't do with your source code, so it's important to make an informed decision. [Add license to GitHub repo](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/licensing-a-repository)

### GitHub _Work In Progress_ Pull request

While you are working on pull request, you can clearly tag when you're coding a work in progress.<br>
Tags such as WIP or [WIP] can be added to the Title either at the begining or at the end.<br>
It would be considered by GitHub Pipeline itself

### Initializing a git repo: 2 ways

**Create remote first** Create a new repo or fork an existing repo in your Github account online. Then use `git clone <repo.git>` to copy the repo to your local machine. (This is what we did in the workshop.)

**Create local first** Locally create a new directory for your project, `cd` to the directory, and enter `git init`. This will turn your directory into a git repo with a `.git` file. Add a remote with `git remote add <remote_name> <remote_repo_url>` and set this as the repo to push to with `git push -u <remote_name> <local_branch_name>`.

More info:<br>
<https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-init><br>
<https://www.atlassian.com/git/tutorials/syncing>

### Git rebase in depth

You can rebase one branch by itself, or rebase a branch onto another branch.<br>
More info: <https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase>

### Git reset in depeth

You can use reset to revert or remove commits or HEAD to specified state.<br>
More info: <https://git-scm.com/docs/git-reset>

### Use ohmyzsh to configure useful plugins and themes

ohmyzsh: Oh My Zsh is an open source, community-driven framework for managing your zsh configuration. [README](https://github.com/ohmyzsh/ohmyzsh/blob/master/README.md)

## Other

### Version control

Check out the Atlassian tutorial on version control: <https://www.atlassian.com/git/tutorials/what-is-version-control>

### What is the terminal, and why use it?

More info: <https://learntocodewith.me/getting-started/topics/command-line/>

### Basic bash commands

These are the commands used in many Linux and Mac terminals (and similar to Windows PowerShell). More info: <https://dev.to/awwsmm/101-bash-commands-and-tips-for-beginners-to-experts-30je> <https://www.unr.edu/research-computing/the-grid/using-the-grid/bash-commands>

### Markdown

Markdown is used in GitHub's README and other `.md` files. More info: <https://guides.github.com/features/mastering-markdown/>

## Open source projects to get started

### Moxilla

<https://codetribute.mozilla.org/>

### Pinax

<https://github.com/pinax> Search issues by filter "first-timers-only" che

### Google Summer of Code

<https://summerofcode.withgoogle.com/>

### Blogs

Blog on beginner's friendly open source projects. <https://opensource.com/life/16/1/6-beginner-open-source>
