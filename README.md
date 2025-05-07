# Boston Bioimage Analysis Course (BoBIAC)
Teaching materials for Boston Bioimage Analysis Course (BoBIAC).

## Install juv

After installing [uv](https://docs.astral.sh/uv/):

```bash
uv tool install juv
```

Then to use any command you run:

```bash
juv [OPTIONS] COMMAND [ARGS]...
```

If you do not want to install it, you can run juv with:

```bash
uvx juv [OPTIONS] COMMAND [ARGS]...
```

## Create a notebook

```bash
juv init notebook.ipynb
juv init --python=3.12 notebook.ipynb # specify a minimum Python version
```

## Add dependencies to the notebook

```bash
juv add notebook.ipynb "ndv[vispy,jupyter]" tifffile

# or

juv add notebook.ipynb package-name --requirements=requirements.txt
```

## Launch the notebook

```bash
# Launch the notebook
juv run notebook.ipynb

# or

juv run --with=pyqt6 notebook.ipynb # additional dependencies for this session (not saved)
juv run --jupyter=nbclassic notebook.ipynb -- --no-browser # pass additional arguments to Jupyter
```
