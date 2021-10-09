⬅️ [Go Back](README.md)

✏️ [Contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/simulator.md)

# Simulator

### Tiling the simulator

If you frequently move from Xcode to the simulator, tile them side by side. With the simulator active, go to the Window menu and choose Tile Window To Right Of Screen, then select Xcode on the left. You can adjust the split so the simulator sits snugly on the right.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/229/24-quick-xcode-tips)

### Status bars

Clean up and configure Simulator status bars using `simctl status_bar`, automate using [Nine41](https://github.com/jessesquires/Nine41).

Source: [Jesse Squires](https://www.jessesquires.com/blog/2020/04/13/fully-automating-perfect-status-bar-overrides-for-ios-simulators/)

### Device mask in screenshots

Since Xcode 12 you can configure the simulator to apply a device mask to screenshots.

> Go into simulator's `File` menu, press **&#8997;**, "Save Screen..." and there tick "Apply device mask to screenshot". Now your sim will save screenshots with a transparent notch and corners!

You can also enable it within Simulator preferences.

Source: [Roman Shevtsov and Jean-Étienne](https://twitter.com/ryushev/status/1386626956351901704)

### Save Simulator recordings as GIFs

> You can go to Xcode Simulator `File > Record Screen` to record the simulator, and turn it into a GIF (if you want to) by right clicking on the clip, and `Save as Animated GIF`.

Source: [Ting Becker](https://twitter.com/teekachu1/status/1431314346311815175?s=21)
