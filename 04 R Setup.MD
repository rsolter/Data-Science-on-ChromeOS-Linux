


## R

### Instructions for R, R Studio, and Jupyter Notebooks


Steps

- Add the cran repository to the list in sources.list Cran [link](https://cran.r-project.org/bin/linux/debian/) here.
    - `sudo nano /etc/apt/sources.list`
    - `deb http://cloud.r-project.org/bin/linux/debian buster-cran35/`
- Following guide from Digital Ocean
    - `sudo apt install dirmngr --install-recommends`
    - `sudo apt install software-properties-common`
    - `sudo apt install apt-transport-https`
- Fetch and import the current key from [Cran](https://cran.r-project.org/bin/linux/debian/)
    - `apt-key adv --keyserver keys.gnupg.net --recv-key 'E19F5F87128899B192B1A2C2AD5F960A256A04AF'`
- Install up to date version of R
    - `apt-get update`
    - `apt-get install r-base r-base-dev`

- Download R Studio for [Ubuntu/Debian](https://rstudio.com/products/rstudio/download/#download)

- Install R Studio `sudo gdebi <rstudio deb file>`


### Packages in R:
Among the packages [recommended by RStudio](https://support.rstudio.com/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages), I installed the following:

    `install.packages("rvest","tidyverse","shiny","prophet","dtwclust","caret","WDI","leaflet","sf","fields","RODBC","DBI","xlsx","Hmisc","zoo","devtools","jsonlite","rmarkdown","randomForest","multcomp","kableExtra","data.table","reshape","tm","plotly","forecast","tseries")`

(_Ongoing issues with "Hmisc", "reshape"_)


## Incorporating R into Anaconda/Jupyter Notebooks**

Adding R to functional notebooks is tricky, and I have not yet successfully achieved it. Some useful links and tutorials are listed below:




  Official Documentation [link](https://docs.anaconda.com/anaconda/user-guide/tasks/using-r-language/)

  Datacamp [link](https://www.datacamp.com/community/blog/jupyter-notebook-r#comments)

  Requires **irkernel** to be [installed via conda](https://medium.com/@kyleake/how-to-install-r-in-jupyter-with-irkernel-in-3-steps-917519326e41).

  Also requires [r-essentials?](https://stackoverflow.com/questions/47615044/installin-r-in-jupyter-notebook)

  [Error I'm seeing](https://github.com/ContinuumIO/anaconda-issues/issues/1133)

  Possible help:
  - https://github.com/ContinuumIO/anaconda-issues/issues/11108
  - https://www.storybench.org/install-r-jupyter-notebook/
