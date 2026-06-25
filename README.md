# diffractive-MOKE

Micromagnetic modelling of the magneto-optical Kerr effect (MOKE), built on
[Ubermag](https://ubermag.github.io/) (OOMMF) and related tools. The analysis
lives in [`MOKE.ipynb`](MOKE.ipynb).

## Prerequisites

This project uses [pixi](https://pixi.sh/) to manage its conda/PyPI
environment. Install pixi if you don't have it yet:

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

Then restart your shell (or `source ~/.bashrc` / `~/.zshrc`) so the `pixi`
command is on your `PATH`. See the
[pixi install docs](https://pixi.sh/latest/#installation) for other methods
(Homebrew, Windows, etc.).

## Install the environment

From the project root, run:

```bash
pixi install
```

This resolves and installs everything pinned in `pixi.toml` / `pixi.lock`
(Python 3.11, Ubermag, JupyterLab, and the supporting packages) into a local
`.pixi/` environment. No global state is touched.

## Run JupyterLab

A `lab` task is defined in `pixi.toml`:

```bash
pixi run lab
```

This launches JupyterLab inside the project environment; open the printed URL
in your browser and select `MOKE.ipynb`.

To get an interactive shell with the environment activated instead, use:

```bash
pixi shell
```
