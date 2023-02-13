# Swift_opaque_type

```swift
import Foundation
import SwiftUI


func someInt() -> Int {
    return Int.random(in: 0...10)
}

func someString() -> String {
    return "hello world"
}

func someIntEqutable() -> some Equatable {
    return Int.random(in: 0...10)
}

func someStringEqutable() -> some Equatable {
    return "Hello World"
}

protocol Anything {
    
    associatedtype VALUE
    
    var something: VALUE { get }
    
}


struct Something: Anything {
    
    var something: String = ""
}

struct AnotherThing: Anything {
    
    var something: Int = 3
    
}

func getAnything() -> some Anything {
    return Something()
}

func getAnything2() -> some Anything {
    return AnotherThing()
}

print(getAnything())
print(getAnything2())

```
