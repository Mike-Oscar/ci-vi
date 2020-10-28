# ci-vi
LaTeX source code for my personal design of the curriculum vitae.

## Purpose
I want to write my CV in LaTeX to create something personal, original and good-looking. Moreover, I use this as an excuse to learn to write a LaTeX document class. Probably I will succeed mostly in the last thing.

## References
I take inspiration mainly from the document classes [moderncv](https://www.ctan.org/pkg/moderncv) by Xavier Danaux and [limecv](https://ctan.org/pkg/limecv) by Olivier Pieters because they are the most professional and clean I have found, even though I would like to introduce some changes. Obviously, I may have been inspired by many other CV styles and examples I have seen over time, but in this case my intentions are far from copy the creation of others.

## Notes
Although there is the possibility to insert the .ins file inside the .dtx file with the purpose of avoiding the detection of the former as malicious, I prefer to keep them separated as it seems to be the usual choice for package distribution. Moreover, in this case I like the resulting separation of tasks, in fact during development I just have to "compile" the .ins file to obtaind the "code" to test, i.e. the .cls file, while I think the documentation should not need the same amount of testing.

Passing ci-vi.ins to pdfLaTeX produces ci-vi.cls: lines starting with `%` are deleted, even if they start with the `%<...>` tag, except for lines starting with `%<class>` (in this case), which are added to the class file along with uncommented lines.
Passing ci-vi.dtx to pdfLaTeX produces ci-vi.pdf: the uncommented lines are read until the call to `\DocInput{}`, then the file ci-vi.dtx itself is added inside the `document` environment with `%` symbols removed, turning previous comments in executable LaTeX code.

## License
The present material is published under the BSD-3-Clause License but the LaTeX and Tex-related code provided in these files are covered by the LaTeX Project Public License (LPPL) Version 1.3c. The idea is to grant freedom of action while preserving the existing well-oiled code through the LPPL, whose updated version is stated in its entirety at http://www.latex-project.org/lppl.txt.

## Fun facts
I had no idea how to make a good title for this repo (or at least, one following my twisted sense of humor), so I decided to use the writing of the acronym pronounced in Italian. Very simple, very trivial, anyway this makes a serious thing like a CV a cute one. No, I am not so proud.
