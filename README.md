# Dots files I have created for phyp usage.

### Setup

#### Manual Install
Backup your files then do the following:
```
cp ./bash ~/.bash
ln -s ~/.bash/rc ~/.bashrc
ln -s ~/.bash/profile ~/.bash_profile
```

#### Install the base bash env automatic install
The install file has not been fully tested, works on linux environments,
hardlinked .bashrc and other files might mess it up. It should backup configs.
run `install`

### Removal

#### Manual Removal
Everything of importance is in ~/.bash, we can remove it and the symlinks,
restoring is up to you, if installed with the script, there will be a backup
directory in `~/.bash` with any bash files we stashed away on install.
```
rm -r ~/.bash
rm ~/.bashrc
rm ~/.bash_profile
```
#### Automatic Removal
Same as above, be careful, a backup is saved of the installer but not the
uninstaller, we instead restore what was backed up by the installer and delete
everything else the installer would have added.

run `uninstaller`

### Install modules
Add whatever module you want to source into your bashrc into ~/.bash/modules
and rerun bash to pick it up.
`cp ./modules/$modulename ~/.bash/modules/`
