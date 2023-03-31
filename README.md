# Curriculum Vitae

This repository contains the source files for my resume, written in LaTeX using a custom template based on [santisoler/CV](https://github.com/santisoler/cv)

My CV is available in a [PDF versions](https://raw.githubusercontent.com/aguspesce/cv-latex/gh-pages/resume.pdf).

## How to build

To build the PDF version of the resume from the source file, I use
[Tectonic](https://tectonic-typesetting.github.io/en-US/), a modern and self-contained LaTeX engine that is faster than regular LaTeX compilers.

### Step 1 - Install a Python distribution

If you already have Anaconda or Miniconda installed, you can skip this step. 
Otherwise, please follow the instructions to get Anaconda up and running on your system by visiting: [https://docs.anaconda.com/anaconda/install/](https://docs.anaconda.com/anaconda/install/)

### Step 2 - Create the cv environment

Now you could install all the dependencies through the conda package manager:

```
conda env create -f environment.yml
```

And then activate the environment:

```
conda activate cv
```

You can use the `Makefile` to build the PDF:

- `make all`: **build** the PDF.
- `make show`: **open** the PDF with your favourite PDF reader.
- `make clean`: **remove** the built PDF.

### Using texlive

If you cannot install Tectonic, you can still generate the PDF using your regular texlive installation.
However, you may need some extra packages:

For Ubuntu or Debian:

- `latexmk`
- `texlive`
- `texlive-latex-extra`
- `texlive-xetex`
- `texlive-fonts-extra`

To build the PDF run:

```
mkdir _output
latexmk -xelatex -outdir=_output cv.tex
```

## License

The LaTeX template source code is distributed under the [BSD 3-clause
License](https://opensource.org/licenses/BSD-3-Clause).
