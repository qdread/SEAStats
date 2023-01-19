# Getting Bayesian model software to work in R

My preferred setup for Bayesian models in R is to use the [brms][brms] modeling package. [brms][brms] is a R interface that allows you to write multilevel models with simple code that has similar syntax to the common mixed-model package [lme4][lme4]. "Behind the scenes" it fits a Bayesian model with the software [Stan][Stan] that has a state-of-the-art algorithm coded in C++ for quickly and efficiently sampling posterior distributions. There are two different packages that integrate between Stan and R, and you can specify which one to use in **brms**. While the default is [rstan][rstan], the best option which makes the models run the fastest is [CmdStanR][cmdstanr]. So in order to get **brms** working in R, you need to not only install **brms** but also install Stan and [CmdStanR][cmdstanr] on your system. Then you have to set up everything so that all those pieces of software can communicate with each other.

I want to give props to Paul B&uuml;rkner, the developer of `brms`, and all the developers of `Stan` including Andrew Gelman, Bob Carpenter, and lots of other hard-working people. Their hard work makes our life easier and our stats better!

## Installing brms, Stan, and CmdStanR

*Note: these instructions are intended for Windows users with R 4.2 installed.*

Run the following code in your RStudio console. First you have to install the `brms` package and all its dependencies from CRAN:

`install.packages('brms')`

Then you have to install CmdStanR. This is a summary of the [installation instructions](https://mc-stan.org/cmdstanr/articles/cmdstanr.html) on the CmdStanR homepage.

Install `CmdStanR` from its own repository:

`install.packages("cmdstanr", repos = c("https://mc-stan.org/r-packages/", getOption("repos")))`

Now, because everything will be running in C++, you need to make sure your system is configured to compile C++ programs:

```
library(cmdstanr)
check_cmdstan_toolchain(fix = TRUE)
```

You may get a message that Rtools is not installed on your computer. If you don't have Rtools installed, you will need to install it so that the brms models can compile. To install Rtools, quit RStudio, go to the [Rtools installation page on CRAN](https://cran.r-project.org/bin/windows/Rtools/rtools42/rtools.html), and download the **Rtools42 installer** using the link (it's a very large file, several hundred MB). Run the installer, and restart RStudio when the installation is complete. Go back to the previous step, starting from `library(cmdstanr)`, to reload the CmdStanR package and check the toolchain.

Once you have confirmed that the CmdStan toolchain is configured correctly, you can install Stan (more specifically, a version of it called CmdStan):

`install_cmdstan()`

All of the above only needs to be done once.

## Running brms

Every time you run an R session with brms, you need to load the package with 

`library(brms)`

Then I prefer to set the following options:

`options(mc.cores = 4, brms.backend = 'cmdstanr', brms.file_refit = 'on_change')`

This tells `brms` to run four chains in parallel (set this to a smaller number if your machine will blow up if you try to run 4 cores in parallel), ensures that `cmdstanr` is being used to fit the models, and also allows you to load pre-fit models from a file if you call the same model again which will save you time!
