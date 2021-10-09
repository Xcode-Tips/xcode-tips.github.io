⬅️ [Go Back](README.md)

✏️ [Contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/settings.md)

# Settings

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
