# PyInstaller offline installer for Windows x64

This folder contains PyInstaller 6.22.3 and its offline installation dependencies.
It supports 64-bit CPython 3.9 through 3.15, except Python 3.10.0.

## Install offline

Open Command Prompt in the folder containing the .whl files.
Replace -3.15 with your installed Python version, such as -3.12.

```bat
py -3.15 --version
py -3.15 -m pip install --no-index --find-links "." pyinstaller==6.22.3
py -3.15 -m PyInstaller --version
```

## Build and run your EXE

Open Command Prompt in your project folder on Windows.
Install your project's dependencies in the same Python environment.
Replace main.py with your entry script and main.exe with the matching output name.

```bat
py -3.15 -m PyInstaller --onefile main.py
.\dist\main.exe
```

If using an activated virtual environment, replace py -3.15 with python in every command.
