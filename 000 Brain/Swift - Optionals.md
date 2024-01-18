---
Created On: 2024-01-14, 19:13
Unique ID: 202401141913
---
**Status:** #moc 

**Tags:** #SwiftCards  

# Swift - Optionals


#### In Swift, what are implicitly unwrapped optionals?
?
Implicitly unwrapped optionals are optional values that you specify upon declaration that you don't need to unwrap them. For example, if you are are okay treating a value as nil, or you definitely know that it will be defined by the time you need to use it. 
In general, it is not recommended, and you should unwrap optionals using the built in unwrapping features. 
```swift
let age: Int! = nil
```

#### What is a failable Initializer?
?
It is a way to specify that a class or struct may fail to initialize, and return nil instead of a defined value.
```swift
struct Person {
    var id: String

    init?(id: String) {
        if id.count == 9 {
            self.id = id
        } else {
            return nil
        }
    }
}
```

