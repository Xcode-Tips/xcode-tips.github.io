# Xcode Tips 💡

The more you know... 😎

## User Defaults

#### Make Xcode's Assistant aware of your ViewModels, Views, etc:

```bash
defaults write com.apple.dt.Xcode IDEAdditionalCounterpartSuffixes -array-add "ViewModel" "View" "Screen"
```

Credit: [Peter Friese](https://twitter.com/peterfriese/status/1364544309878534144)
