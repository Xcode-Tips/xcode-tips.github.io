Have a cool tip? Send us [a pull request](https://github.com/Xcode-Tips/xcode-tips.github.io)!

# Breakpoints

Use breakpoints as "bookmarks".

> Any time I am exploring or getting familiar with a new codebase in Xcode, especially very large projects, I use disabled breakpoints as “bookmarks” to keep track of where I am, where I have been, and things I want to remember or need to revisit. Sometimes I even do this when debugging issues in codebases that I know well.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/01/21/xcode-tip-breakpoints-as-bookmarks/)

# Code

#### Generating class initializers

Xcode can generate class initializers. Select your class name, then go to the Editor menu and choose Refactor > Generate Memberwise Initializer.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

#### Selecting blocks of code

You can double click a brace to select the entire block of code it contains.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

#### Apply all fix-its

Go to the Editor menu and choose Fix All Issues to apply fix-its all at once.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

# Crashes

#### Viewing .crash files

In Xcode’s Organizer, in the Crashes section, you can right-click or ctrl-click on any row and choose Show in Finder. This will reveal a .crashpoint file — do a Show Package Contents and then dig in further. You will find .crash files with the full crash logs, which provide a lot more info than what you see in Organizer.

Source: [Brent Simmons](https://inessential.com/2021/03/16/the_hottest_of_all_xcode_tips)

# Settings

#### Improving the assistant editor

1. Set “Uses Focused Editor” in the Navigation preferences
1. `cmd-J` to switch between panes or open new ones
1. `cmd-shift-O` to open files in the currently focused pane

Source: [Jesse Squires](https://www.jessesquires.com/blog/2018/06/12/xcode-tip-improving-assistant-editor/)

#### Using behaviors to improve debugging

> In Xcode’s preferences, go to the Behaviors tab. Navigate to the ‘Running’ section and click ‘Pauses’. Here you can instruct Xcode to open a new tab by checking the box for ‘Show tab named’ and giving it a name. By default, showing the ‘Debug Navigator’ should be enabled. Next, I like to show the debugger with the ‘Variables & Console View’, as well as hide the Utilities sidebar on the right.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2018/07/01/xcode-tip-debugging-behavior-new-tab/)

# Simulator

#### Status bars

Clean up and configure Simulator status bars using `simctl status_bar`, automate using [Nine41](https://github.com/jessesquires/Nine41).

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/04/13/fully-automating-perfect-status-bar-overrides-for-ios-simulators/)

# Testing

#### Improving UI test reliability

You can disable or speed-up animations, and increase timeouts for `waitForExistence()`.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2021/03/17/xcode-ui-testing-reliability-tips/)

# User Defaults

#### Make Xcode's Assistant aware of your ViewModels, Views, etc:

```bash
defaults write com.apple.dt.Xcode IDEAdditionalCounterpartSuffixes -array-add "ViewModel" "View" "Screen"
```

Source: [Peter Friese](https://twitter.com/peterfriese/status/1364544309878534144)

# Xcode-select

#### Quickly switching between Xcodes

> Using plain xcode-select is slow because you have to provide the path to the Xcode you want to select each time. I wrote a custom shell command to switch between Xcodes more quickly.
 
Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/07/07/quickly-switching-between-xcodes/)
