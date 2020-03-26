---
layout: post
title: Swift Protocol
---

In Swift language a protocol defines a blueprint of methods and properties. The protocol can be adopted by a class, structure, or enumeration. Any type that satisfies the requirements of a protocol is said to conform to that protocol.

## What is protocol?

  1. Protocol is a type just like class, struct and enum.
  2. Protocol is basically just a list of methods and properties with no implementation.
  3. Protocol is a way to express an API more concisely.

## How to use protocol?

### Protocol declaration:

```swift
protocol Moveable {
  func move()
}
```

### Conforming protocol:

```swift
class Car: Moveable {
  func move() {
    print("Moving!")
  }
}
```

Conforming multiple protocols is possible.

```swift
class Car: Moveable, Paintable {
  // class definition
}
```

## Property requirement

A protocol can require any conforming type to provide an instance property or type property with a particular name and type. The protocol also specifies whether each property must be gettable or gettable and settable. Gettable and settable properties are indicated by writing { get set } after their type declaration, and gettable properties are indicated by writing { get }.

```swift
protocol FullNamable {
  var firstName: String { get set }
  var lastName: String { get set }
  var fullName: String { get }
}
```

Type property is prefixed with the static keyword in a protocol definition.

```swift
protocol SomeProtocol {
  static var someTypeProperty: Int { get set }
}
```

## Method requirement

Protocols can require specific instance methods and type methods to be implemented by conforming types.
Type method is prefixed with the static keyword in a protocol definition.

```swift
protocol SomeProtocol {
  static func someTypeMethod()
}
```

## Protocol example

```swift
let car = Car()
let dog = Dog()

let movingObjects: [Movable] = [car, dog]

for movingObject in movingObjects {
  movingObject.move()
}
```
