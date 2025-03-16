# More Information
Based on [Best way to manage your dotfiles](https://medium.com/@simontoth/best-way-to-manage-your-dotfiles-2c45bb280049)
# Setup a New Machine
First, create a `git` alias to use with the new repo:
```
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
```
Then clone and checkout
```
git clone --bare git@github.com:BoldMoose/dotfiles.git $HOME/.dotfiles
dotfiles config --local status.showUntrackedFiles no
dotfiles checkout
```
