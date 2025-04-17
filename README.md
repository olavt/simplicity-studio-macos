# Install Simplicity Studio 5 on MacBook Pro with Apple Silicon CPU

## Install the Git Large File Storage

Download the Git Large File Storage Installer from https://git-lfs.com

## Install Rosetta 2

There are some executables used in Simplicity Studio 5 that is not built for Apple silicon. One example is the ZAP editor.

```
softwareupdate --install-rosetta
```

## Install Simplicity Studio 5

Download the Simplicity Studio Installer from the Silicon Labs web site. Select the "Mac (ARM) Installer".

## Backup info.plist

There could be some cases where an update to Simplicity Studio 5 components could modify Info.plist, which will change the digital signature and cause a problem launching Simplicity Studio 5 on MacOS. To avoid this, keep a backup of Info.plist and restore it in case it's modified.

### Backup command

```
cp /Applications/Simplicity\ Studio.app/Contents/Info.plist .
```

### Restore command

```
cp Info.plist /Applications/Simplicity\ Studio.app/Contents/.
```