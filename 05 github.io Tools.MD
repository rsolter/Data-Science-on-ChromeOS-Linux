
## Guides and tools for creating a github.io page with Jekyll


**Resources**
- [Jonathan McGlone's Guide](http://jmcglone.com/guides/github-pages/)
- [Jekyll website](https://jekyllrb.com/)
- [Giraffe Academy - YouTube Tutorial](https://www.youtube.com/watch?v=T1itpPvFWHI&list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB&index=1)
- [Debian Error Handling](https://stackoverflow.com/questions/49800432/gem-cannot-access-rubygems-org)
- Another useful [tutorial](https://decentralized-id.com/how-to-contribute/website-config-minimal-mistakes/)





### What is jekyll?

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


### Creating a jekyll

Creation
`jekyll new <<name>>`

Execution
first time execution : `bundle exec jekyll serve`
normal execution: `jekyll serve`



### Error when updating/downloading ruby gems files:
https://stackoverflow.com/questions/49800432/gem-cannot-access-rubygems-org


### Adding theme

Inside existing gemfile, add `gem "minimal-mistakes-jekyll"`
Fetch the updated gem file `bundle install`
Update the  config.yml with `theme: minimal-mistakes-jekyll`

Finalize by typing `bundle exec jekyll serve`.

However, this will Building Warning errors for Layout: Page and Layout: Post.
This is caused by incompatible layout templates created when switching pages. For a quick fix, ensure any and all layout: '' in the front matter of each .MD file read `layout: default`
