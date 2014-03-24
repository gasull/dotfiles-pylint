pylintrc files
==============

My global pylintrc and my django.pylintrc for Django projects.

django.pylintrc was originally created by
[TomasFlam](https://github.com/TomasFlam).

## Installation

Put django.pylintrc in your PYLINTRC environment variable.  I like to keep all
my configuration files in the standard $XDG_CONFIG_HOME (~/.config by default).

```bash
cd ~/src/
git clone https://github.com/gasull/dotfiles-pylint.git
cd ~/.config
ln -s
ln -s ~/src/dotfiles-pylint/pylint
```

And in your ~/.bashrc or ~/.bashrc_local:

```bash
# pylint
export PYLINTRC="$XDG_CONFIG_HOME/pylint/pylintrc"
```

Optional: Configure .vimrc to use django.pylintrc in
[Syntastic](https://github.com/scrooloose/syntastic):

```vim
" Syntastic for Django files
if search('^from django', 'npw')
  let g:syntastic_python_pylint_args='--rcfile="$XDG_CONFIG_HOME/pylint/django.pylintrc"'
endif
```

This requires
[pylint-django plugin](https://github.com/landscapeio/pylint-django)
(follow link for installation instructions).
