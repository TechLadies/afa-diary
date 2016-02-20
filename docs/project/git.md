# Git

We are using [Git](http://www.git-scm.com) as our version control system and
[GitHub](https://github.com) for hosting our repositories and for collaboration.

## Tutorials

To learn the basics of Git we worked through the following tutorials:

* [https://try.github.io](https://try.github.io)
* [https://guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/)
* [https://github.com/git-game/git-game](https://github.com/git-game/git-game)

We also participated in a three-hour workshop conducted by the organizers of
the [Grumpy Gits SG User Group](http://www.meetup.com/Grumpy-Gits-SG/).

**Warning**: Learning Git on your own is a difficult task, because there are
many different commands that you need to memorize. To make things worse, there
is one command called "checkout" that does at least three completely different
things and some of those things don't even have anything to do with "checking
something out.

There are also dozens of ways to orchestrate all those many commands. Basically
every company out there has their own internal workflow, therefore you will not
find the one definite tutorial that teaches you how to do it and if you ask
questions, three people will give you three different answers.

You should definitely team up with a mentor who can guide you and work through a
few test-scenarios with you and ultimately you need to understand what Git is
doing on your hard disk in order to really have confidence in whatever workflow
you decided to use.

## Workflow

In order to collaborate on this repository, we will stick to a simplified
workflow that has only the `master` branch as a stable branch.

This means, whatever we merge into `master` should be good. At all times must we
be confident that the `master` branch can be deployed by using the
`mkdocs gh-deploy` command.

In plain English, our workflow works as follows: When you decide to create a
change, you first pull the latest version of the `master` branch from GitHub.
Then you create a feature branch and make your changes. When you are done, you
push your feature branch to GitHub so that the team can make a code-review.

1. `git co master` (switch to master branch)
1. `git pull` (get the latest version of the master branch)
1. `git co -b feature_branch` (create your own feature branch)
1. work work work work work work
1. `git add .` (add your changes to the staging area)
1. `git commit` (commit your changes)
1. `git push origin feature_branch` (push your feature branch to GitHub)

Your mentor will usually do this, but for the sake of completeness, here is how
we merge your changes back into the `master` branch when you have passed the
code-review:

First we pull the latest `master` branch just to be sure that we are up to
date. Then we go into the feature branch and try to merge the `master` branch
into the feature branch. We do this because other team members might have
pushed to the `master` branch while you were working on your feature and there
might be merge conflicts if both members worked on the same files. We want to
resolve those conflicts in the feature branch, just to be sure that we don't
accidentally mess up the master branch during the conflict resolution.

Most of the time, there won't be any conflicts. In that case, we will switch
back into the `master` branch and then merge the feature branch with the
`--no-ff` flag into the `master` branch. The `--no-ff` makes sure that we can
see "a bump" in the diagram view of our repository, so in the future we can
still tell that a bunch of commits have all been made inside a certain
feature branch. Once the feature branch has been merged into the master branch,
it can be deleted locally and on GitHub.

1. `git co master` (switch to master branch)
1. `git pull` (get latest version of master branch)
1. `git co feature_branch` (switch to feature branch)
1. `git merge master` (resolve merge conflicts, if any)
1. `git co master` (switch back to master branch)
1. `git merge --no-ff feature_branch` (merge the feature branch)
1. `git push` (push new master branch to GitHub)
1. `git branch -d feature_branch` (delete the feature branch locally)
1. `git push origin :feature_branch` (delete feature branch on GitHub)
