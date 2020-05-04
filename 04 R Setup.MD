



## R

### Installing current version of R on Debian


- Ensure Debian Unstable Repository is added to the sources.list (see '01 Pixelbook Setup.MD')
- Add the CRAN repository to the list in sources.list Cran [link](https://cran.r-project.org/bin/linux/debian/) here.
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

****

### Incorporating R into Anaconda/Jupyter Notebooks

Adding R to Jupyter notebooks installed via Anaconda is tricky. After a few failed attempts, I found the following worked ([stackoverflow link](https://stackoverflow.com/questions/44056164/jupyter-client-has-to-be-installed-but-jupyter-kernelspec-version-exited-wit/47895042)):

  - Open R from the **command line**

  - Install [IRKernel](https://irkernel.github.io/installation/) as well as the following dependencies: 'repr', 'IRdisplay', 'crayon', 'pbdZMQ', 'devtools'

  - Following [official instructions](https://irkernel.github.io/installation/), install 'IRkernel' and then make the kernel available to Jupyter by running the following:
    `IRkernel::installspec()` (for current user)
    `IRkernel::installspec(user = FALSE)` (for all users)

****
### Installing Packages in R:

  **Important note**: Install packages from the command line in base r

  Among the packages [recommended by RStudio](https://support.rstudio.com/hc/en-us/articles/201057987-Quick-list-of-useful-R-packages), I installed the following:

      `install.packages("rvest","tidyverse","shiny","dtwclust","caret","caretEnsemble","RCurl","RANN","WDI","leaflet","sf","fields","RODBC","DBI","Hmisc","zoo","devtools","jsonlite","rmarkdown","randomForest","multcomp","kableExtra","data.table","reshape","tm","plotly","forecast","tseries", "geojsonio", "tmap","corrplot","nnet" "ggmap","mapdata","mapview","rgdal","spData","fpc","tidyquant")`

  (_Ongoing issues with "xlsx" and Java_)


****
**Appendix**

Links used in Troubleshooting IRKernel:
  - R Installation can break [following a Conda R install](https://github.com/ContinuumIO/anaconda-issues/issues/11108)
  - [“jupyter kernelspec --version” exited with code 127](https://stackoverflow.com/questions/44056164/jupyter-client-has-to-be-installed-but-jupyter-kernelspec-version-exited-wit)
  - [R in Jupyter under Linux](https://community.rstudio.com/t/r-in-jupyter-under-linux/18594)
  - Official Documentation [link](https://docs.anaconda.com/anaconda/user-guide/tasks/using-r-language/
  - Datacamp [link](https://www.datacamp.com/community/blog/jupyter-notebook-r#comments)
  - https://github.com/ContinuumIO/anaconda-issues/issues/11108
  - https://www.storybench.org/install-r-jupyter-notebook/
