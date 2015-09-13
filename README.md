# dotsetup
A shell script to clone and symlink dotfiles from a specified git repository

## quick install

```bash
curl -sSL http://git.io/rcndots -o dotsetup && chmod +x dotsetup
```
or
```bash
wget -q http://git.io/rcndots -O dotsetup && chmod +x dotsetup
```

## usage

```
usage: dotsetup [options]

  -a   symlink dotfiles for all installed programs"
  -c   clone git repository"
  -h   print this screen"
  -t   print a list of installed programs"
  -v   install or update vim plugins"
```

## example

### Get the setup script and make it executable
```bash
curl -sSL http://git.io/rcndots -o dotsetup && chmod +x dotsetup
```

### Check for already installed programs
```bash
./dotsetup -t
```

### Install missing programs
Depending on your distribution run f.e.:
```bash
# For Arch Linux based distributions
pacman -Sy git tmux vim zsh

# For Debian based distributions
apt-get update && apt-get install git tmux vim zsh

# For Red Hat based distributions
yum update && yum install git tmux vim zsh
```

### Clone dotfiles repo and try to symlink the config files for each installed program
```bash
./dotsetup -a
```

### Run zsh shell and make default it the default
f.e.:
```bash
exec zsh
sudo chsh -s /bin/zsh [username]
```


## TODO

[ ] add more arrays to dotfiles()
[ ] add a flags to overwrite/backup existing dotfiles
    [ ] add interactive confirmation switch

