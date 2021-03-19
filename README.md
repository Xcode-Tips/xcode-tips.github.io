*Have a cool tip? Send us [a pull request](https://github.com/Xcode-Tips/xcode-tips.github.io)!*

# Contents

- [Breakpoints](#breakpoints) 
- [Code](#code)
- [Crashes](#crashes)
- [Search](#search)
- [Settings](#settings)
- [Shortcuts](#shortcuts)
- [Simulator](#simulator)
- [Testing](#testing)
- [Usability](#usability)
- [User Defaults](#user-defaults)
- [Xcode-select](#xcode-select)

# [Breakpoints](#breakpoints)

### Use breakpoints as "bookmarks"

> Any time I am exploring or getting familiar with a new codebase in Xcode, especially very large projects, I use disabled breakpoints as “bookmarks” to keep track of where I am, where I have been, and things I want to remember or need to revisit. Sometimes I even do this when debugging issues in codebases that I know well.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/01/21/xcode-tip-breakpoints-as-bookmarks/)

### Quickly toggling breakpoints

Use `Cmd+\` to toggle a breakpoint on the current line.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Code](#code)

### Generating class initializers

Xcode can generate class initializers. Select your class name, then go to the Editor menu and choose Refactor > Generate Memberwise Initializer.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Selecting blocks of code

You can double click a brace to select the entire block of code it contains.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Apply all fix-its

Go to the Editor menu and choose Fix All Issues to apply fix-its all at once.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Crashes](#crashes)

### Viewing .crash files

In Xcode’s Organizer, in the Crashes section, you can right-click or ctrl-click on any row and choose Show in Finder. This will reveal a .crashpoint file — do a Show Package Contents and then dig in further. You will find .crash files with the full crash logs, which provide a lot more info than what you see in Organizer.

Source: [Brent Simmons](https://inessential.com/2021/03/16/the_hottest_of_all_xcode_tips)

# [Interface Builder](#interface-builder)

- [Xcode Interface Builder Tips](https://useyourloaf.com/blog/xcode-interface-builder-tips/), Keith Harrison
- [More Interface Builder Tips And Tricks](https://useyourloaf.com/blog/more-interface-builder-tips-and-tricks/), Keith Harrison

# [Search](#search)

### Deleting search results

When you search using Xcode’s find navigator, you can click on individual results and tap Backspace to remove them.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Settings](#settings)

### Improving the assistant editor

1. Set “Uses Focused Editor” in the Navigation preferences
1. `cmd-J` to switch between panes or open new ones
1. `cmd-shift-O` to open files in the currently focused pane

Source: [Jesse Squires](https://www.jessesquires.com/blog/2018/06/12/xcode-tip-improving-assistant-editor/)

### Using behaviors to improve debugging

> In Xcode’s preferences, go to the Behaviors tab. Navigate to the ‘Running’ section and click ‘Pauses’. Here you can instruct Xcode to open a new tab by checking the box for ‘Show tab named’ and giving it a name. By default, showing the ‘Debug Navigator’ should be enabled. Next, I like to show the debugger with the ‘Variables & Console View’, as well as hide the Utilities sidebar on the right.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2018/07/01/xcode-tip-debugging-behavior-new-tab/)

# [Shortcuts](#shortcuts)

### Jump to a specific line

Open the file you want. Press `Cmd+L`, type a line number and Xcode will jump directly to that line.

### Reindenting/Formatting code

Press `Ctrl+I` to apply Xcode's indentation and formatting.

### Adding comments quickly

Use `Cmd+/` to toggle comments for the current line or selection. Use `Option+Cmd+/`, pressed directly before a method to have Xcode generate a documentation comment.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

###  Remapping unhelpful keys

Some great shortcuts (e.g. `Shift+Cmd+O` for Open Quickly) are next to useless shortcuts (`Shift+Cmd+P`, for the never times you want to print code.) It takes only seconds to remove unhelpful keys, and you can even remap things like `Cmd+P` to resuming SwiftUI's preview.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Simulator](#simulator)

### Tiling the simulator

If you frequently move from Xcode to the simulator, tile them side by side. With the simulator active, go to the Window menu and choose Tile Window To Right Of Screen, then select Xcode on the left. You can adjust the split so the simulator sits snugly on the right.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Status bars

Clean up and configure Simulator status bars using `simctl status_bar`, automate using [Nine41](https://github.com/jessesquires/Nine41).

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/04/13/fully-automating-perfect-status-bar-overrides-for-ios-simulators/)

# [Testing](#testing)

### Re-run your last test

Use `Ctrl+Opt+Cmd+G` to re-run your last test. [Jon Reid](https://twitter.com/qcoding) has a name for this making it easier to remember: “smash go!”

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Randomizing test order

Go to the Product menu, hold down Option, then click Test. Inside the Info tab, click Options then check Randomize Execution Order to run tests in a different order every time.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Improving UI test reliability

You can disable or speed-up animations, and increase timeouts for `waitForExistence()`.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2021/03/17/xcode-ui-testing-reliability-tips/)

### Testing in-app purchases

Make a new StoreKit Config File, and add your IAP. Now go to the Product menu, hold down Option, and click Run. From the Options tab of the window, change StoreKit Config, and now you'll use the test IAP.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [Usability](#usability)

### Expanding autocomplete

You can grab the edge of the autocomplete popup and drag it as wide as you want!

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Generating an interface file

Press `Ctrl+Cmd+Up` to display a generated interface, showing properties, function signatures, and comments for a type. Press it again, to jump to tests for that file if they exist.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# [User Defaults](#user-defaults)

### Make Xcode's Assistant aware of your ViewModels, Views, etc:

```bash
defaults write com.apple.dt.Xcode IDEAdditionalCounterpartSuffixes -array-add "ViewModel" "View" "Screen"
```

You can check the current value of this default using `defaults read com.apple.dt.Xcode IDEAdditionalCounterpartSuffixes`.

Source: [Peter Friese](https://twitter.com/peterfriese/status/1364544309878534144)

# [Xcode-select](#xcode-select)

### Quickly switching between Xcodes

> Using plain xcode-select is slow because you have to provide the path to the Xcode you want to select each time. I wrote a custom shell command to switch between Xcodes more quickly.
 
Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/07/07/quickly-switching-between-xcodes/)
