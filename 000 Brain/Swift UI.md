---
Created On: 2024-01-17, 09:56
Unique ID: 202401170956
---
**Status:** #moc 

**Tags:** #SwiftCards 

# Swift UI

#### How do you mark a variable to be updated as State?
?
Add the `@State` modifier to it's declaration.
```swift
@State private var stateBoolean = false;

struct body: View {
		Button("Text") {
				// This change will update UI
				stateBoolean = true
		}
}
```
<!--SR:!2024-05-06,64,270-->


#### In SwiftUI, what are Bindings?
?
Bindings are elements that naturally attach a state to a view. Some Views require bindings (like pickers and sliders) because they require a piece of data to power them (i.e. slider position or picker selection).
<!--SR:!2024-05-07,65,270-->


#### In SwiftUI, how do you create a binding?
?
You can either use an `@State` variable and add a `$` before it to create a binding. But under the hood, that is creating a `Binding`. You can create custom bindings to manipulate state in more succinct ways.
```swift

@State private var agreedToTerms = false
@State private var agreedToPrivacyPolicy = false
@State private var agreedToEmails = false

let agreedToAll = Binding<Bool>(
            get: {
                agreedToTerms && agreedToPrivacyPolicy && agreedToEmails
            },
            set: {
                agreedToTerms = $0
                agreedToPrivacyPolicy = $0
                agreedToEmails = $0
            }
        )
```
<!--SR:!2024-04-07,35,250-->


#### In Swift UI, what is the default click action of a button (or any view), in an alert?
?
The default click action closes the alert.
<!--SR:!2024-05-14,72,290-->


#### Why does SwiftUI use structs instead of classes? And what is the history of this choice?
?
Classes originate from the earliest programming languages. Classes are generally, but not strictly, coupled to object-oriented program design.
Object-oriented design was the leading design trend for many UI based programs for many years, but in the internet age, as application development has jerked forward (i.e. has continued to accelerate), some pitfalls of at-scale object-oriented design have been displayed.
Primarily, the issue of inheritance.
See my note on [[Swift - Protocols#What is the difference between Inheriting and Composing when designing object or protocol-oriented software?]]
Inheritance is a very rigid structure. At first this seems good. To play the game, you need to know the definitive set of rules.
But over time, these rules change, break, grow large, and start to make less and less sense. 
It has become evident that breaking large apps into smaller, composable pieces is much more maintainable. 
In summary
> **Structs suggest composition over inheritance, leading to smaller, more performant, more flexible, and easier-to-understand applications.**
<!--SR:!2024-05-05,63,270-->



#### Why does Modifier order matter in SwiftUI?
?
Because Views are structs, and each modifier on a struct creates a new struct (not a modified version of the last one).
Put in other words, as soon as a frame can be rendered, it is rendered.
For example
```swift
Button("Hello, world!") {
    // do nothing
}    
.background(.red)
.frame(width: 200, height: 200)
```
vs.
```swift
Button("Hello, world!") {
    print(type(of: self.body))
}
.frame(width: 200, height: 200)
.background(.red)
```
The first will not create what you expect - the size of the red box will only cover the text. This is because the red frame is painted before the new frame width is called.
<!--SR:!2024-05-08,66,270-->


#### In Swift, what is the `@ViewBuilder`?
?
It is essentially a block-level compiler adjustment. This means that attaching `@ViewBuilder` to a function, allows you to write code differently within that block. The `@ViewBuilder` is designed to make returning views easier to work with. 
In the example below - if you didn't have `@ViewBuilder` on `GreetingView` - you would need return statements and you wouldn't be able to return multiple elements.
```Swift
import SwiftUI

@ViewBuilder
func GreetingView(show: Bool) -> some View {
    if show {
        Text("Hello, SwiftUI!")
            .font(.largeTitle)
            .padding()
		Button("Press me!") {
			print("You've done it. You've built a view!")
		}
    } else {
        Text("Goodbye, SwiftUI!")
            .font(.headline)
            .padding()
    }
}

struct ContentView: View {
    @State private var showGreeting = true

    var body: some View {
        VStack {
            Toggle(isOn: $showGreeting) {
                Text("Show Greeting")
            }.padding()

            GreetingView(show: showGreeting)
        }
    }
}

```
<!--SR:!2024-05-04,62,270-->

