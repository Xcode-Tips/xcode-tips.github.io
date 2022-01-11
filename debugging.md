⬅️ [Go Back](README.md)

✏️ [Contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/debugging.md)

# Debugging

### `NSDoubleLocalizedStrings` and Friends

> The `NSDoubleLocalizedStrings` user default is a reasonably well-known and officially documented localization debugging aide. It repeats the text of each localized string, making it double-length so that you can test whether your layout still works.
>
> Another longstanding one is `NSShowNonLocalizedStrings`, which logs to Console when a string can’t be found.
>
> Interface Builder also lets you preview views using an “Accented Pseudolanguage” and a “Bounded String Pseudolanguage.” These correspond to the `NSAccentuateLocalizedStrings` and `NSSurroundLocalizedStrings` user defaults.
>
> Finally, there are `NSForceRightToLeftLocalizedStrings` and `AppleTextDirection` to enable the “Right to Left Pseudolanguage.” This lets you use test right-to-left layout (e.g. for Arabic) using strings from your development language.

Source: [Michael Tsai](https://mjtsai.com/blog/2018/03/27/nsdoublelocalizedstrings-and-friends/)

### Use frame variable in LLDB

> Did you know that most of the time you want to use `v` instead of `po` or `p` in lldb?
>
> This is something that the majority of Swift developers don't realise but `v` is an alias for `frame variable` that was added back in Xcode 10.2, it's a faster and more reliable way to get your info.

Source: [Krzysztof Zabłocki](https://twitter.com/merowing_/status/1392389928844156928)

### Forcing an app out of memory on iOS

> I’ve recently been working on a background uploading feature for an app. One of the key aspects to get right with a feature like that is to correctly handle scenarios where your app is suspended by the system due to RAM constraints or other, similar, reasons. Testing this is easily done by clearing the RAM memory on your device. Unfortunately, this isn’t straightforward. But it’s also not impossible.
>
> [...]
>
> To force-clear your iOS device’s RAM memory, [go through the following steps...](https://www.donnywals.com/forcing-an-app-out-of-memory-on-ios/)

Source: [Donny Wals](https://www.donnywals.com/forcing-an-app-out-of-memory-on-ios/)
