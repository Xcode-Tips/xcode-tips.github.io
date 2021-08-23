[Return to root](README.md)

# Keyboard Shortcuts

### Cheatsheet

A handy list of Xcode keyboard shortcuts.

Source: [Keith Harrison](https://useyourloaf.com/blog/xcode-keyboard-shortcuts/)

### Jump to a specific line

Open the file you want. Press **&#8984;L**, type a line number and Xcode will jump directly to that line.

### Re-indenting/Formatting code

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

### Show/hide the preview canvas

It takes up a lot of space, you can quickly toggle it.

> **&#8984; &#8963; &#8629;**
> `Editor menu > Canvas`

Source: [Sarun Wongpatcharapakorn](https://sarunw.com/posts/xcode-shortcuts-for-swiftui/)

### Refresh Preview Canvas

If you type too fast Xcode can stop updating the preview, so you may have to trigger a refresh.

> **&#8984; &#8997; P**
> `Editor menu > Canvas > Refresh Canvas`

This will refresh your preview and start automatically updating again.

Source: [Sarun Wongpatcharapakorn](https://sarunw.com/posts/xcode-shortcuts-for-swiftui/)

### Move line of code up or down

You can use a keyboard shortcut to move a line of code up or down, which can be useful for re-ordering things. This can be the current line or you can select multiple lines to move together.

To move line of code up:

> **&#8984; &#8997; \[**
> `Editor menu > Structure > Move Line Up`

To move line of code down:

> **&#8984; &#8997; \]**
> `Editor menu > Structure > Move Line Down`

Source: [Sarun Wongpatcharapakorn](https://sarunw.com/posts/xcode-shortcuts-for-swiftui/)