# Visualizing Spin Chains with TikZ

![Spin Chain](diagram.jpg)

This repository contains a LaTeX file [diagram.tikz](diagram.tikz) with a generated picture for a spin chain.

In the diagram, a spin is represented by a circle with an (randomly directed) arrow, and the interactions between them are represented by rounded rectangles. The interactions for the odd and even bonds are different.

To compile the diagram, please use the following command:

```bash
# "lualatex" is part of the "texlive" distribution
lualatex diagram.tikz
```

Alternatively, for the LaTeX Workshop extension in Visual Studio Code, you can compile with the command:

1. `Ctrl+Alt+P` calls the command palette
2. Type `recipe`, and select `LaTeX Workshop: Build with recipe`
3. Select `latexmk (lualatex)` from the list
4. `Ctrl+Alt+V` to view the PDF file

A PDF file `diagram.pdf` will be generated. To convert it to an `jpg` image, you can use the following command:

```bash
# "magick" is provided by the "imagemagick" tool
magick -density 300 diagram.pdf -quality 90 diagram.jpg
```