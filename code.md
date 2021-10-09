⬅️ [Go Back](README.md)

# Code

### Generating class initializers

Xcode can generate class initializers. Select your class name, then go to the Editor menu and choose Refactor > Generate Memberwise Initializer.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Selecting blocks of code

You can double click a brace to select the entire block of code it contains.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Apply all fix-its

Go to the Editor menu and choose Fix All Issues (**&#8963;&#8997;&#8984; F**) to apply fix-its all at once.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

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
