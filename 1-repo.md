# Creating a repo

## Step 1.1 Creating a repo on GitHub

In your GitHub account, find the Repositories tab and click. Then click the green New button.

![PACSPull Plugin](/images/github-new-repo.png)

Choose a name for your repo (ex. `myawesomerepo`). Choose the button to make the repo public and select "Initialize this repository with a README." Leave all other choices on the default setting.

![PACSPull Plugin](/images/github-repo-initialize.png)

## Step 1.2 Cloning the repo locally

Copy the repo's URL. In your GitHub account, click the Repositories tab and click on your new repo. Click the green "clone or download" button on the right.

![PACSPull Plugin](/images/clone-via-ssh.png)<br>
you clone either with HTTPS or SSH(Recommended) URL.

In the terminal, navigate to your home directory and clone the repo with:

```
cd ~
git clone <URL>
```

You should be able to paste the URL into the terminal by right-clicking and selecting `Paste`. (`ctrl` + `v` usually won't work.)

You should see:

```
Cloning into 'myawesomerepo'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
```

Then change directory to your local repo with:

```
cd myawesomerepo/
```

Now you are inside the repo folder. You can see the files in your repo by using:<br>
`ls`

This should show you:<br>
`README.md`
