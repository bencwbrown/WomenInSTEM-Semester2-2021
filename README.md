# XeLaTeX Beamer Template

Because all of the predefined beamer themes are overloaded with mostly useless stuff I decided to make my own minimalistic beamer theme.

## Requirements

Tools:

- xelatex
- biber
- makeglossaries

Fonts:

- Linux Biolinum
- Linux Libertine
- Consolas

To install Linux Biolinum and Linux Libertine using Homebrew, run the commands:

`brew cask install font-linux-libertine font-linux-biolinum`.

Packages:

- see `content/misc/preamble.tex`
- I've installed the `texlive-most` meta-package on Arch, but `texlive-full` for ubuntu should also include all the needed packages

## Presentation Setup

The author, title, department etc. has to be set in `content/misc/variables.tex`.

## Build

Simply call `make`. This will call `make.sh` subsequently which `rsyncs` your content in the `build` directory and copies the generated pdf's to the `output` folder afterwards. The `rsync` step is done to prevent your `content` folder from being cluttered with countless of auxiliary files. If you don't have `cmake` and `rsync` try to install a reasonable operating system ;).

## Features

- The titleframe will only show the section or subsection, depending where you are in the presentation
- With the `\plaintextframe` command you can set up a plain frame with a message vertically and horizontally centered, f.e. a *Questions* slide
- Bibliography and glossary support
- A build script that prevents your content from being cluttered with auxiliary files

---

## todo

- plain frame command
- convert theme to sty files [read](http://tex.stackexchange.com/questions/146529/design-a-custom-beamer-theme-from-scratch)