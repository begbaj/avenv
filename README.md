# Avenv

Avenv is a very simple **bash** script to activate and create python virtual environments with ease.

## Why?
Many asked me. There are a lot of other options out there, so why this?
Because it is handy to me. There is no other reason.

I simply didn't like other workflows. And some years ago I developed this one that just resulted to be extreamly optimal for me.
Besides: this is not an entire program, aliases do not do the same thing this script does, and is not changing anything on the package management structure itself.
It just changes WHERE virtual environments are stored, and makes access easier than just `python -m venv venv` and then `source .venv/bin/activate`. Also, this
doesn't even let you source the activate script from anywhere else than the directory where the venv is stored itself. Unless you are confortable writing absolute path strings.

## How it Works

Avenv simply creates virtual environments in a predefined directory (by default `$HOME/.local/virtualenvs/`).
Then, it just returns the path to the selected virtual environments activate script.

So, when you lunch `avenv my_env` it actually is just `echo "$HOME/.local/virtualenvs/my_env/bin/activate"`.
This makes it enough to activate the script when you combine it with `source`:

```console
user@local:/wherever/you/are/ > source avenv my_env
(my_env) user@local:/wherever/you/are/ > nvim . # this lunches neovim within my_env
```

## How to use

to create a venv:

```bash
avenv -m my-venv-name
```

to activate a venv (wherever you are):

```bash
source avenv my-venv-name
```

If you don't remember which venvs you created:

```bash
avenv -l
```

If you want to **permanentely** delete a venv:

```bash
avenv -r my-env-name
```

# License

This Software is distributed under GPLv3 License
