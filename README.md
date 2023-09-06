Versão em Português do livro Homotopy Type THeory

This is a textbook on informal homotopy type theory.
It is part of the [Univalent foundations of mathematics](http://www.math.ias.edu/sp/univalent)
project that took place at the Institute for Advanced Study in 2012/13.

## License

This work is licensed under the
[Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/).

## Distribution

Compiled and printed versions of the book are available at the
[homotopy type theory website](http://homotopytypetheory.org/book),
and nightly builds are available on the
[github wiki](https://github.com/HoTT/book/wiki/Nightly-Builds).

## Editing the book

This book is not a community project, but we do welcome our readers to suggest improvements. The best way to propose an edit is to [open a pull request](https://github.com/HoTT/book/compare) with your suggested change. You can also [open an issue](https://github.com/HoTT/book/issues/new/choose) if you do not have a concrete proposal yet. The issues and the pull requests are dedicated to improvements, questions, and other issues pertaining to the HoTT book itself. General discussions about homotopy type theory and topics related to the wider HoTT community are welcome at the [homotopytypetheory google group](https://groups.google.com/g/homotopytypetheory) or at the [HoTT zulip](https://hott.zulipchat.com). For further directions about editing the book, see the [guidelines for contributions](https://github.com/HoTT/book/blob/master/CONTRIBUTING.md)

## Code of conduct

For many, the HoTT book is their introduction to our subject and our diverse community, including people from any nationality, gender identity, sexual orientation, race, color, ability, and background. In order to ensure for everyone a welcoming and inclusive environment in our discussions, we follow the guidelines of the [GitHub code of conduct](https://docs.github.com/en/site-policy/github-terms/github-community-forum-code-of-conduct). You can expect from the authors and any participant that we are kind and respectful in discussions, that we use inclusive language, and that we do our best to understand each other's different perspectives. It might not always be that we accept the change in the way you proposed it, but we always value your input, regardless of your level of experience or status within the community.

## Prerequisites and compilation

To compile the book for yourself you need a fairly new version of LaTeX.
[Texlive](http://www.tug.org/texlive/) 2012 is confirmed to work. You might need
to install some packages; see `main.tex` for packages that are used by the book.

[BasicTeX](http://www.tug.org/mactex/morepackages.html), which is a minimalistic
version of MacTeX, is confirmed to work once the following packages have been
installed: `tlmgr`, `install`, `braket`, `comment`, `courier`, `enumitem`,
`helvetic`, `mathpazo`, `nextpage`, `ntheorem`, `palatino`, `rsfs`, `stmaryrd`,
`symbol`, `titlesec`, `wallpaper`, `wasy`, `wasysym`, `xstring`, `zapfding`.

You also need the `make` utility. The book is a fairly complex piece of LaTeX
code. Also, the file `version.tex` is generated on the fly, so you will need the
`make` utility with which you can compile the main files, as follows:

* `make hott-online.pdf` -- the book appropriate for online reading, with colors and green links
* `make hott-ebook.pdf` -- the book with small margins, suitable for ebook readers
* `make hott-ebook-wide.pdf` -- the book with small margins, suitable for ebook readers, wider page
* `make hott-ebook-narrow.pdf` -- the book with small margins, suitable for ebook readers, narrower page
* `make hott-letter.pdf cover-letter.pdf` -- the book in black & white, letter paper format,
   for printing at home, as well as a color cover (just two pages)
* `make hott-a4.pdf cover-a4.pdf` -- the book in black & white, A4 paper format,
   for printing at home, as well as a color cover (just two pages)
* `make hott-arxiv.pdf` -- the version that is uploaded to arXiv
* `make hott-letter-exercises.pdf` -- the book in black & white, letter paper format, but with exercises one-per-page
* `make hott-a4-exercises.pdf` -- the book in black & white, A4 paper format, but with exercises one-per-page
* `make hott-ustrade.pdf cover-lulu-hardcover.pdf cover-lulu-paperback.pdf` --
   the book in US Trade format, without cover, used for the bound copy available
   at http://lulu.com/
* `make exercise_solutions.pdf` -- (some) solutions to exercises
* `make errata.pdf` -- errata for the HoTT Book, first edition

Note: once `make` is run so that `version.tex` is generated, you need not run `make` every time you make
a change to the source file. You can just perform the usual LaTeX cycle from your favorite editor.

#### Compiling without `make`

If you do not have `make` (for example, because you are on MacOS and you did not
install the XCode command-line utilities), you can still fake it as follows.
Create the file `version.tex` and put in it (where "Joe Hacker" should be
replaced with your name):

    \newcommand{\OPTversion}{Joe-Hacker-version}

Then use whatever tools you normally do to compile LaTeX. The main LaTeX files are called 
`hott-XXX.tex`. But you really should have `make`, you know.

