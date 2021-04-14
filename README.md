*A community-run website for documenting Xcode Tips*

**Have a cool tip to share?** Send [a pull request](https://github.com/Xcode-Tips/xcode-tips.github.io/pulls) or [open an issue](https://github.com/Xcode-Tips/xcode-tips.github.io/issues)!

# About

Folks in the Apple developer community are always sharing great Xcode tips &mdash; usually via Twitter or blog posts. Wouldn't it be nice if we collected them all in a single place to share? The goal of this project is to host all of these Xcode tips in a single place, and make it [easy for anyone to contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/.github/CONTRIBUTING.md).

# Contents

- [Breakpoints](#breakpoints)
- [Build Times](#build-times)
- [Code](#code)
- [Crashes](#crashes)
- [Debugging](#debugging)
- [Interface Builder](#interface-builder)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [Refactoring](#refactoring)
- [Search](#search)
- [Settings](#settings)
- [Simulator](#simulator)
- [Testing](#testing)
- [Usability](#usability)
- [User Defaults](#user-defaults)
- [Xcode Versions](#xcode-versions)

> 💡 **Tip:** we recommend following the "source" links for each tip to learn even more.

# [Breakpoints](#breakpoints)

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

# [Build Times](#build-times)

### Fix slow codesigning

> Poking around, I came across this [thread](https://developer.apple.com/forums/thread/66418). While I didn’t have the main problem described there of duplicate certificates, buried in that thread was the following advice: trim `~/Library/Preferences/com.apple.security.plist`
>
> Opening that file up revealed that I had several entries, all except one pointing to non-existent files with the one valid entry pointing to my login keychain. After removing the invalid entries, code signing only took up to 1 second, max. This shaved 40-60 seconds off of my full release builds and 10 seconds off of incremental ones. Huge savings.

Source: [Paul Kim](https://www.noodlesoft.com/blog/2020/08/24/a-couple-of-random-xcode-tips-to-speed-up-your-builds/)

### Copying framework headers

> Another thing I noticed in the cleanup was that some of my frameworks were being copied without their headers.
> [...]
> Apparently, there’s a hidden setting in your `project.pbxproj` file for copying frameworks where you can specify whether headers get copied over.

The only way to enable/disable this is to edit the `project.pbxproj` by hand. The flag in question is `RemoveHeadersOnCopy`.

Source: [Paul Kim](https://www.noodlesoft.com/blog/2020/08/24/a-couple-of-random-xcode-tips-to-speed-up-your-builds/)

# [Code](#code)

### Generating class initializers

Xcode can generate class initializers. Select your class name, then go to the Editor menu and choose Refactor > Generate Memberwise Initializer.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Selecting blocks of code

You can double click a brace to select the entire block of code it contains.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Apply all fix-its

Go to the Editor menu and choose Fix All Issues (**&#8963;&#8997;&#8984; F**) to apply fix-its all at once.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Crashes](#crashes)

### Viewing .crash files

In Xcode’s Organizer, in the Crashes section, you can right-click or ctrl-click on any row and choose Show in Finder. This will reveal a `.crashpoint` file — do a "Show Package Contents" and then dig in further. You will find `.crash` files with the full crash logs, which provide a lot more info than what you see in Organizer.

Source: [Brent Simmons](https://inessential.com/2021/03/16/the_hottest_of_all_xcode_tips)

# [Debugging](#debugging)

### `NSDoubleLocalizedStrings` and Friends

> The `NSDoubleLocalizedStrings` user default is a reasonably well-known and officially documented localization debugging aide. It repeats the text of each localized string, making it double-length so that you can test whether your layout still works.
>
> Another longstanding one is `NSShowNonLocalizedStrings`, which logs to Console when a string can’t be found.
>
> Interface Builder also lets you preview views using an “Accented Pseudolanguage” and a “Bounded String Pseudolanguage.” These correspond to the `NSAccentuateLocalizedStrings` and `NSSurroundLocalizedStrings` user defaults.
>
> Finally, there are `NSForceRightToLeftLocalizedStrings` and `AppleTextDirection` to enable the “Right to Left Pseudolanguage.” This lets you use test right-to-left layout (e.g. for Arabic) using strings from your development language.

Source: [Michael Tsai](https://mjtsai.com/blog/2018/03/27/nsdoublelocalizedstrings-and-friends/)

# [Interface Builder](#interface-builder)

- [Xcode Interface Builder Tips](https://useyourloaf.com/blog/xcode-interface-builder-tips/), Keith Harrison
- [More Interface Builder Tips And Tricks](https://useyourloaf.com/blog/more-interface-builder-tips-and-tricks/), Keith Harrison

# [Keyboard Shortcuts](#keyboard-shortcuts)

### Jump to a specific line

Open the file you want. Press **&#8984;L**, type a line number and Xcode will jump directly to that line.

### Reindenting/Formatting code

Press **&#8963;I** to apply Xcode's indentation and formatting.

### Adding comments quickly

Use **&#8984;/** to toggle comments for the current line or selection. Use **&#8997;&#8984;/**, pressed directly before a method to have Xcode generate a documentation comment.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Jump to file in source navigator

Press **&#8984;&#8679;J** to quickly jump to the current open file in the navigator to easily see and select related files.

Source: [Jeroen Leenarts](https://leenarts.net/2020/02/18/frequently-used-keyboard-shortcuts-i-use-inwith-xcode/)

### Open the jump bar

Press **&#8963;6** to open the symbol jump bar in Xcode. Now start typing. Try it, jumping to a function in the current file, never has been so easy.

Source: [Jeroen Leenarts](https://leenarts.net/2020/02/18/frequently-used-keyboard-shortcuts-i-use-inwith-xcode/)

### Remapping unhelpful keys

Some great shortcuts (e.g. **&#8679;&#8984;O** for Open Quickly) are next to useless shortcuts (**&#8679;&#8984;P**, for the never times you want to print code.) It takes only seconds to remove unhelpful keys, and you can even remap things like **&#8984;P** to resuming SwiftUI's preview.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Increase or decrease editor font size

Press **&#8984;+** to increase and **&#8984;-** to decrease.

### Move cursor to the top or bottom of the file

Press **&#8984;&#8593;** to move to the top of the file. Press **&#8984;&#8595;** to move to the bottom of the file.

### Show and hide debug area

Press **&#8984;&#8679;Y** to open and close the debug area.

### Generating an interface file

Press **&#8963;&#8984;&#8679;** to display a generated interface, showing properties, function signatures, and comments for a type. Press it again, to jump to tests for that file if they exist.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Trigger Custom Behaviors

If you find yourself wasting time continually opening and closing the `Navigator`, `Inspectors`, or the `Preview` when you switch the type of file you're working on, you can define custom `Behaviors` and assign keyboard shortcuts to them.

Xcode Behaviors set the state of the Xcode interface when events occur such as a build starting. Custom Behaviors allow you to define your own triggers.

* Go to `Xcode -> Preferences`
* Open the `Behaviors` tab
* Click `+` at the bottom of the list and name the new Behavior (E.g. `IB File`, `Code File`, `SwiftUI File`)
* On the right side, set the state of the `Navigator`, `Inspectors`, `Preview` or other elements
* Assign a keyboard shortcut next to each name

Now you can quickly set the state of your panels to focus on the type of work you're doing.

Source: [Erwin Mazariegos](https://github.com/erwinmaza)

### Open Human Interface Guidelines

Press **&#8984;&#8679;H** to open the Human Interface Guidelines in your web browser.

# [Refactoring](#refactoring)

### Faster Xcode Rename Refactoring

If you use the rename refactoring in Xcode a lot, you can save some time by skipping the code folding animation:

```bash
defaults write com.apple.dt.Xcode CodeFoldingAnimationSpeed -int 0
```

Source: [Daniel Martín](https://twitter.com/dmartincy/status/1173289543124029440) (via [Michael Tsai](https://mjtsai.com/blog/2019/09/16/faster-xcode-rename-refactoring/))

# [Search](#search)

### Deleting search results

When you search using Xcode’s find navigator, you can click on individual results and tap Backspace to remove them.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Settings](#settings)

### Customizing the file header comment and other text macros

Xcode allows you to customize the file header and other so-called text macros using a plist file.

1. Create a property list file named `IDETemplateMacros.plist`.
2. For every text macro you want to customize, add a new key to the plist’s dictionary.
3. Copy the file to one of the following locations.
    1. `<Name>.xcodeproj/xcshareddata/`
    2. `<Name>.xcworkspace/xcshareddata/`
    3. ...

Source: [Ole Begemann](https://oleb.net/blog/2017/07/xcode-9-text-macros/)

### Improving the assistant editor

1. Set “Uses Focused Editor” in the Navigation preferences
1. **&#8984;J** to switch between panes or open new ones
1. **&#8984;&#8679;O** to open files in the currently focused pane

Source: [Jesse Squires](https://www.jessesquires.com/blog/2018/06/12/xcode-tip-improving-assistant-editor/)

### Navigation using the assistant editor

The assistant editor is very useful for navigating around while remaining at your original position:

- Use **&#8984;&#8997;,** to open the current location in the neighbouring editor
- Hold **&#8984;&#8963;&#8997;** and click on any method to jump to that method in the neighbouring editor (**&#8984;&#8963;** opens in the current editor)
- **&#8984;&#8963;&#8593;** to switch between associated files, and **&#8984;&#8963;&#8997;&#8593;** to do so using the neighbouring editor
- **&#8984;&#8963;&#8592;** and **&#8984;&#8963;&#8594;** to move back and forward through navigation history, add **&#8997;** for their neighbouring editor counterparts

### Spelling and Grammar

> You can turn on spell checking in Xcode. Go to `Edit > Format > Spelling and Grammar`. This works on comments and identifiers, and is aware of capitalization conventions.

Source: [Micheal Gorbach](https://twitter.com/mgorbach/status/1314662158819627010)

### Using behaviors to improve debugging

> In Xcode’s preferences, go to the Behaviors tab. Navigate to the ‘Running’ section and click ‘Pauses’. Here you can instruct Xcode to open a new tab by checking the box for ‘Show tab named’ and giving it a name. By default, showing the ‘Debug Navigator’ should be enabled. Next, I like to show the debugger with the ‘Variables & Console View’, as well as hide the Utilities sidebar on the right.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2018/07/01/xcode-tip-debugging-behavior-new-tab/)

# [Simulator](#simulator)

### Tiling the simulator

If you frequently move from Xcode to the simulator, tile them side by side. With the simulator active, go to the Window menu and choose Tile Window To Right Of Screen, then select Xcode on the left. You can adjust the split so the simulator sits snugly on the right.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Status bars

Clean up and configure Simulator status bars using `simctl status_bar`, automate using [Nine41](https://github.com/jessesquires/Nine41).

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/04/13/fully-automating-perfect-status-bar-overrides-for-ios-simulators/)

# [Testing](#testing)

### Re-run your last test

Use **&#8963;&#8997;&#8984;G** to re-run your last test. [Jon Reid](https://twitter.com/qcoding) has a name for this making it easier to remember: “smash go!”

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Randomizing test order

Go to the Product menu, hold down **&#8997;**, then click Test. Inside the Info tab, click Options then check Randomize Execution Order to run tests in a different order every time.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Improving UI test reliability

You can disable or speed-up animations, and increase timeouts for `waitForExistence()`.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2021/03/17/xcode-ui-testing-reliability-tips/)

### Testing in-app purchases

Make a new StoreKit Config File, and add your IAP. Now go to the Product menu, hold down **&#8997;**, and click Run. From the Options tab of the window, change StoreKit Config, and now you'll use the test IAP.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Usability](#usability)

### Expanding autocomplete

You can grab the edge of the autocomplete popup and drag it as wide as you want!

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Fix Freezing

If your Xcode freezes a lot, unpair all devices (Window/Devices and Simulators).

Source: [Michał Januszewski](https://twitter.com/mjanuszewski/status/1374434141672853508)

# [User Defaults](#user-defaults)

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

# [Xcode Versions](#xcode-versions)

### Quickly switching between Xcodes

> Using plain xcode-select is slow because you have to provide the path to the Xcode you want to select each time. I wrote a custom shell command to switch between Xcodes more quickly.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/07/07/quickly-switching-between-xcodes/)

### Install, manage and switch between different Xcode versions

An easy-to-use command line tool to install and uninstall different Xcode versions on your machine. Xcode versions are installed side-by-side with the version in their name and makes downloading/installing them incredibly easy.

Source: [xcinfo](https://github.com/xcodereleases/xcinfo)
