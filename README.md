## Swift
#### Language purposes/genesis
1. ##### Why was the language created/What problems was the language trying to address?
	- Swift was a large improvement to Objective-C, it incorporated a lot of the benefits of other languages into one package. It read like a modern language, but had the performance of C++. It also didn’t have issues with garbage collection. On Top of this it allowed programmers to incorporate swift with Objective-C so the language didn’t become obsolete

2. ##### Is the language a reaction to a previous language or a replacement for another language?
	- Yes it is a reaction to Objective-C

#### Unique features of the language
1. ##### Does the language have any particularly unique features?
	- Simple, easy to read syntax. It reads like a sentence. Optionals and nil which take down the issue of null pointer exceptions. It has lazy properties and allows parameters to be named.

#### Name Spaces
1. ##### How are name spaces implemented?
	- Namespacing is implicit in Swift, all classes (etc) are implicitly scoped by the module they are in. no class prefixes needed
2. ##### How are name spaces used?
	- TODO

#### Types
1. ##### What types does the language support?
	- Int, UInt, Float, Double, Bool, String, Character, Optional, Tuples

2. ##### Are both reference and value types supported?
	- Yes, swift has classes and structs which allows you to store data in a form of an object

3. ##### Can new value types be created?
	- Yes, swift has classes and structs which allows you to create new types

#### Classes
1. ##### Defining
```
	class SomeClass {
		//Class Body
	}

	struct SomeStruct {
		//Struct Body
	}
```
2. ##### Creating new instances
```
	let someObject = SomeClass()
```
3. ##### Constructing/initializing
```
	class Thermometer {
	      var temperature: Double
	      init() { 
		  temperature = 32.0 
	      }
	}
```
4. ##### Destructing/de-initializing
	- This method is included in the body of the class
	```
	deinit {
    		//perform the deinitialization
    	}
	```

#### Instance reference name in data type (class)
- Swift uses self 
```
	self.myVar = 32.0
```

or in an init
```
	var myVar;
	init(myVar: String) {
    		self.myVar = myVar
    	}
```

#### Properties
1. ##### Getters and setters…write your own or built in?
	- Swift uses computed properties
	```
	var x: Int { 
        	set {x2 = valuePassed} 
            	get {return x2}
        }
    ```
2. ##### Backing variables?
	- You can use backing variables in swift
	```
    	var myVar
        init(myVar: String) {
        	self.myVar = myVar
        }
        
        func getMyVar() -> String {
        	return self.myVar
        }
        
        func setMyVar(myVar: String) {
        	self.myVar = myVar
        }
    ```
3. ##### Computed properties?
	- Same as above, they can be used as getters and setters (Example 1)

#### Interfaces/Protocols
1. ##### What does the language support?
	- Swift supports protocols which function as interfaces
2. ##### What abilities does it have?
	- A protocol in Swift defines methods or properties that a class can then adopt
3. ##### How is it used?
	- Its used when a methods can be used my multiple objects, so instead of duplication that object just implements the method from one place

#### Inheritance/Extension
- Swift has inheritance
```
	class GermanShephard: Dog {
    
    	}
```
- Inheritance allows us to go from general to specific, for example all dogs can bark, but only a german shephard can sniff drugs, so we would have a drug sniffing method in the GermanShephard class but not in the dog class.

#### Reflection
1. ##### What reflection abilities are supported?
	- Swift reflection allows us to look at objects properties without modifying them.
2. ##### How is reflection used?
	- TODO

#### Memory management
1. ##### How is it handled?
	- Swift uses ARC (Automatic Reference Counting)
2. ##### How does it work?
	- Every time you create a new instance of a class, ARC allocates a chunk of memory to store information about that instance. This memory holds information about the type of the instance, together with the values of any stored properties associated with that instance.
	- Additionally, when an instance is no longer needed, ARC frees up the memory used by that instance so that the memory can be used for other purposes instead. This ensures that class instances do not take up space in memory when they are no longer needed.
3. ##### Garbage collection?
	- Swift does not use garbage collection
4. ##### Automatic reference counting?
	- Yes, described above

#### Comparisons of references and values
1. ##### How are values compared? (i.e. comparing two strings)
	- Swift uses ```==``` even for strings

#### Null/Nil references
1. ##### Which does the language use? (null/nil/etc)
	- Swift uses ```nil```
2. ##### Does the language have features for handling null/nil references?
	- Swift has optionals, which can either have a value or not, eliminating null pointer exceptions

#### Errors and exception handling
- Swift has the throws statement
- characteristics of a ```throws``` statement are comparable to those of a return statement.
- There is also do-catch statements 
```
	do { 
    		try expression
        		statement 
	} catch { 
    
	}
```

#### Lambda expressions, closures, or functions as types
- Swift does not use lambda expressions but has closures
- This allows you to condense 
```
reversedNames = names.sorted(by: { (s1: String, s2: String) -> Bool in
   return s1 > s2
})
```
into

```
reversedNames = names.sorted(by: >)
```

#### Implementation of listeners and event handlers
- Swift uses IBActions, which allow you to link actions to UI elements to can handle events
#### Singleton
1. ##### How is a singleton implemented?
	- Singletons in swift are implemented by creating an Instance of the class in itself (statically) and then calling that variable on the class whenever its needed
2. ##### Can it be made thread-safe?
	- Yes the above method is thread safe
3. ##### Can the singleton instance be lazily instantiated?
	- Swift singletons are guaranteed to be lazy
#### Procedural programming/Functional Programming
1. ##### Does the language support procedural/functional programming?
	- Swift primarily uses procedural programming, but there are tools that allow you to use bits of functional programming [Monad](https://en.wikipedia.org/wiki/Monad_(functional_programming))
#### Multithreading
1. ##### Threads or thread-like abilities
	- There are timers, which allow you have timed tasks that repeat indefinitly or finish after one run
2. ##### How is multitasking accomplished?
	- Code implementation here
