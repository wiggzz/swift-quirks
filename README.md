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
