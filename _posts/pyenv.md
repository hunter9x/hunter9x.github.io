## Best practice pyenv

### Installation

* Use the [installer](https://github.com/pyenv/pyenv-installer)

  `curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash`

* Edit zshrc

  ```shell
  WARNING: seems you still have not added 'pyenv' to the load path.
  
  # Load pyenv automatically by adding
  # the following to ~/.zshrc:
  
  export PATH="/home/kai/.pyenv/bin:$PATH"
  eval "$(pyenv init -)"
  eval "$(pyenv virtualenv-init -)"
  
  ```

  

* Then `source ~/.zshrc`

* OK. Now install the version of Python that you need to use

  ```shell
  $ pyenv install 3.6.5
  $ pyenv versions
  * system (set by /home/kai/.pyenv/version)
    3.6.5
  $ pyenv global 3.6.5
  $ python --version
  Python 3.6.5
  ```

  ### Build environment for specific project

* Project path: `/home/kai/learn/timestrack-bot`

* I use `venv` to build develop environment for this project

* How dose it look like?

  ```shell
  $ cd /home/kai/learn/timestrack-bot
  $ mkdir .venv
  # add this folder to .gitignore
  # the python basic environment is like installation part
  $ python -m venv .venv
  # .venv folder look like this
  $ tree .venv -L 1
  .venv
  ├── bin
  ├── include
  ├── lib
  ├── lib64 -> lib
  └── pyvenv.cfg
  # start new env
  $ source .venv/bin/activate
  # you can check version of python and pip
  # install some package via pip like this
  $ pip install slackclient
  # check it out
  $ pip list
  # you can see slackclient be installed
  # So, let close this venv
  $ deactivate
  # and check pip list, you wil know the difference
  # note: the slackclient package be installed with its dependencies
  ```

  ## Summary

  * Use pyenv to manage python's versions

  * In each python versions (shims) use venv (python3) to create the environment for each project

  * Why?

    