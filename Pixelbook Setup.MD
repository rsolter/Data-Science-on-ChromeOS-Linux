

# Setting up Linux on Chromebook for Data Science

The steps below are ones I took to set up my Pixelbook to run Linux and install some common Data Science tools, including R (and R Studio), Python (Anaconda distribution), and Jupyter notebooks. While my machine runs Debian, the instructions should be similar for any Linux distribution.

**Initial Steps**
 1. Set up Linux on your Chromebook following the instructions on [Google Support]([https://support.google.com/chromebook/answer/9145439?hl=en](https://support.google.com/chromebook/answer/9145439?hl=en)). Note that Debian is installed by default.
 2. Set password for Linux:
  - Switch to root with `$ sudo su`
  - Run `passwd your-username-here`
  - It will prompt you twice for a new password. To exit, type exit`
 3. Update your Linux distro and packages from the terminal:
  `sudo apt-get update && sudo apt-get dist-upgrade`
 4. Install **GDebi** for installing further packages, along with their dependencies:  `sudo apt install gdebi`


**Python: Anaconda and Jupyer Notebooks**
Following guide posted [here]([https://randlow.github.io/posts/python/set-up-pixelbook-python/#install-nodejs](https://randlow.github.io/posts/python/set-up-pixelbook-python/#install-nodejs))
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
  - Add the following line into the _.bashrc_ file and save with (basic vim commands)[https://www.howtoforge.com/vim-basics]:
  `export PATH="/home/<USERNAME>/anaconda3/bin/:$PATH"`
  - Rerun the _.bashrc_ file: `source .bashrc`
  - Activate the Python environment to check that you have successfully added Anaconda Python executable files into your Linux PATH: `source activate root`


**R & R Studio**

 1. Install basic R and development package `sudo apt-get install r-base r-base-dev`
 2. Download R Studio for [Ubuntu/Debian](https://rstudio.com/products/rstudio/download/#download)
 3. Install R Studio `sudo gdebi rstudio-1.2.5033-amd64.deb`
