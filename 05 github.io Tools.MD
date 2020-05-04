
## github.io Tools

### Guides and tools for creating a github.io page with Jekyll

**Required software**

- Ruby 2.5 or greater
- Ruby Gems -
- GCC + Make: ensure installation with `gcc -v` `make -v`

https://jekyllrb.com/docs/installation/ubuntu/



Install [plainwhite](https://github.com/thelehhman/plainwhite-jekyll) theme: `gem install plainwhite`

**Other resources**
- [Jonathan McGlone's Guide](http://jmcglone.com/guides/github-pages/)
- [Jekyll website](https://jekyllrb.com/)




## Steps

1. Fork the repository [https://github.com/mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)
2. Remove the unnecessary folders and files. See link [here](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
3. Update the `GemFile`. See link [here](https://mmistakes.github.io/minimal-mistakes/docs/installation/#install-dependencies)




## What is jekyll?

Jekyll is a static website generator that can be written in markdown and is widely-used to build a blog from github repositories

Jekyll requires Ruby and Ruby Gems (a package manager for Ruby) to be installed.
	`sudo apt-get install ruby-full build-essential`

Following official guidance [here](https://jekyllrb.com/docs/installation/ubuntu/), it's best to avoid installing Ruby gems as root user:

		  `echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc

		  echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc

		  echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc

		  source ~/.bashrc`

Finally, we can install jekyll itself
	`gem install jekyll bundler`

_Checking to ensure they're installed_
`ruby -v`
`gem -v`
`jekyll -v`


## Creating a jekyll

Creation
`jekyll new <<name>>`

Execution
first time execution : `bundle exec jekyll serve`
normal execution: `jekyll serve`



## Error when updating/downloading ruby gems files:
https://stackoverflow.com/questions/49800432/gem-cannot-access-rubygems-org
