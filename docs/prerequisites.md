# Setup Your Machine

Here are list of applications required to setup development environment on Mac.
It's also recommended that you refer to our Glossary page

##1. iTerm2

Download iTerm2 from [http://iterm2.com](http://iterm2.com). Drag and drop the
app into your Applications folder.

##2. ZSH

1. Open iTerm2 window.
1. Go to [http://ohmyz.sh](http://ohmyz.sh), scroll down, copy and paste the
installation line into iTerm2 window (we'll call this **terminal**).
2. If Zshell is not activated immediately, quit iTerm2 and open again.


##3. Homebrew

Go to [http://brew.sh](http://brew.sh), find, copy and paste the installation
line into terminal.

To make sure it's installed properly, type `which brew` and it should reply
you with something like `/usr/local/bin/brew`

##4. Atom Editor

Download Atom from [http://atom.io](http://atom.io). Drag and drop the app into
your Applications folder.
If you start the editor on OSX for the first time, you should click at
"Atom > Install Shell Commands"

Optionally, you can install these packages to help us deal with Python syntax:
1. [autocomplete-python](https://atom.io/packages/autocomplete-python)
1. [linter-flake8](https://atom.io/packages/linter-flake8)
Also checkout the installation guide for each package.

##5. Git

We'll be using local git and Github.

- Check if you already have git by typing `git` in terminal. If you get a ton
of output, you already have it. If not, install via Brew by typing
`brew install git`

- If you're not familiar on how git works, a good interactive tutorial can be
found on
[https://try.github.io/levels/1/challenges/1](https://try.github.io/levels/1/challenges/1)
- Create a profile on [GitHub](https://github.com)

##6. Slack
Team TechLadies uses [Slack](https://slack.com/) for daily communications and
it has downloadable Mac app [here](https://slack.com/downloads)

##7. Python
Mac comes with Python. Try typing `python --version` into terminal and
it will show you which version installed. Alternatively, you can also install
via Homebrew by typing `brew install python`.

The difference is that if you install via Homebrew, the Python binary will be
placed under `/usr/local/bin/python` and it also automatically install `pip`
Python package manager.

##8. Virtualenv & virtualenvwrapper

Steps to configure Virtualenv:
1. From terminal, type `sudo pip install virtualenv` wait until completed.
2. Next, type `sudo pip install virtualenvwrapper` wait until completed.
3. Next, type `export WORKON_HOME=~/Envs`. This will place all your virtualenv
under your `HOME_DIRECTORY/Envs`
4. Next, type `echo 'export WORKON_HOME=~/Envs' >> ~/.zshrc`
5. Next, type `echo 'source /usr/local/bin/virtualenvwrapper.sh' >> ~/.zshrc`
6. Next, type `mkdir -p $WORKON_HOME`
7. Next, type `source /usr/local/bin/virtualenvwrapper.sh`

### Test virtualenv & virtualenvwrapper

1. Open new terminal session and type `mkvirtualenv myproject`.
It should output few lines and the prompt on the left will indicate your
current active virtualenv which is `(myproject)`
2. To exit the virtualenv, type `deactivate`, the prompt will go normal again.
3. To enter the virtualenv again, type `workon myproject`.
4. You can create more virtualenv and to list all virtualenv you have,
type `workon` only.
5. To delete a virtualenv, type `rmvirtualenv myproject`

![Screenshot](http://i.imgur.com/WMD1yfZ.png)

Any Python packages installed in this virtualenv only valid within this
virtualenv. To list the packages installed, type `pip freeze`.

## And that's a wrap!

Looks like we're good to go!
