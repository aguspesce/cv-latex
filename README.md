# Curriculum Vitae

Sources for my resume written in LaTeX and using a custom template based on
[santisoler/CV](https://github.com/santisoler/cv)

My resume is available in a [PDF versions](https://raw.githubusercontent.com/aguspesce/cv-latex/gh-pages/resume.pdf).

## How to build

To build the PDF version of the resume from the source file, I use
[Tectonic](https://tectonic-typesetting.github.io/en-US/), which is a
modernizes self-contained LaTeX engine that's usually faster than using a
regular LaTeX compiler.

#### Step 1 - Install a Python distribution

If you already have Anaconda or Miniconda installed, you can skip this step.
If not, please follow the instructions for getting Anaconda up and running in
your system: https://docs.anaconda.com/anaconda/install/

#### Step 2 - Create the cv environment

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

If you cannot install Tectonic, you can still generate the PDF out of you
regular texlive installation. But you might need some extra packages:

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

All LaTeX template source code is distributed under the [BSD 3-clause
License](https://opensource.org/licenses/BSD-3-Clause).
