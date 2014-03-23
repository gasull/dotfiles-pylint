Customized pylintrc for Django projects
=======================================

For Django projects customized pylintrc. Others can be added as needed.

## Installation

Put django.pylintrc in your PYLINTRC environment variable.  I like to keep all
my configuration files in the standard $XDG_CONFIG_HOME (~/.config by default).

    cd ~/src/
    git clone https://github.com/gasull/dotfiles-pylintrc.git
    cd ~/.config
    ln -s ~/src/dotfiles-pylintrc/django.pylintrc pylintrc

And in your ~/.bashrc or ~/.bashrc_local:

    # pylint
    export PYLINTRC="$XDG_CONFIG_HOME/pylintrc"
