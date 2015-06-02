# swift-quirks
Quirks and interesting facts from learning Swift

### failable initializers
```swift
struct Animal {
    let species: String
    init?(species: String) {
        if species.isEmpty { return nil }
        self.species = species
    }
}
```
### no mocking right now (or reflection)

### no protected access modifier
> When you develop a framework, mark the public-facing interface to that framework as public so that it can be viewed and accessed by other modules, such as an app that imports the framework.

### weird closure errors
If you get weird errors when dealing with closures, it is most likely because of the polymorphic type matching system being used to match the type of the closure to the function being called.  For instance:

```swift
func foo(closure: () -> Int) {
    // do something
}

func foo(closure: () -> Double) {
    // do something
}

foo {
    println("This will not compile")
}

foo {
    println("This will")
    return 1.5
}
```
