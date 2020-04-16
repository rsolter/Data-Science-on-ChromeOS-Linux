

### Python

**Python: Anaconda and Jupyer Notebooks**
Following guide posted [here](https://randlow.github.io/posts/python/set-up-pixelbook-python/#install-nodejs):


 1. Install _nodejs_ which is required for _tldr_ and Jupyter Lab:

 ` $ curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -`

  `$ sudo apt-get install -y nodejs`

  `$ sudo apt-get install -y build-essential`

 2. Install _tldr_ a more user-friendly version of `man`, short and useful help page for commands:
  `$ sudo npm install -g tldr`

  `$ tldr --update`

  `$ tldr conda`

 3. Download Anaconda from the [official website](https://www.anaconda.com/download/#linux) and install the .sh file using bash. Ensure that you are in your home directory before doing so (i.e., /home/USERNAME)
 `$ bash Anaconda3-x.x.x-Linux-x86_64.sh`

**Adding Anaconda3 distribution to the Linux PATH**

  Open the .bashrc file: `vim .bashrc`

  Add the following line `export PATH="/home/<USERNAME>/anaconda3/bin/:$PATH"`

  Rerun the .bashrc file `source .bashrc`

  Activate the Python environment to check that you have successfully added Anaconda Python execuable files into your Linux PATH. `source activate root`


**Setting up Jupyter Lab**

  Follow steps in the same [blog](https://randlow.github.io/posts/python/set-up-pixelbook-python/#id12) referred to above:

  - Obtain the IP address: `ip addr`

  - Analyze output and copy the second IP address refered to in the 'Broadcast section'. Something like **100.115.92.205**

  - Generate a _jupyter_notebook_config.py_ in the directory _home/<user>/.jupyter/_:
      `jupyter notebook --generate-config`

  - Open the congif file and update the following lines:

  `c.NotebookApp.allow_origin ='*' #allow all origins
   c.NotebookApp.ip = '100.115.92.205' # listen to specific IP address`

   - Test to ensure everything was installed correctly:
   `jupyter notebook`
   `jupyter lab`
   `spyder`
   `anaconda-navigator`





****

**Libraries worth Installing**
- 'BeautifulSoup'
- 'Selenium'


**Getting Selenium Working**
- Install a browser of your choice on the Debian partition, I installed Chrome using instructions [here](https://linuxize.com/post/how-to-install-google-chrome-web-browser-on-debian-9/)
- Download [ChromeDriver - Webdriver](https://chromedriver.chromium.org/downloads)
- Copy the 'chromedriver' file to '/usr/local/bin' using `sudo cp chromedriver /usr/local/bin`
- Run `sudo chmod ugo+x /usr/local/bin/chromedriver`

Alternatively, I could have installed Firefox and the [required Libraries/Packages](https://www.mozilla.org/en-US/firefox/74.0.1/system-requirements/)
