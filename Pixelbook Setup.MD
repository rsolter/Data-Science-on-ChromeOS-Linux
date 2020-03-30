

## Setting up Linux on Chromebook for Data Science

The steps below are ones I took to set up my Pixelbook to run Linux (Debian 10) and install some common Data Science tools, including R (and R Studio), Python (Anaconda distribution), and Jupyter notebooks.

****

### Linux System

**Initial Steps**
 1. Set up Linux on your Chromebook following the instructions on [Google Support]([https://support.google.com/chromebook/answer/9145439?hl=en](https://support.google.com/chromebook/answer/9145439?hl=en)). Note that Debian is installed by default.
 2. Set password for Linux:
  - Switch to root with `$ sudo su`
  - Run `passwd your-username-here`
  - It will prompt you twice for a new password. To exit, type exit`
 3. Update your Linux distro and packages from the terminal:
  `sudo apt-get update && sudo apt-get dist-upgrade`
 4. Install **GDebi** for installing further packages, along with their dependencies:
  `sudo apt install gdebi`

**Install Atom**
  1. Download latest .deb file from [https://atom.io/](https://atom.io/)
  2. Navigate to wherever the .deb file is saved and run `sudo gdebi <deb_file_name>`

**Installing Linux libraries**

  In attempting to install certain pacakges on R, I was receiving error messaging pointing to missing libraries in my Linux install. For example, 'rvest' wouldn't install initially because 'libcurl' was not installed by default and [needed to be](https://community.rstudio.com/t/packages-installation-process-failed-on-linux-probably-due-to-missing-path-in-the-pkg-config-search-path/50619).

  Note that some instructions will ask that you [add-apt-repository](https://tecadmin.net/add-apt-repository-ubuntu/) before installing the software itself

  In total, I found myself needing to install the following to support installation of all the R packages I wanted to use (many pertained to mapping):

      -   `sudo apt install libcurl4-openssl-dev`

      -   `sudo apt install libssl-dev`

      -   `sudo apt install libudunits2-dev`

      -   `sudo apt install gdal-bin`

      -   `sudo apt install libgdal-dev`

      -   `sudo apt install libprotobuf-dev protobuf-compiler`

      -   `sudo apt install libv8-dev`

      -   `sudo apt install libjq-dev`

      -   `sudo apt install libfontconfig1-dev`

      -   `sudo apt install libcairo2-dev`


  I also needed to [install Java](https://www.r-bloggers.com/installing-rjava-on-ubuntu/):

      -  `sudo apt-get install -y default-jre`
      -  `sudo apt-get install -y default-jdk`
      -  `sudo R CMD javareconf`


**ZSH**

****

### Python

**Python: Anaconda and Jupyer Notebooks**
Following guide posted [here]([https://randlow.github.io/posts/python/set-up-pixelbook-python/#install-nodejs](https://randlow.github.io/posts/python/set-up-pixelbook-python/#install-nodejs)):

 1. Install _nodejs_ which is required for _tldr_ and Jupyter Lab:
 ` $ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
$ sudo apt-get install -y nodejs
$ sudo apt-get install -y build-essential`
 2. Install _tldr_ a short and useful help page for commands:
 `$ sudo npm install -g tldr
  $ tldr --update
  $ tldr conda`
 3. Download Anaconda from the [official website](https://www.anaconda.com/download/#linux) and install the .sh file using bash
 `$ bash Anaconda3-x.x.x-Linux-x86_64.sh`

**Adding Anaconda3 distribution to the Linux PATH**
  - Navigate to home director (e.g., /home/USERNAME)
  - Use the vim editor to open the _.bashrc_ file: `vim .bashrc`
  - Add the following line into the _.bashrc_ file and save with [basic vim commands](https://www.howtoforge.com/vim-basics):
  `export PATH="/home/<USERNAME>/anaconda3/bin/:$PATH"`
  - Rerun the _.bashrc_ file: `source .bashrc`
  - Activate the Python environment to check that you have successfully added Anaconda Python executable files into your Linux PATH: `source activate root`

****

### R

**Base R & R Studio**

 1. Install basic R and development package `sudo apt-get install r-base r-base-dev`
 2. Download R Studio for [Ubuntu/Debian](https://rstudio.com/products/rstudio/download/#download)
 3. Install R Studio `sudo gdebi <rstudio deb file>`


**Installing packages in R:**
Among the packages [recommended by RStudio](https://support.rstudio.com/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages), I installed the following:

    `install.packages("rvest","tidyverse","shiny","prophet","dtwclust","caret","WDI","leaflet","sf", "fields","RODBC","DBI","xlsx","Hmisc","zoo","devtools","jsonlite","rmarkdown","randomForest","multcomp","kableExtra","data.table","reshape","tm","plotly")`

_Ongoing issues with "xlsx", "Hmisc"_

 **Updating R on Linux**

 [link](http://scottsfarley.com/research/cloudcomputing/2016/07/19/Updating-R-on-Debian.html)

****

### Other Tools


**Docker**
[https://docs.docker.com/install/linux/docker-ce/debian/](https://docs.docker.com/install/linux/docker-ce/debian/)
