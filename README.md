# RCOMPILE #
Small ever changing R script for compiling **knitr** `.Rtex` and **LaTeX** `.tex` files.

Put this in your `path` (often suggested to be in your home directory:
`$HOME/bin`, you might be forced to add this to your `PATH` variable,
i.e., modify your `.bashrc`, but your `.profile` might be already doing this)

make it executable: `sudo chmod +x rcompile`

run from anywhere: `rcompile my_document.Rtex`. 

(you can rename `rcompile` to `rlatex` or anything you want)

### Description ###
Assuming your `latex` and `bibtex` (and `Rscript`) are callable, this will do
standard three-pass compilation of your **LaTeX** document. If you are using
bibtex, three compilations are required for fully updating everything.

Additionally, if input file is **knitr** `.Rtex` file, this will additionally
compile your file in knitr (assuming you have it installed).

### Todo ###
This script is changing from time to time to coop with my needs. Its core is
very simple (calling 4x external binary) and the rest is just error catching,
any new update is just making existing code "smarter".

A bit more functionalities might appear in future:
- silent execution
- specification for number of passes
- detecting bibliography keyword and running bibtex only if bibliography is
detected? (this could be a bit more complicated as with `\include`, bibliography
might be specified in other files
- support for Windows (I have no access to Windows machine and no idea how
knitr/LaTeX users work there, so if you need something similar, contact me
and we can make it together!)
