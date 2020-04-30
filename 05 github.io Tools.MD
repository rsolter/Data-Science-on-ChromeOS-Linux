## github.io Tools

### Guides and tools for creating a github.io page with Jekyll

**Required software**

- Ruby 2.5 or greater `sudo apt-get install ruby-full build-essential`
- Ruby Gems -
- GCC + Make: ensure installation with `gcc -v` `make -v`

https://jekyllrb.com/docs/installation/ubuntu/

Following guide [here](https://jekyllrb.com/docs/installation/ubuntu/), it's best to avoid installing Ruby gems as root user:

  `echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
  echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
  echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
  source ~/.bashrc`



**Other resources**
- [Jonathan McGlone's Guide](http://jmcglone.com/guides/github-pages/)
- [Jekyll website](https://jekyllrb.com/)
