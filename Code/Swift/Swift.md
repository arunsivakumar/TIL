# Swift

### Features
##### Structures & Classes

```
struct Resolution {
    var width = 0
    var height = 0
}
class VideoMode {
    var resolution = Resolution()
    var interlaced = false
    var frameRate = 0.0
    var name: String?
}

let tenEighty = VideoMode()
let alsoTenEighty = tenEighty
tenEighty.frameRate = 25.0
alsoTenEighty.frameRate = 30.0
```
tenEighty and alsoTenEighty themselves don’t “store” the VideoMode instance—instead, they both refer to a VideoMode instance behind the scenes. It’s the frameRate property of the underlying VideoMode that is changed, not the values of the constant references to that VideoMode.

###### Mutating Struct
```
struct Counter {
    private var value = 0
    mutating func next() {
        value += 1
} }
```

works -
```
var counter = Counter()
counter.next()
```

doesnt work -

```
let counter = Counter()
counter.next()
//  error: cannot use mutating member on immutable value: 'counter' is a 'let' constant
```

###### Equatable
```
class Dog: Equatable {
    let name: String
    init(name: String) { self.name = name }
}

// Consider two dogs equal if their names are equal.
func ==(lhs: Dog, rhs: Dog) -> Bool {
    return lhs.name == rhs.name
}

// Create two Dog instances which have the same name.
let spot1 = Dog(name: "Spot")
let spot2 = Dog(name: "Spot")

spot1 != spot2   // false

spot1 === spot2  // false, because the dogs are different instances
spot1 !== spot2  // true
```

##### Type Methods:

Struct - use static func()   
Class - static (non-override), class (override)

```
class Animal {
    class var noise: String {
        return "Animal noise!"
    }
}
class Pig: Animal {
    override class var noise: String {
        return "Oink oink!"
    } }
Pig.noise
```
Struct with let never changes values even though x and y are variables

```
struct Point {
var x: Int
var y: Int
}

var p = Point(x: 0, y: 0){
    didSet{
        print(p)
    }
}

p.x = 20
```

even if we change something deep inside the struct, the didSet handler will get triggered

###### Class vs Struct

###### Structures
* Useful for representing values.
* Implicit copying of values.
* Becomes completely immutable when declared with let.
* Fast memory allocation (stack).

###### Classes
* Useful for representing objects with an identity.
* Implicit sharing of objects.
* Internals can remain mutable even when declared with let.
* Slower memory allocation (heap).”


### Others
##### Defer

https://nshipster.com/guard-and-defer/

```
func procrastinate() {

    defer{
        print("clean the gutter 1")
        defer{
            print("clean the gutter 2")
        }
    }
//    defer { print("wash the dishes") }
//    defer { print("take out the recycling") }
//    defer { print("clean the refrigerator") }

    print("play videogames")
}
procrastinate()
```

##### [unowned self] [weak self]

##### Array:
```
extension Array {
    subscript (safe index: Int) -> Element? {
        return indices ~= index ? self[index] : nil
    }
}
```
Excerpt From: By Ray Fix. “Swift Apprentice.” iBooks.

#####  Associated Type
#####  Error handling
##### Closure- Escaping and non escaping
##### Protocol Extensions

##### SequenceType, Comparable, Equitable, Hashable
```
extension Action: Equatable { }
func ==(lhs: Action, rhs: Action) -> Bool {
return false
}
```
TODO:   

[] - BNR  Mutating methods
