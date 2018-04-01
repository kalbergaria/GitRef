# GitRef
My personal git reference guide. For the most part I have excluded the basics, however, for the basics I recommend referring to my favorite git guide in the following section.
<br><br>

# 1) Guides I like to Reference
- :sparkles: http://rogerdudler.github.io/git-guide/ :sparkles: - is my personal favorite because of its simplicity and because it covers all of the basics!
- Of course, for a more official source, there is also https://git-scm.com/ which covers everything git.
<br><br>

# 2) Submodules
This section will contain helpful info for working with submodules. To access the guide I gathered and condensed most of the info below from, go [HERE](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

## Adding Submodules to a Project
To add a submodule to a project use `git submodule add <repo URL>` where *<repo URL>* is the URL for the repo you would like to add as a submodule. This will add a file called *.gitmodules* which maps the repo between where it lives and your current project. After this command finishes cloning the specified repo into your current project amke sure to commit and push those changes.

## Cloning a Repo with Submodules
Clone a project that contains submodules, using `git clone <repo URL> --recurse-submodules`. This will clone the specified repo as well as any of its submodules.

## Updating Submodule(s)
To update a submodule with its latest commits, run `git submodule update --remote <submod name>` from outside the submodule's directory. While passing a submodule's name is optional, note that if a name is not provided all submodules within the repository will be updated.

## Working in a Submodule
You may work in a submodule as you would work in a repository normally (i.e. add, commit, push, etc.) once you **checkout a branch to work on**.

*Note: If you would like to work in a branch that does not yet exist in the repo, refer to the *branching* section of [this guide](http://rogerdudler.github.io/git-guide/) to learn how to create a branch and push it to your remote repo. If you create the branch from within a submodule version of it, then you may have to set the upstream using a variation of the following command `git push --set-upstream <branch name>`. Assuming you want to push local commits to the remote version of the branch you are working in, you can simply replace* *<branch name>* *in the previous command with the name or the branch you are working in.*
