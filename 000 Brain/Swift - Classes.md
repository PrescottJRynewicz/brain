---
Created On: 2024-01-14, 11:12
Unique ID: 202401141112
---
**Status:** #moc 

**Tags:** #SwiftCards 

# Swift - Classes


#### In Swift, What is the difference in instantiation between Classes and Structs, specifically for their members?
?
Structs come with a default property member-wise initializer, classes you don't. If you have properties in a class, you must always create your own initializer. 
<!--SR:!2024-03-04,1,210-->

#### How do you Inherit a class in Swift?
?
Just add a `: ParentClass` to the inherited classes definition.
```swift
class Dog {
    var name: String
    var breed: String

    init(name: String, breed: String) {
        self.name = name
        self.breed = breed
    }
}
```
```swift
class Poodle: Dog {
    init(name: String) {
        super.init(name: name, breed: "Poodle")
    }
}
```
<!--SR:!2024-03-04,19,270-->

#### How do you override class methods in Swift?
?
Simply define the method in the child class, the only difference is that you must ass the `override` keyword. 
```swift
class Poodle: Dog {
    override func makeNoise() {
        print("Yip!")
    }
}
```
<!--SR:!2024-05-01,59,250-->


#### In Swift Classes, what is the `final` keyword?
?
The `final` keyword means that the class cannot be inherited. 
```swift
final class Dog {
    var name: String
    var breed: String

    init(name: String, breed: String) {
        self.name = name
        self.breed = breed
    }
}
```
<!--SR:!2024-05-03,61,270-->

#### In swift, what is the difference between copying classes and structs?
?
When you copy a struct, the data is duplicated, and creates a new reference.
When you copy a class, it is referenced, so mutating the class will update both variables pointing to the class. 
<!--SR:!2024-04-01,29,230-->

#### What are de-initializers in Swift Classes?
?
The `deinit` method is run when the class gets destroyed (i.e. it goes out of scope and can no longer be referenced by the program)
<!--SR:!2024-03-31,28,230-->

#### In Swift, the mutating keyword applies to Structs; does it also apply to Classes?
?
No - you can instantiate a class as a constant and change it's properties. This is valid code.
```swift
class Singer {
    var name = "Taylor Swift"
}

let taylor = Singer()
taylor.name = "Ed Sheeran"
print(taylor.name)
```
To avoid changing a property within a class, define the property as constant.
```swift
class Singer {
    let name = "Taylor Swift"
}
```
<!--SR:!2024-04-02,30,230-->