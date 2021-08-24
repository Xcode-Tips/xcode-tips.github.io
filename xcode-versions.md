[Return to root](README.md)

# Xcode Versions

### Quickly switching between Xcodes

> Using plain xcode-select is slow because you have to provide the path to the Xcode you want to select each time. I wrote a custom shell command to switch between Xcodes more quickly.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/07/07/quickly-switching-between-xcodes/)

### Switch Xcode versions without entering password

> When using `xcode-select` it can be problematic entering the password in situations like on remote CI. We can configure sudo using `sudoers` so that the password will no longer be required using this command:

```bash
echo "%admin ALL=NOPASSWD: /usr/bin/xcode-select,/usr/bin/xcodebuild -runFirstLaunch" | sudo tee /etc/sudoers.d/xcode
```

Source: [Keith Smiley](https://www.smileykeith.com/2021/08/12/xcode-select-sudoers/)

### Install, manage and switch between different Xcode versions

An easy-to-use command line tool to install and uninstall different Xcode versions on your machine. Xcode versions are installed side-by-side with the version in their name and makes downloading/installing them incredibly easy.

Source: [xcinfo](https://github.com/xcodereleases/xcinfo)