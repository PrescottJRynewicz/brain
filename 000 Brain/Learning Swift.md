---
Created On: 2024-01-11, 12:40
Unique ID: 202401111240
---


**Tags:** #SwiftCards

# Intro Concepts

#### How do you define multiline strings in swift?
?
By using `"""` quotes.
If you don't want the whitespace to be preserved, end each line with a \
<!--SR:!2024-04-19,47,270-->


#### How Are Arrays and Tuples different in Swift?
?
1. You cannot add or remove items from Tuples.
2. You can't change the type of items in a tuple
3. You can access access in a tuple using positions or names.
<!--SR:!2024-04-05,33,230-->


#### What is the default behavior of Swift Function params?
?
They are value parameters or constants - i.e. **not referenced**. This means they can't be changed inside of a function.
To make a function param a reference, you have to add the `inout` keyword to the parameter.
<!--SR:!2024-04-04,32,228-->


#### What is Trailing Closure Syntax
?
It means that if the last parameter to a function is a closure, you can use special syntax to pass it in as a parameter
```
func travel(action: () -> Void) {
    print("I'm getting ready to go.")
    action()
    print("I arrived!")
}


travel() {
    print("I'm driving in my car")
}
```
<!--SR:!2024-05-09,67,290-->

#### What is Closure Inference?
?
It means that Swift will infer the parameter and return types of a closure. You can also omit parameter names to a closer, and use the `$0` syntax.
```swift
travel {
    "I'm going to \($0) in my car"
}
```
<!--SR:!2024-04-13,41,248-->

[[Swift - Structs]]
[[Swift - Classes]]
[[Swift - Protocols]]
[[Swift - Optionals]]
[[Swift UI]]
[[Core ML]]
