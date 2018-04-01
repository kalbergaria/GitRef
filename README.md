# GitRef
My personal git reference guide. For the most part I have excluded the basics, for that I recommend referring to my favorite git guise in the following section.
<br><br>

# 1) Guides I like to Reference
- :star: http://rogerdudler.github.io/git-guide/ :star: - is my personal favorite because of its simplicity and because it covers all of the basics!
- Of course, for a more official source, there is also https://git-scm.com/ which covers everything git.
<br><br>

# 2) Submodules
This section will contain helpful info for working with submodules.

## Cloning a Repo with Submodules
Clone a project that contains submodules, using `git clone <repo url> --recurse-submodules`. This will clone the specified repo as well as any of its submodules.

## Updating Submodule(s)
To update a submodule with its latest commits, run `git submodule update --remote <submod name>` from outside the submodule's directory. While passing a submodule's name is optional, note that if a name is not provided all submodules within the repository will be updated.

## Working in a Submodule
You may work in a submodule as you would work in a repository normally (i.e. add, commit, push, etc.) once you:

1) Checkout a branch to work on

*Note: If you would like to work in a branch that does not yet exist in the repo, refer to the *branching* section of [this guide](http://rogerdudler.github.io/git-guide/) to learn how to create a branch and push it to your remote repo (you may want to do this from a non-submodule version of the repo).*

2) Set the upstream using a variation of the following command `git push --set-upstream <branch name>`

*Note: Assuming you want to push local commits to the remote version of the branch you are working in, you can simply replace* *<branch name>* *in the previous command with the name or the branch you are working in.*
