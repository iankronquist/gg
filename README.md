Good Game
=========

How many times have you typed the following commands?
```sh
$ git clone $SOME_PROJECT
$ cd $SOME_PROJECT
$ virtualenv ~/venv/$SOME_PROJECT
$ source ~/venv/$SOME_PROJECT/bin/activate
$ pip install -r requirements.txt
```

or maybe:
```sh
$ git clone $SOME_PROJECT
$ cd $SOME_PROJECT
$ npm install
```

Wouldn't it be great if you could just tab complete a project name and be
whisked there with your environment all set up for you?
What if this command could sniff out python versions, requirements files vs
setup.py files, node dependencies, and more?


Installation
------------
To install, clone the repo and place the
following lines in your `.bashrc`, `.zshrc` or equivalent config file.

```sh
# in .bashrc or .zshrc
source path/to/gg
```
You may also prefer to set the environment variables `$PROJECTS_DIR` and
`$VENV_DIR` to customize where you keep your projects and virtual environments.

Usage
-----
To visit your `$PROJECTS_DIR` and see what's in there, run:
```sh
$ gg
```

To clone a new repo and automatically install dependencies, run:
```sh
$ gg $SOME_GIT_REPO 
```

TODO
----
- Add tab completion for directories in `$PROJECTS_DIR`.
- Sniff the appropriate python version and install it accordingly.
	* maybe look at tox.ini or setup.py files
- Look at adding support for cabal, ruby gems, go get, cargo, and possibly
  others.

Pull requests welcome!
