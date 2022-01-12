# Lab instructions for TFY4155/FY1003
![LaTeX](https://img.shields.io/badge/latex-%23008080.svg?style=for-the-badge&logo=latex&logoColor=white)

*This README was written for the January 2022 revision where the document was translated to English.*

# The Kaobook document class
This LaTeX document uses the [Kaobook](https://github.com/fmarotta/kaobook) document class, which is based on the KOMA-script library.
It features a "1.5 column" layout: a side-justified main column with a wide margin for notes, figures, and captions.

## Compiling
In order to compile, you need the `Kaobook` files.
For this project, we need `kaobook.cls`, `kao.sty`, and `kaotheorems.sty`.
These files must be placed in the project root, which they are, or included in your Latex system's include dir (`~/texmf/tex/latex/kaobook/` on modern Linux systems).
For more information on how to kompile Kaobook, refer to the [documentation, section instructions](https://github.com/fmarotta/kaobook/tree/master/instructions/normal_usage).

## Notes and issues
The margin figures and tables are slightly more cumbersome to position than normal figures, as they do not float.
They are placed exactly where included.
This may sometimes look ugly.
Either move where in the code the figure is positioned, or add an offset, such as 
```latex
\begin{marginfigure}[-2cm]  % Move figure 2cm up.
...

```
See the [example document](https://github.com/fmarotta/kaobook/blob/31deae764f3901e5616ca3c3fbe5473d4b75c2d2/example_and_documentation.pdf) for more details.

# Strucutre of the document
The main file of the document i `Elmag-labhefte-2021.tex`, which imports files from the `tex` folder.
Each chapter is in its own file in the `tex` folder, with the English version having the name `chaptername_english.tex`.
The original Norwegian files, `chaptername.tex`, are kept for reference.

*Note: The file `tex/kapittel2.tex` is not used, but is kept for reference.*

## Notes and issues
Some of the code is ancient, using TeX, as opposed to LaTeX, syntax in some places.
Also, several figures are made with the Picture environment, instead of the now mor common Tikz package.
This makes the document somewhat difficult to work with.
An effort was made in January 2022 to modernize some of the code, but still much old code remains.
