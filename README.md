# install-r-on-ubuntu
Instructions for installing R on Ubuntu, including RStudio.

## Notes
- At the moment, these instructions are for installing Microsoft R Open, but can be modified for CRAN-R
- R Open is no the same as R Client--consider installing R Client instead if intend to use Machine Learning Server
- This is my current preferred baseline configuration and packages

## 1. Download installer from MS R Open
https://mran.microsoft.com/documents/rro/installation/

https://mran.microsoft.com/download/#download

## 1.(a) Alternatively, download installer for MS R Client
https://docs.microsoft.com/en-us/machine-learning-server/r-client/install-on-linux
And follow instructions on this page.

## 2. Run these bash commands, adjust cmd line for specific file downloaded
`$ sudo tar -xf microsoft-r-open-3.4.0.tar.gz`

`$ cd microsoft-r-open/`

`$ sudo ./install.sh`

## 3. Download RStudio .deb installer
https://www.rstudio.com/products/rstudio/download/

## 4. Run these bash commands, adjust cmd line below as appropriate
`$ sudo dpkg -i /path/to/deb/file`

`$ sudo apt-get install -f`

## 5. Get package dependencies
`$ sudo apt-get install build-essential libcurl4-gnutls-dev libxml2-dev libssl-dev`

`$ sudo apt-get install gfortran`

## 6. Install these packages from within R
`> install.packages('devtools')`

`> library(devtools)`

`> install.packages(c('curl', 'httr'))`

`> install.packages('tidyverse')`

`> install.packages(c('doParallel', 'doMC', 'doRedis')`

`> install_github(c("Azure/rAzureBatch", "Azure/doAzureParallel"))`
