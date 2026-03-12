Use .eps for figures.

How to install environment:
```
sudo apt update
sudo apt install texlive-lang-japanese texlive-latex-extra texlive-science
```
Initial process:
```
rm -f main.aux main.bbl main.blg main.log main.dvi
platex main.tex
bibtex main
platex main.tex
platex main.tex
```
How to convert figures:
```
convert figs/hoge.png eps3:figs/hoge.eps
```
For compile:
```
platex main.tex
dvipdfmx main.dvi
```
Tips: To compile easily, just type 'com' on CUI:
```
echo "alias com='platex main.tex && dvipdfmx main.dvi && evince main.pdf'" >> ~/.bashrc
source ~/.bashrc
```