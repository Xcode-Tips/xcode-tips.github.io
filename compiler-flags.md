⬅️ [Go Back](README.md)

✏️ [Contribute](https://github.com/Xcode-Tips/xcode-tips.github.io/blob/main/compiler-flags.md)

# Compiler Flags

### Measuring build times for type checking

You can use the Swift compiler flags `-warn-long-function-bodies` and `-warn-long-expression-type-checking` to emit warnings for functions or expressions that take longer than a set time to type check. Surfacing these within your projects can help improve and manage type checking times which contribute to overall build times.

Source: [Jesse Squires](https://www.jessesquires.com/blog/2017/09/18/measuring-compile-times-xcode9/)

### Swift Concurrency flags

> If you’re writing Swift concurrency code, add these compiler flags:
>
> `-Xfrontend -warn-concurrency -Xfrontend -enable-actor-data-race-checks`
>
> (in Xcode: Other Swift Flags)
>
> Warnings in Swift 5.5 identify unsafe constructs, will become errors in Swift 6.
>
> [Swift Forums: Concurrency in Swift 5 and 6](https://forums.swift.org/t/concurrency-in-swift-5-and-6/49337)

Source: [Ole Begemann](https://mobile.twitter.com/olebegemann/status/1421144304127463427)
