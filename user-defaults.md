[Return to root](README.md)

# User Defaults

### Make Xcode's Assistant aware of your ViewModels, Views, etc

```bash
defaults write com.apple.dt.Xcode IDEAdditionalCounterpartSuffixes -array-add "ViewModel" "View" "Screen"
```

You can check the current value of this default using `defaults read com.apple.dt.Xcode IDEAdditionalCounterpartSuffixes`.

Source: [Peter Friese](https://twitter.com/peterfriese/status/1364544309878534144)

### Prevent restoring the last open project

This is useful if you have a project that crashes Xcode on launch, if you want to run multiple Xcode versions for different projects, or if you always want to choose the project to open.

```bash
defaults write com.apple.dt.Xcode ApplePersistenceIgnoreState -bool YES
```

Source: [Txai Wieser](https://txaiwieser.github.io/articles/2021-03-08-xcode-defaults)

### Show project build times in the activity viewer

This shows the build time duration directly in the activity viewer every time you build.

```bash
defaults write com.apple.dt.Xcode ShowBuildOperationDuration -bool YES
```

Source: [Txai Wieser](https://txaiwieser.github.io/articles/2021-03-08-xcode-defaults)

### Enable Internal Debug Menu

Xcode has a secret internal debug menu. To enable it:

```bash
defaults write com.apple.dt.Xcode ShowDVTDebugMenu -bool YES
sudo touch /Applications/Xcode.app/Contents/Developer/AppleInternal/Library/Xcode/AppleInternal.plist
```

You can also [enable a similar menu for the iOS simulator](https://medium.com/flawless-app-stories/simulator-on-steroids-c12774ca6b).

⚠️ **Use with caution.** ⚠️

Source: [Khoa, @onmyway133](https://twitter.com/onmyway133/status/1380084248829251586)