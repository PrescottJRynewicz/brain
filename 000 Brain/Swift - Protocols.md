---
Created On: 2024-01-14, 11:31
Unique ID: 202401141131
---
**Status:** #moc 

**Tags:** 

# Swift - Protocols


#### What is a Swift Protocol?
?
To use typescript language, it is an `interface` - a definition that can be applied to a struct or a class that the item must adhere to.

#### In Swift, what are extensions?
?
Extensions allow you to add methods to existing classes, structs, or protocols.
For example, you can extend a class, or you could extend a protocol that applies to many classes.
Unlike protocols, extensions define their code in the extension.
```swift
extension Int {
    func squared() -> Int {
        return self * self
    }
}
```


#### What is the difference between Inheriting and Composing when designing object or protocol-oriented software?
?
Inheriting defines a lineage - all members of the lineage must adhere to the parent's guidelines. Similar to the parenting of biological children, this made sense in the mid-1900s. You believe and do what your parents do. If your parents were farmers, you were also a farmer, but now, maybe you had an upgraded type of plow to become a slightly better farmer.  
Composition is the ability to define more flexible individuals without needing to adhere to an existing lineage. This is much more akin to parenting in the 21st century. Every person is encouraged to find out who they are as an individual by deducing the composition of their personal traits. You could compose some traits from your parents, but you are not required to. 