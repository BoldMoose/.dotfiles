# More Information
Based on [Best way to manage your dotfiles](https://medium.com/@simontoth/best-way-to-manage-your-dotfiles-2c45bb280049)
# Setup a New Machine
Clone the repo as a bare repo:
```
git clone --bare git@github.com:BoldMoose/dotfiles.git $HOME/.dotfiles
```
Checkout the new dir, specifying the working tree a `~/`:
```
git --git-dir=$HOME/.dotfiles --work-tree=$HOME checkout
```
Set local config to not show untracked files by editing ~/.dotfiles/config to add the following:
```
[status]
	showUntrackedFiles = no
```

# Making changes
An alias is provided for ease of making changes to the bare repo:
```
alias dotfiles=/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME
```
To add a new file, call:
```
dotfiles add <path/to/file>
```