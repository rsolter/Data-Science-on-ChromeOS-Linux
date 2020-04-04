

### Python

**Python: Anaconda and Jupyer Notebooks**
Following guide posted [here](https://randlow.github.io/posts/python/set-up-pixelbook-python/#install-nodejs):


 1. Install _nodejs_ which is required for _tldr_ and Jupyter Lab:
 ` $ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
$ sudo apt-get install -y nodejs
$ sudo apt-get install -y build-essential`
 2. Install _tldr_ a more user-friendly version of `man`, short and useful help page for commands:
 `$ sudo npm install -g tldr
  $ tldr --update
  $ tldr conda`
 3. Download Anaconda from the [official website](https://www.anaconda.com/download/#linux) and install the .sh file using bash
 `$ bash Anaconda3-x.x.x-Linux-x86_64.sh`

**Adding Anaconda3 distribution to the Linux PATH**

While this can be done manually, it's actually [not recommended](https://docs.anaconda.com/anaconda/user-guide/faq/#) according to documentation on the Anaconda site:

  `We do not recommend adding Anaconda to the PATH manually. During installation, you will be asked “Do you wish the installer to initialize Anaconda3 by running conda init?” We recommend “yes”. If you enter “no”, then conda will not modify your shell scripts at all. In order to initialize after the installation process is done, first run source <path to conda>/bin/activate and then run conda init."`



**Libraries Worth Installing**
- 'BeautifulSoup'
- 'Selenium'


**Getting Selenium Working**
- Download [ChromeDriver - Webdriver](https://chromedriver.chromium.org/downloads)
- Place the 'chromedriver' file in '/usr/local/bin' using `sudo cp chromedriver /usr/local/bin`
- Run `sudo chmod ugo+x /usr/local/bin/chromedriver`


Install Firefox and [required Libraries/Packages](https://www.mozilla.org/en-US/firefox/74.0.1/system-requirements/)
