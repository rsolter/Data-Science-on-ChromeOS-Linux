

### R

**Base R & R Studio**

 1. Install basic R and development package `sudo apt-get install r-base r-base-dev`
 2. Download R Studio for [Ubuntu/Debian](https://rstudio.com/products/rstudio/download/#download)
 3. Install R Studio `sudo gdebi <rstudio deb file>`


**Installing packages in R:**
Among the packages [recommended by RStudio](https://support.rstudio.com/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages), I installed the following:

    `install.packages("rvest","tidyverse","shiny","prophet","dtwclust","caret","WDI","leaflet","sf","fields","RODBC","DBI","xlsx","Hmisc","zoo","devtools","jsonlite","rmarkdown","randomForest","multcomp","kableExtra","data.table","reshape","tm","plotly","forecast","tseries")`

(_Ongoing issues with "Hmisc", "reshape"_)

****

 **Updating R on Debian**
As mentioned in '01 Pixelbook Setup', Debian runs on much older, more stable versions of software. Here is a [link](http://scottsfarley.com/research/cloudcomputing/2016/07/19/Updating-R-on-Debian.html) for updating R manually.

****

**Adding R Environment to Anaconda/Jupyter Notebooks**



  Datacamp [link](https://www.datacamp.com/community/blog/jupyter-notebook-r#comments)

  Requires **irkernel** to be [installed via conda](https://medium.com/@kyleake/how-to-install-r-in-jupyter-with-irkernel-in-3-steps-917519326e41).

  Also requires [r-essentials?](https://stackoverflow.com/questions/47615044/installin-r-in-jupyter-notebook)

  [Error I'm seeing](https://github.com/ContinuumIO/anaconda-issues/issues/1133)

  Possible help: https://github.com/ContinuumIO/anaconda-issues/issues/11108
