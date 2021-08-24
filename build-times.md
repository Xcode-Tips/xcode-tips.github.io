[Return to root](README.md)

# Build times

### Measuring build times for type checking

You can use the Swift compiler flags `-warn-long-function-bodies` and `-warn-long-expression-type-checking` to emit warnings for functions or expressions that take longer than a set time to type check. Surfacing these within your projects can help improve and manage type checking times which contribute to overall build times.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2017/09/18/measuring-compile-times-xcode9/)

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