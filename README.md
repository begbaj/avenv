# Avenv
A venv is a very simple script to manage python virtual environments with ease.
I firstly developed this because I didn't like the management via the `venv` module directly, it seemd too verbose, and to activate a venv you needed to look for `activate` script.
Also, many times, I need just one virtual environment for many projects, like a "global" virtual environment. I didn't want to use `conda` and other solutions seemed to me too complex for such a simple task.
Thus, **avenv** (which initially stood for "activate venv", and there was a "mkvenv" which obviously created a venv).

## How it Works
to create a venv:
```bash
$ avenv -m my-venv-name
```

to activate a venv (wherever you are):
```bash
$ source avenv my-venv-name
```

If you don't remember which venvs you created:
```bash
$ avenv -l
```

If you want to **permanentely** delete a venv:
```bash
$ avenv -r my-env-name
```

# License
No license, use it as is, I don't care what you do with it
