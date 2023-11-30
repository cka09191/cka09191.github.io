---
title: Optional in Swift Programming
categories:
  - Swift
feature_text: Ideally, there should be no nil values initially. However, like in a GUI environment where asynchronous tasks exist, encountering nil values is not uncommon. You have to use optional values where safety is required. Also, consider the situation you are in when unwrapping to choose the most readable and stable approach for your program.
excerpt: |
  We can avoid errors caused by nil values by using Optional types. Optional types should be safely unwrapped before use.
---

## Define Optional Values

```swift
//1. Using Type?
var specificOptionalNumber: Int? = 123


//2. Using Optional<Type>
var anotherOptionalNumber: Optional<Int> = 123
```
There are two ways to define an optional value: `Type?` or `Optional<Type>` .


## Unwrapping Optional Values
There are two ways to unwrap an optional value: optional binding and using unwrapping operators(?, ??, !).

#### Using Optional Binding
You can bind the value wrapped inside the optional value to a non-optional value.

There are three statements for optional binding: `if let`, `guard let`, and `switch`. Each can be used depending on the situation: What kind of optional value is? Does the fact that it's not a `nil` value matter? Or is `nil` value dangerous? Do you need more options?

###### Using `if let`
Use `if let` statement if you need to perform a task only when your value is not `nil`.
```swift
//1. if let
if let nonOptionalValue = optionalValue {
	print("I can use "+nonOptionalValue)
}
```

###### Using `guard let`
Use `guard let` for an early exit pattern.
```swift
//1. throw exception
guard let nonOptionalValue = optionalValue else {
	throw ValueIsNilException	
}

//2. return or break
guard let secondNonOptionalValue = secondOptionalValue else {
	return false
	//break //in loop
}

```

###### Using `switch`
Use `switch` if you need more options.
```swift
switch optionalValue {
case let .some(nonOptionalValue as Int) where nonOptionalValue>10:
	// 'nonOptionalValue' is an Int and over 10.
case let .some(nonOptionalValue as Int):
    // 'nonOptionalValue' is an Int
case let .some(nonOptionalValue as String):
    // 'nonOptionalValue' is a String
case .none:
    // 'optionalValue' is nil
}

```

#### Using Unwrapping Operators
There are three operators unwrapping an optional value: optional chaining(`?`), nil coalescing operator(`??`), forced unwrapping(`!`). These operators can used for simple cases. You can consider as same above: What kind of optional value you using? How do you do when it is nil?

###### Using Optional chaining(`?`)
You can use methods or properties of optional value with `?`. If the value is nil, the whole return or value is nil.
```swift
let nameLength = person?.name?.count
```

###### Using nil coalescing(`??`)
You can designate replacement for nil with `??`
```swift
let name = person?.name ?? "Unknown"
```


###### Using forced unwrapping(`!`)
If you know the optional value is not nil, or you need to get error for this situation, you can use `!`
```swift
for person in checkedListofStudents {
	let name = person!.name
}
```

## Afterword
Ideally, there should be no nil values initially. However, like in a GUI environment where asynchronous tasks exist, encountering nil values is not uncommon. You have to use optional values where safety is required. Also, consider the situation you are in when unwrapping to choose the most readable and stable approach for your program.