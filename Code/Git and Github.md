[Hello World - GitHub Docs](https://docs.github.com/en/get-started/quickstart/hello-world)
[GitHub flow - GitHub Docs](https://docs.github.com/en/get-started/quickstart/github-flow)
[Quickstart - GitHub Docs](https://docs.github.com/en/get-started/quickstart)
## Creating a repository
A repository is usually used to organize a single project. Repositories can contain folders and files, images, videos, spreadsheets, and data sets -- anything your project needs. Often, repositories include a _README_ file, a file with information about your project.

`git config --global user.email "316222290@qq.com"`

```
git init # only when creating a new repository
git add .
git commit -m "<note>"
git remote add origin https://github.com/Ohhhhhhhhyjay/Notes.git
git push -u origin main
```
-u: set-upstream, For every branch that is up to date or successfully pushed, add upstream (tracking) reference, used by argument-less [git-pull(1)](git-pull.html) and other commands. For more information, see `branch.<name>.merge` in [git-config(1)](git-config.html).

## Creating a branch

Branching lets you have different versions of a repository at one time.

By default, your repository has one branch named `main` that is considered to be the definitive branch. You can create additional branches off of `main` in your repository. You can use branches to have different versions of a project at one time. This is helpful when you want to add new features to a project without changing the main source of code. The work done on different branches will not show up on the main branch until you merge it, which we will cover later in this guide. You can use branches to experiment and make edits before committing them to `main`.

When you create a branch off the `main` branch, you're making a copy, or snapshot, of `main` as it was at that point in time. If someone else made changes to the `main` branch while you were working on your branch, you could pull in those updates.

Here at GitHub, our developers, writers, and designers use branches for keeping bug fixes and feature work separate from our `main` (production) branch. When a change is ready, they merge their branch into `main`.


