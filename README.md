# About rbtool-cloudstack

This is a fork of the reviewboard tool from reviewboard.org:
http://downloads.reviewboard.org/releases/RBTools/0.4/RBTools-0.4.2.tar.gz

I enhanced this tool as per my needs to automate and productivize my
day to day encounters with RB on apache.org.

- Rohit Yadav <bhaisaab@baagi.org>

Do these things to use this
tool:

Append this to your ~/.gitconfig, this is how the tools finds the RB.

    [reviewboard]
      url = https://reviews.apache.org

Get this tool:

    $ mkdir -p ~/bin && cd ~/bin
    $ git clone git://github.com/bhaisaab/RBTool.git

Let's add a script that saves you from lengthy commands and having to type in
username and password everytime:

    $ echo #!/bin/bash >> rbtool-cs
    $ echo export PYTHONPATH=~/bin/RBTools/:$PYTHONPATH >> rbtool-cs
    $ echo python ~/bin/RBTools/rbtools/postreview.py --username=<put your username here> --password='put here password' $* --debug >> rbtool-cs

Update your PATH:

    $ echo export PATH=~/bin:$PATH >> ~/.zshrc # or ~/.aliasrc or ~/.bashrc or ~/.profile
    $ source ~/.zshrc



