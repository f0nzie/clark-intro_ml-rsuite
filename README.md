# clark-intro-ml-rsuite

## ebook built with rsuite. How is this different
This ebook was created with bookdown. It is different in the way it has been built, and can be rebuilt.

I have used `rsuite` to make it fully reproducible. This ebook is, in some way, difficult to match all the dependencies. 
Unfortunately, not all good things last forever. After a package upgrade the ebook may stop building. These are all the packages required to build this ebook:

```
logging,
  tidyext,
  visibly,
  DT, 
  viridis, 
  kableExtra, 
  broom, 
  pander, 
  tidyr,
  tidyverse, 
  htmltools,
  mgcv,
  dplyr,
  doParallel,
  caret,
  ggRandomForests,
  randomForestExplainer,
  kernlab,
  xgboost,
  lime,
  network,
  sna,
  DiagrammeR,
  ggnetwork,
  scico,
  plotly,
  heatR,
  tibble,
  lazerhawk,
  GGally,
  GPArotation
```  


So, what I did is creating an isolated environment for the book, one where all the packages are spelled out in advance so the ebook can be rebuilt after: (i) an R re-installation, (ii) a new R version, or (iii) a full package upgrade. The book will be able to be regenerated to the CRAN snapshot at the time it was first built.

Because `rsuite` allows a supervising project on top of other projects or packages, you can control:

1. the date of the snapshot; 
1. the R version under you want the book to be built; 
1. the names of all the packages that satisfy the dependencies for the book to work; 
1. define a place for the source code of the package if the package is not in CRAN; 
1. a master project and a master package that takes care of reproducing the whole book, again and again, even after changing the operating system.
1. a cntrolling environment with its own scripts and configuration files.

## How to reproduce this ebook yourself
* Download and install the **RSuite** client. Available for Linux, Mac and Windows.
* Install the rsuite package with `rsuite install`
* Clone or download this repository.
* Change to this repo folder and install the dependencies on its own isolated reproducible environment. Use `rsuite proj depsinst`
* Build the project with `rsuite proj build`
* Go to the folder `/work/book`, or where the bookdown lives, and open the `.Rproj` project.
* Click on the RStudio **Build Book** button.
* Enjoy


## Publishing this book in Github pages
To publish this book in Github pages, push the folder `./work/introduction-to-machine-learning/public` as a branch `gh-pages` with this git command:

```
git subtree push --prefix work/introduction-to-machine-learning/public https://github.com/f0nzie/clark-intro_ml-rsuite.git gh-pages
```

If you are building this in your own machine and own repository, change my username `f0nzie` by your own. This example assumes you are using `https` instead of `ssh`. Do not forget to activate `gh-pages` in *Settings, GitHub Pages*.


## References
* Original repository [m-clark/introduction-to-machine-learning](https://github.com/m-clark/introduction-to-machine-learning)
* [Online ebook](http://m-clark.github.io/introduction-to-machine-learning/)
* [Michael Clark's website](https://m-clark.github.io/)
* [Bookdown website](https://bookdown.org/)
