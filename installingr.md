---
layout: default
title: Installing R, RStudio, and packages
---

# R Installation Instructions

The following instructions describe how to set up all the software you will need for the "R Boot Camp," "Mixed Models in R," "Data Viz Basics," and the R part of "R for SAS Users" courses on your own machine. For the "Bayesian Mixed Models with brms" lesson, you will still need to follow these instructions, and you will also need to [install brms and CmdStanR]({{ 'brms_crash_course/simple_brms_install_instructions' | relative_url }}). 

## What you need to install

You will need to have the following software installed on your laptop:

- R 
- RStudio
- R packages:
  + [tidyverse](https://www.tidyverse.org/) (this includes the packages [dplyr](https://dplyr.tidyverse.org/), [tidyr](https://tidyr.tidyverse.org/), [readr](https://readr.tidyverse.org/), and [ggplot2](https://ggplot2.tidyverse.org/) that we will be working with)
  + [lme4](https://cran.r-project.org/web/packages/lme4/index.html)
  + [lmerTest](https://cran.r-project.org/package=lmerTest)
  + [nlme](https://cran.r-project.org/package=nlme)
  + [emmeans](https://cran.r-project.org/web/packages/emmeans/index.html)
  + [multcomp](https://cran.r-project.org/package=multcomp)
  + [easystats](https://easystats.github.io/easystats/)
  + [agridat](https://kwstat.github.io/agridat/)
  + several other packages that we will not use directly, but are used behind-the-scenes by the other packages: [patchwork](https://patchwork.data-imaginist.com/), [pbkrtest](https://cran.r-project.org/package=pbkrtest), [multcompView](https://cran.r-project.org/package=multcompView)

In addition, you will need to download the example datasets and code worksheets.
  
### Step 1. Install R

You will need to download R from [The Comprehensive R Archive Network](https://cran.r-project.org/), or CRAN. 

![CRAN R download screenshot]({{ 'images/cran_screenshot.png' | relative_url }}){: align="left" style="padding-right: 25px" width="400px" }

Go to the [CRAN website](https://cran.r-project.org/) and select the link to download the most recent version of R for your operating system. Follow the installation instructions. You will need admin rights to do this so you may need to get help from your IT staff.

### Step 2. Install RStudio

RStudio is an additional software program that makes it easy for you to write R code. It provides an interface that lets you run code, edit scripts, see what variables are in your working environment, and manage files. *RStudio is a program that makes it easier to use R, but you need to download both R and RStudio separately.*

![Posit RStudio download screenshot]({{ 'images/posit_screenshot.png' | relative_url }}){: align="left" style="padding-right: 25px" width="300px" }

As of early November 2022, RStudio is now distributed by a company called Posit. Go to the [RStudio Desktop download page](https://posit.co/download/rstudio-desktop/) and download the free version of RStudio Desktop. Again, you will need admin rights to do this on your USDA machine.

### Step 3. Install R packages

To install the packages we will be working with in this course, you will need to either install packages by typing a command into the R console, or install them using RStudio's package installation window. 

> **NOTE**: On some Windows systems, the default R package installation directory is inside the `Program Files` directory. Please ask your IT person to change the default R package installation directory to one that you have administrator rights to. This will allow you to install R packages in the future without involvement from an administrator.

##### Installing packages from the R console

- Open RStudio.
- Type the following command into the R console and press Enter. Voila!

```
install.packages(c("tidyverse", "lme4", "lmerTest", "nlme", "emmeans", "multcomp", "easystats", "agridat", "patchwork", "pbkrtest", "multcompView"))
```

##### Installing packages from the RStudio package installation window

You can also install the packages using the RStudio package installation dialog.

- The files pane has a tab called "Packages." Click on the "Packages" tab and then click the "Install" button in the upper left.
- Type the package names, separated by space or comma, into the box:

```
tidyverse, lme4, lmerTest, nlme, emmeans, multcomp, easystats, agridat, patchwork, pbkrtest, multcompView
```

It should look like this (with a few more package names listed):

![installation dialog]({{ 'images/install_dialog.png' | relative_url }})

- Ensure that the library you are installing to is somewhere in a folder you can write to without admin rights. (See above.) 
- Ensure that "install dependencies" is selected.
- Click "Install."

#### Step 4. Download the worksheets and example datasets

Go back to the [main page](/index.html) and download the .zip files containing the example datasets and worksheets needed for the lessons. Unzip them to a directory on your local file system. You will need to specify the file path to that directory when you load the example datasets during the workshop.