# Glossary

During our journey of learning how to build a full-stack Django project,
we will learn many new technical terms. We will try to keep track of them
in this glossary.

**Ansible**

Ansible is a tool to "provision" servers. That means it helps to install
software on a server in an automated, scripted and repeatable way.

**Branch**

A branch is the parallel version of the Master Branch (See also: Master Branch). The Master Branch is copied and branched out into a branch. Work on or modify the code here, as changes will not affect the main repository. Branches can also be used for bug fixing, as the work here does not affect the main repository until merged and committed. Merge the branch into the Master Branch only after all changes are made and it is ready to publish.

There can be several branches in a repository. Branches can be deleted after the merge is complete. Branches can also be referred to as volatile branches.

The command to create a new branch is `git branch new_branch name`. Check existing branches and which branch you are currently on by using the command `git branch`. The branch you are currently on will be indicated by an asterisk before its name.

**Clone**

A clone is a copy of a repository that lives on your local computer once copied from a remote server. The command to clone a remote server is `git clone [url of server]`. Changes have to be pushed (See also: Push) onto the remote server, to be able to see them on the remote server.

**Checkout**

Checkout in Git is tricky, as it serves multiple uses.

One use is to switch from to a branch, as seen in `git checkout branch_name`. Create a new branch and checkout to it at the same time by using the command `git checkout -b new_branch_name`.

Checkout can also be used to return the file to a previous version. `git checkout <commit>` returns the file to the version of the particular commit. <commit> is the first 7 character of your commit hash (See also: Hash), which helps to identity which particular commit it is.

**Commit**

Commit is the action to apply your changed and staged files. To make a commit
type `git commit -m "Description about your commit"`

**Django**

Django is a high-level Python Web framework that encourages rapid development
and clean, pragmatic design. It's free and open source.

**Droplet**

Droplet refers to a virtual private server instance at DigitalOcean that is
setup and can be configured to user's need such as CPU size, memory, hard disk
capacity, installed OS, and more.

**Full Stack**

A web application consists of many layers for instance: user interface, business
logic, servers, databases, operating systems. Each layer has different
technology which is what we call a *stack*. This entire web application is
therefore called Full Stack.

**Git**

Git is a version control system. You can turn a normal folder on your hard disk
into a "repository". When you do that, Git will keep track of all changes made
to all files. You can then "commit" your changes and review them in a log or
even go back to an older version of your files. When working on a project with
a team, this helps to keep track about who did what and when.

**Hash**

A hash is a unique ID that is generated with each commit.

**Master Branch**

Master branches are stable branches. These are the ones to be shared amongst collaborators of a project, which ought to stay the way they are. Any modifications should go into volatile branches (See also: Branch) to avoid affecting the repository.

**Merge**

Merge is git action of joining two or more development histories together.

**Pull**

Pull is to extract the latest version of the master branch and other branches from Git so that the user can work off the latest version of a repository.

**Push**

When a user is done with making changes to their branch they can "push" their changes to the master. By doing so, they update the master with the changes that they have committed.

**Rebase**

Rebasing is the process of moving a branch to a new base commit.
From a content perspective, rebasing really is just moving a branch from one
commit to another. But internally, Git accomplishes this by creating new
commits and applying them to the specified base—it’s literally rewriting
your project history.

**Repository**

Repository is where git stores information about a project files and its
history.

**Staged**

When a user has made changes to a repository they can add those changes. By doing so the user "stages" their changes. Only staged changes can be committed.

**Terminal**

The Terminal is the part of the computer where programmers can program information and data into the computer.
