# git-machete


[![Join the chat at https://gitter.im/VirtusLab/git-machete](https://badges.gitter.im/VirtusLab/git-machete.svg)](https://gitter.im/VirtusLab/git-machete?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

![](logo.png)

If you work a with a git rebase flow, git machete will (vastly!) help you manage the jungle of branches stacking on top of each other when you're, for example, working on a couple of different PRs in parallel.

![git machete status](https://raw.githubusercontent.com/PawelLipski/git-machete-blog-2/master/status.png)

## Install

Installation could be done by following commands:

```bash
$ git clone https://github.com/VirtusLab/git-machete.git
$ cd git-machete
$ sudo python setup.py install
```

To install you will need python with installed `pip` and `setuptools`.

python could be installed with system packages or using [pyenv](https://github.com/pyenv/pyenv).

Regular python env should have `pip` and `setuptools`.

If python env is missing any of those tools, please execute following commands:

```bash
# missing pip? check with command: pip
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py

# missing setuptools? check with command: pythom -m "import setuptools"
pip install setuptools
```

[More](https://pip.pypa.io/en/stable/installing/) information about `pip` installation.

## Quick start

```bash
$ cd your-repo/
$ git machete discover
  # (see and possibly edit the suggested layout of branches)
$ git machete go root
$ git machete traverse
  # (put each branch one by one in sync with its parent and remote counterpart)
```

## Contribute

Use `tox -e venv` to setup virtual environment to work on that project in your favorite IDE. Use `.tox/venv/bin/python` as a reference `python` interpreter in your IDE.

## Reference

Take a look at [https://virtuslab.com/blog/make-way-git-rebase-jungle-git-machete/](https://virtuslab.com/blog/make-way-git-rebase-jungle-git-machete/) for a guide on how to use the tool.

The more advanced features like automated traversal, upstream inference and tree discovery are described in the second part of the series:
[https://virtuslab.com/blog/git-machete-strikes-traverse-git-rebase-jungle-even-faster-v2-0/](https://virtuslab.com/blog/git-machete-strikes-traverse-git-rebase-jungle-even-faster-v2-0/)
