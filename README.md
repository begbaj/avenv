# Avenv

Avenv is a very simple **bash** script to activate and create python virtual environments with ease.

## Background

I firstly developed this because I didn't like the management via the `venv` module directly, it seemd too verbose, and to activate a venv you needed to look for `activate` script.
Also, many times, I need just one virtual environment for many projects, like a "global" virtual environment. I didn't want to use `conda` and other solutions seemed to me too complex for such a simple task.
Thus, **avenv** (which initially stood for "activate venv", and there was a "mkvenv" which obviously created a venv).

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
