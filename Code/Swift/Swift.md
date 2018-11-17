# Swift

### Defer

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

### [unowned self] [weak self]

### Type Properties:
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

### Array:
```
extension Array {
    subscript (safe index: Int) -> Element? {
        return indices ~= index ? self[index] : nil
    }
}
```

### Class vs Struct

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

Excerpt From: By Ray Fix. “Swift Apprentice.” iBooks.

###  Associated Type
###  Error handling
### Closure- Escaping and non escaping
### Protocol Extensions

### SequenceType, Comparable, Equitable, Hashable
```
extension Action: Equatable { }
func ==(lhs: Action, rhs: Action) -> Bool {
return false
}
```
