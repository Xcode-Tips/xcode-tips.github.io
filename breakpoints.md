⬅️ [Go Back](README.md)

✏️ [Contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/breakpoints.md)

# Breakpoints

### Use breakpoints as "bookmarks"

> Any time I am exploring or getting familiar with a new codebase in Xcode, especially very large projects, I use disabled breakpoints as “bookmarks” to keep track of where I am, where I have been, and things I want to remember or need to revisit. Sometimes I even do this when debugging issues in codebases that I know well.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/01/21/xcode-tip-breakpoints-as-bookmarks/)

### Quickly toggling breakpoints

Use **&#8984; \\** to toggle a breakpoint on the current line.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Play sound files in breakpoints

> Audible Xcode breakpoints allow a sound effect to be played while continuing the executable without interruptions. This can be a really useful debugging tool. Custom Xcode breakpoint sound files can be found on GitHub at [Xcode Breakpoint Sounds](https://github.com/matthewreagan/Xcode-Breakpoint-Sounds).

Source: [Matt Reagan](http://mattreagandev.com/?article=20170306)

### Automate user actions with LLDB expressions

When developing a view that requires app navigation to reach, you can use breakpoints to speed up iterations by simulating user actions, instead of modifying or hacking code that you might forget to remove later. Using breakpoints this way instead of adding temporary debug or development code eliminates the possibility of shipping that code by accident.

For example, on a login screen, you can set a breakpoint on `viewDidLoad()`, or `view{Will|Did}Appear()`, then edit the breakpoint to add a Debugger Command action to invoke other methods in the view controller, like a `loginSuccess()` method. Then, set the breakpoint to automatically continue after evaluating the actions. This essentially bypasses login, but only when running the app through Xcode, and only when that breakpoint is enabled.

Another use case: you can pre-populate text fields, make text fields first responders, and change mutable variables at runtime. Once set, enable or disable these breakpoints to simulate different user interaction flows.

Example debugger commands: `expr loginSuccess()`, `expr nameTextField?.text = "Erwin Maza"`, etc.

Source: [Erwin Mazariegos](https://github.com/erwinmaza)

### Disabling Exception Breakpoint When Running Unit Tests

> The problem is that I usually have Xcode’s built-in “All Exceptions” breakpoint enabled when debugging my application, but when I run unit tests in Xcode, I have certain unit tests that will throw exceptions and trigger the breakpoint, halting the test until I tell it to continue.
>
```swift
func BWIsUnitTesting() -> Bool {
  return NSProcessInfo.processInfo().environment["XCTestConfigurationFilePath"] != nil
}
```
> Then, open up the breakpoints navigator in Xcode, right-click on the exceptions breakpoint, and add !BWIsUnitTesting() to the “Condition” field...

Source: [Brian Webster](https://brian-webster.tumblr.com/post/632528822118629376/disabling-exception-breakpoint-when-running-unit), [Michael Tsai
](https://mjtsai.com/blog/2021/12/29/disabling-exception-breakpoint-when-running-unit-tests/)
