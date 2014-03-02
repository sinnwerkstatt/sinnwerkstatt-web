# GitLab

[GitLab](http://gitlab.org/) - open source Self hosted Git management software based on Ruby on Rails and MIT License.

## Installation

The current installation is of version:
gitlab         5.2.0
gitlab-shell 1.4.0

These installation instructions were followed to the letter: https://github.com/gitlabhq/gitlabhq/blob/master/doc/install/installation.md

The following bugfix was required for a working installation with rvm:
- move sourcing rvm script before return statement for non-interactive logins in /home/git/.bashrc:

```bash
PATH=$PATH:$HOME/.rvm/bin # Add RVM to PATH for scripting

# If not running interactively, don't do anything
case $- in
    *i*) ;;
      *) return;;
esac
```

solutions found in:
- https://github.com/gitlabhq/gitlab-shell/issues/12
- http://stackoverflow.com/questions/6918536/rvm-is-not-working-over-ssh/7158894#7158894
