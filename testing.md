⬅️ [Go Back](README.md)

✏️ [Contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/testing.md)

# Testing

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

### UI testing cheat sheet

Here are some quick code snippets that help you solve a variety of common problems using Xcode’s UI testing system.

Source: [Paul Hudson](https://www.hackingwithswift.com/articles/148/xcode-ui-testing-cheat-sheet)

### How to Speed Up SwiftUI Development and Testing Using PreviewSnapshots

A quick guide on PreviewSnapshots, an open-source preview snapshot tool that can share configurations between Xcode previews and snapshot tests

Source: DoorDash Engineering(https://doordash.engineering/2023/01/18/how-to-speed-up-swiftui-development-and-testing-using-previewsnapshots/)
