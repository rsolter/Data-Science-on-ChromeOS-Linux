# Setting up Git

Referred to the [guide](https://kbroman.org/github_tutorial/pages/first_time.html) guide written by Karl Broman.

Set up username and email:
`$ git config --global user.name "John Doe"`
`$ git config --global user.email johndoe@example.com`

Setting up Atom as the default editor. Code for others linked [here](https://help.github.com/en/github/using-git/associating-text-editors-with-git)
`$ git config --global core.editor "atom --wait"`

Enable colored output in the terminal:
`$ git config --global color.ui true`

Generate a SSH key using your email address associated with GitHub:
- `$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
- Press Enter to save the key to the default location (/Users/you/.ssh/id_rsa)
- Type a secure passphrase twice

Add the SSH key to the ssh-agent [link](https://gist.github.com/JoaquimLey/31deaf857521319fcba8ee9f7af47299)
- `$ eval "$(ssh-agent -s)"`
- `$ ssh-add ~/.ssh/id_rsa`

Add the new SSH key to your GitHub Account [link](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
- Copy the SSH key to your clipboard.
- `$ pbcopy < ~/.ssh/id_rsa.pub`
- NOTE: Debian does not include 'pbcopy', use 'xclip' [instead](https://www.ostechnix.com/how-to-use-pbcopy-and-pbpaste-commands-on-linux/) and then run code above once editing aliases.
- Add SSH Key to your GitHub by accessing Settings > SSH Keys and GPG Keys > New SSH Key/Add SSH Key

# Creating a new repository from a local working directory:

[Reference](https://help.github.com/en/github/importing-your-projects-to-github/adding-an-existing-project-to-github-using-the-command-line)

- Create a new repository on GitHub.com
- Initialize git inside your working directory `git init`
- Add the files and commit `git add`, `git commit -m <message_here>`
- Add the URL for the remote repository where your local repository will be pushed and verify
  - `$ git remote add origin <remote repository URL>`
  - `$ git remote -v`
- Push the changes: `$ git push -u origin master`



[Adding a remote repository](https://help.github.com/en/github/using-git/adding-a-remote)
- `$ git remote add origin https://github.com/user/repo.git`
- If the remote URL needs to be reset use `$ git remote set-url origin https://github.com/USERNAME/REPOSITORY.git`



# Cloning existing repositories:

- Navigate to the repository you'd like to clone on github
- Click "Clone or Download" then choose "Clone with HTTPS" and click the clipboard icon to copy
- Within the terminal, navigate to whichever to the location where you want the cloned directory to be made
- Type `git clone` and paste the copied HTTPS URL
- Press 'Enter'
