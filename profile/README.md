# Carpet Project
> This is a collaborative fullstack software project for the [TechProAcademy Bootcamp](techproacademy.gr/).

## How to use basic Git - a guide

### Cloning a repository

First steps is to clone the repository you'd like to work on using `git clone`, for example:

```bash
git clone https://github.com/carpetproject/carpet.git
```

This should be done through the VSCode terminal or alternatively through your VM's terminal. After using the clone command, your local files will automatically be connected to the Github repository's files.

### Committing to a repository

The next step is to learn how to make a commit to the repository. Before committing, you'll have to have made some changes to the repository files you cloned earlier.

---

First, you'll need to add all the changes to git, to be able to commit them later on. You can do so by running the following:

```bash
git add .
```

What this does is, take everything in the directory you're currently in, that has been changed, and make it "ready" to be committed. You can then commit using the following command:

```bash
git commit -m "insert message here"
```

Inside the `""` you will need to describe the changes you made in **Imperative** form, i.e. `fix REST API request to properly return data` instead of `fixed REST API request [...]`. This is common practice among git users.

### Pushing to a repository

After committing your changes with a short but descriptive message, you will need to do one last step to push them to the Github repository:

```bash
git push
```

The command is self-explanatory, it pushed the changes you committed to the repository, also called "repo" for short.

### Commit types and message formats

It's common practice for developers to have a format for writing commit messages. In this project we will be using them as well! What is shown below is the commonly used format for commit messages:

> `<type>(thing): <message>`

Commonly Used Types:
> `feat`, `chore`, `ci`, `fix`, `docs`

So an example feature commit would be:
> `feat(carpet): add selection menu`

To explain what the above commit message means; the committed code involves a feature for the carpet repository (or branch - will explain below) which is to add a selection menu.

### Branches

When more than one person is working on a repo, they are usually working on different features, or parts, of the repo. That is where branches come in. Branches are essentially a new/seperate version of the repo. To explain in detail, say I wanted to work on feature A without committing to the main repository, I would make a new branch "`feat/actuallylost/A`" where I could safely commit to without having the risk of breaking the main repo.

The same types that are used for commits, are also used when creating branches, with the following format:

> `<type>/<creator_name>/<branch_name>`

The way to create a branch is a bit tricky because you have to take into account some things. Say I wanted to make a new branch to work on a new feature, I could easily do the following command:

```bash
git checkout -b <branch_name>
```

The above command will create a branch `branch_name` and immediately switch to it. You will now be able to make any changes you want without risking interfering with the master branch. You can then add, commit and push to that branch like you would before, however when pushing, the first time you have to run:

```bash
git push --set-upstream origin branch_name
```

You can always switch between branches by running:

```bash
git checkout <branch_name>
```

The issue is that sometimes you forgot you were on the master branch, and made some changes you wanted to make on another branch! It's not the end of the world, no worries, you will just need to run the following commands:

```bash
git stash
git checkout <branch_name>
git stash pop
```

What the command `git stash` does, is that it "stashes" your changes locally, and then you "pop" them in the other branch, which adds them to it. You can then commit and push as you normally would.

Remember that if the branch you'd like to commit the changes to does not exist, you create it using the `git checkout -b <branch_name>` command.

> **NOTE:** You can only run these commands if you have not already committed the changes!

Usually VSCode will guide you through this process, but you can always return back to this guide when needed.

## Libraries & Languages
> The languages that will be used are `JavaScript` and `Java`.

* `Java` will be used alongside `Maven` & `Sprintboot`.
* `JavaScript` will be used alongside `React.js` and `Vite`.

## License
> **This project uses the GNU General Public License v3.0.**
