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
