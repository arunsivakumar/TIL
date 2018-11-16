# Swift

###### Defer

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

###### [unowned self] [weak self]

###### Type Properties:
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

###### Array:
```
extension Array {
    subscript (safe index: Int) -> Element? {
        return indices ~= index ? self[index] : nil
    }
}
```

###### Associated Type
###### Error handling
###### Closure- Escaping and non escaping
###### Protocol Extensions

###### SequenceType, Comparable, Equitable, Hashable
```
extension Action: Equatable { }
func ==(lhs: Action, rhs: Action) -> Bool {
return false
}
```
