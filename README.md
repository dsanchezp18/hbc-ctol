# Honesty by Convenience: Corruption Tolerance in Ecuador (README)

This is the source code (R) for my Bachelor's thesis for the degree of Economics, BA in Universidad San Francisco de Quito (Ecuador). Between 2014-2016, corruption tolerance greatly increased in Ecuador. Why? 

In memory of the late Jorge Pazmiño (1941-2021).

I've taken great care in trying to ensure maximum reproducibility of my research "paper". Thus, one of the things I have done is upload all the code required to compile a revised version of the document. This version includes minor revisions in format for a better reading experience and some eliminated elements due to copyright reasons. More info about this can be found in the paper itself.

So here you will be able to find my paper and reproduce it completely. I assume you are already knowledgeable of R, Rstudio, LaTeX. However, if you're not and somehow you're here, I recommend learning LaTeX from the Overleaf tutorials, R from the [R For Data Science marvelous textbook](https://r4ds.had.co.nz/) and *sweave/knitr* from this [other textbook](https://www.routledge.com/Dynamic-Documents-with-R-and-knitr/Xie/p/book/9781498716963). 

However, there are some things that need to be considered before doing so: 

- Obviously you'll first need to have an R distribution installed, as well as Rstudio.

- You'll need to download a LaTeX distribution. TeX Live is the one that I use. Some instructions can be found [here](https://tug.org/texlive/acquire-netinstall.html). 

- You'll have to set up your global options in R so that `.Rnw` files are weaved with *knitr*, and that the compiler is Xe LaTeX. Otherwise the Times New Roman font mandated by my university won't work for you (and who knows what sorts of other errors will appear). 

- The execution of the `main_file.rnw` file will compile the complete document. However, to compile the child documents in standalone mode, the paths in this main file for the loading of databases must be changed to absolute paths. This means that, instead of `load('databases/lapop_ecu.Rdata')` you'll have to change it to `load(C:\Users\Daniel Sanchez\Documents\personal\hbc-ctolecu)`, changing the `C:\\...` to wherever you loaded the uncompressed package. If you do not do this, you'll get the following error: `Error in readChar(con, 5L, useBytes = TRUE): cannot open the connection`. You'll have to rinse and repeat for the other three `load()` commands to load the remaining dataframes. The same thing should be done to the `\addbibresource` command in the main file preamble if you want to generate standalone bibliographies. I'm currently working on a solution for this. 

You can find another repository, [hbc-prelim](https://github.com/dsanchezp18/hbc-prelim), where I included more R code which I used to wrangle and analyze the data and be able to manipulate and create the dataframes that I load on this project. The `df` and `df46` dataframes that I load in this repository are created from scratch there. If you'd like to replicate my results using the freely available LAPOP Americas Barometer as seen [here](https://www.vanderbilt.edu/lapop/free-access.php), do take a look at that repository. 

These are the only things you'll need to do, to my own knowledge, to easily compile the paper into your own computer. Please, please let me know if you run into any issues, I'll do my best trying to help you: dsanchezp998@gmail.com. I am also open to suggestions, criticisms, comments and anything else you might need.

A spanish version of the document will be made available soon. 

This repository and all those that are created in relation to it, are a tribute to my late grandfather, Jorge Enrique Pazmiño Enríquez. In his desire to see his grandsons foster a freer, fairer, and worthier society, I have tried to contribute by posting my research for the world to use. I hope it is put to good use. 

Thank you for reading, and happy analysis!

Regards,

Daniel
