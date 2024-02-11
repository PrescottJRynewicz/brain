---
Created On: 2024-01-13, 09:49
Unique ID: 202401130949
---
**Status:** #moc 

**Tags:** #SwiftCards 

# Swift - Structs

#### What is a computed property on a struct?
?
It's value comes from a closure and can use other properties of the struct to get it's value.
<!--SR:!2024-02-12,3,250-->

#### What Are Property Observers for Structs?
?
`willSet` and `didSet`
These are hooks that get called before of after a property is set.
<!--SR:!2024-02-12,2,230-->

#### If A struct has a variable property, but the instance of the struct was defined as a constant, can the variable property be changed?
?
No. It cannot.
<!--SR:!2024-02-12,3,250-->

#### What is a mutating struct method?
?
Because swift does not know how a struct will be instantiated, you have to specify if a method is going to change any of the structs properties ahead of time. 
<!--SR:!2024-02-12,3,250-->


#### In Structs, what is the constructor method keyword?
?
`init`
<!--SR:!2024-02-12,3,250-->

#### What is a lazy property in Swift?
?
It is a property that is not initialized until it is first accessed.
```swift
struct Person {
    var name: String
    lazy var familyTree = FamilyTree()

    init(name: String) {
        self.name = name
    }
}
```
<!--SR:!2024-02-12,2,230-->


#### Can Static properties on Structs be mutated?
?
Yes, they can.
```swift
struct Student {
    static var classSize = 0
    var name: String

    init(name: String) {
        self.name = name
        Student.classSize += 1
    }
}
```
<!--SR:!2024-02-12,2,230-->