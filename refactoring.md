⬅️ [Go Back](README.md)

# Refactoring

### Faster Xcode Rename Refactoring

If you use the rename refactoring in Xcode a lot, you can save some time by skipping the code folding animation:

```bash
defaults write com.apple.dt.Xcode CodeFoldingAnimationSpeed -int 0
```

Source: [Daniel Martín](https://twitter.com/dmartincy/status/1173289543124029440) (via [Michael Tsai](https://mjtsai.com/blog/2019/09/16/faster-xcode-rename-refactoring/))

### Create compile time reminders in Xcode

> Workarounds are a fact of life for programmers. You rarely have the ability to fix all the buggy code you have to work with, and even if you do, it might not be worth the time and effort to find and validate a proper fix. But while a workaround allows you to move forward quickly, it also creates a maintenance burden. Creative solutions like this are usually more fragile and will need to be revisited occasionally. Here are a few ways you can use the compiler to help remind you.

```swift
@available(swift, deprecated: 5.5, message: "Verify if workarounds are still needed")
func foo() {}

@available(iOS, deprecated: 14.0, message: "Verify if workarounds are still needed")
func foo() {}

func foo() {
    #if swift(>=5.5)
    #warning("Verify if workarounds are still needed")
    #endif    
}
```

Source: [Robin Kunde](https://recoursive.com/2021/09/14/create_compile_time_reminders/)

