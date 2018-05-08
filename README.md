# Grant Maloney
# Jeremy Gonzalez

## Java
#### Language purposes/genesis
1. ##### Why was the language created/What problems was the language trying to address?
	- James Gosling, Mike Sheridan, and Patrick Naughton initiated the Java language project in June 1991. Java was originally designed for interactive televrision, but it was too advanced for the digital cable television industry at the time. Later the project went by the name Green and was finally renamed Java, from Java Cofee.

2. ##### What problems was the language trying to address?
	- Java is a general-purpose computer-programming language that is concurrent, class-based, object-oriented, and specifically designed to have as few implementation dependencies as possible. It is intended to let application developers "write once, run anywhere" (WORA), meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.

2. ##### Is the language a reaction to a previous language or a replacement for another language?
	- Gosling designed Java with a C/C++ style syntax that system and application proggamers would find familiar.

#### Unique features of the language
1. ##### Does the language have any particularly unique features?
	- Simple: Java was designed with a small number of language constructs so that programmers could learn it quickly. Eleminates several language features available in C/C++ that are associated with poor programming practices or rarely used: goto statements, header files, structures, operator overloading, multiple inheritance, and pointers.
	- Object-Oriented: Java is an OOPL that supports the construction of programs that consist of collections of collaborating objects. These objects have a unique identity, encapsulate attributes and operations, and are instances of classes related by inheritance and polymorphism.
	- Distributed: Java is designed to support various levels of network connectivity. Java applications are network aware: TCP/IP support is built into Java class libraries. They can open and access remote objects on the internet.
	- Robust: Java is designed to eliminate certain types of progamming errors. Java is strongly typed, which allows extensive compile-time error checking. It does not support memory pointers, which eleminates the possibility of overwriting memory and corrupting data. In addition, its automatic memory management eliminates memory leaks and other problems associated with dynamic memory allocation/de-allocation.
	- Secure: Java is designed to be securein a network environment. The Java run-time environment uses a bytecode verification process to ensure that code loaded over the network does not violate Java security constraints.
	- Architecture neutral: Java applications that are compiled to bytecodes can be interpreted by any system that implements the Java Virtual Machine. Since the Java Virtual Machine is supported across most operating systems, this means tha Java applications are able to run on most platforms.
	- Portable: In addition to supporting architecture neutrality, Java ensures that other implementation-dependent aspects of language specification are eliminated. For example, Java specifies the sizes of primitive data types and their arithmetic behavior. 
	- Multithreaded. Java supports multiple threads of execution (a.k.a., lightweight processes), including a set of synchronization primitives. This makes programming with threads much easier.
	- Dynamic language. Java supports dynamic loading of classes (a.k.a. “load on demand”), dynamic compilation, and automatic memory management (garbage collection).

#### Name Spaces
1. ##### How are name spaces implemented?
	- The Java platform includes packages with names that begin with java, javax, and org.omg. The most fundamental classes of the language are in the package java.lang. Various utility classes are in java.util. Classes for input and output are in java.io, and classes for networking are in java.net. Some of these packages contain subpackages. 
2. ##### How are name spaces used?
	- For example, java.lang contains two more specialized packages, named java.lang.reflect and java.lang.ref, and java.util contains a subpackage, java.util.zip, that contains classes for working with compressed ZIP archives.
	- Every class has both a simple name, which is the name given to it in its definition, and a fully qualified name, which includes the name of the package of which it is a part. The String class, for example, is part of the java.lang package, so its fully qualified name is java.lang.String.

#### Types
1. ##### What types does the language support?
	- Byte, short, int, long, float, double, char, String, boolean

2. ##### Are both reference and value types supported?
	- Yes, java manipulates objects by reference, and all object variables are references; java although passes objects by value

3. ##### Can new value types be created?
	- Yes, you can accomplish this by creating a new class

#### Classes
1. ##### Defining
```
/** 
 * The HelloWorldApp class implements an application that
 * simply displays "Hello World!" to the standard output.
 */
class HelloWorldApp {
    public static void main(String[] args) {
        System.out.println("Hello World!"); //Display the string.
    }
}
```
2. ##### Constructing/initializing
```
public class Point {
   public int x = 0;
	   public int y = 0;
	   //constructor
	   public Point(int a, int b) {
	        x = a;
        y = b;
	   }
}
```
3. ##### Creating new instances
```
	Point originOne = new Point(23, 94);
```

4. ##### Destructing/de-initializing
	- Java is a garbage collected language so it cannot predict when an object will be destroyed. So there is no destructor/de-initializer

#### Instance reference name in data type (class)
	- Java uses the “this” keyword for instance referencing

#### Properties
1. ##### Getters and setters…write your own or built in?
	- In Java you create your own Getter and Setter methods
```
public void setName(String name) {
	This.name = name;
}
public String getName() {
	Return name;
}
```
2. ##### Backing variables?
	- Java does not have backing variables
3. ##### Computed properties?
	- Java does not support computed properties 

#### Interfaces/Protocols
1. ##### What does the language support?
	- Java supports interfaces
2. ##### What abilities does it have?
	- In general, interfaces facilitate the key concepts in OOP like abstraction, inheritance and polymorphism. In addition, interfaces add flexibility and re-usability for software components.
3. ##### How is it used?
	// A simple interface
```
interface Player {
    final int id = 10;
    int move();
}
 
```

#### Inheritance/Extension
1. Java supports inheritance where you can inherit from at most one other class.

#### Reflection
1. ##### What reflection abilities are supported?
	- Allows an executing Java program to examine or "introspect" upon itself, and manipulate internal properties of the program. Does not exist in a lot of other programming languages.
2. ##### How is reflection used?
	- It is used to describe code which is able to inspect other code in the same system (or itself).

#### Memory management
1. ##### How is it handled?
	- Java objects reside in an area called the heap, where the heap is created when the JVM starts up.
2. ##### How does it work?
	- The heap may increase or decrease in size while an application runs.
3. ##### Garbage collection?
	- When the heap becomes full, garbage is collected. During the garbage collection objects that are no longer used are cleared, thus making new space for new objects
4. ##### Automatic reference counting?
	- Should let the garbage collector do the reference management instead of doing it manually.

#### Comparisons of references and values
1. ##### How are values compared? (i.e. comparing two strings)
	- To compare to objects in java you would use the ```.equals()``` method.

#### Null/Nil references
1. ##### Which does the language use? (null/nil/etc)
	- Java uses ```null``` for null references
2. ##### Does the language have features for handling null/nil references?
	- Unlike Swift, Java does not have a feature for handling null references.

#### Errors and exception handling
- In Java, in order to avoid exceptions or errors you would use a try catch block where the catch portion would catch any errors or exceptions that would occur.

#### Lambda expressions, closures, or functions as types
- Lambda expressions enable you to do this, to treat functionality as method argument, or code as data.
  This method prints members that are older than a specific age:
```
public static void printPersonsOlderThan(List<Person> roster, int age) {
	for (Person p : roster) {
		if (p.getAge() >= age) {
			p.printPerson();
		}
	}
}
```

#### Implementation of listeners and event handlers
- Event Listener: 
  Waits for input in order to do something
  Ex) implementing the event handling for a button:
```
public class Beeper ... implements ActionListener {
    ...
    //where initialization occurs:
        button.addActionListener(this);
    ...
    public void actionPerformed(ActionEvent e) {
        ...//Make a beep sound...
    }
}
```
#### Singleton
1. ##### How is a singleton implemented?
	- A class that can have only one object (an instance of the class) at a time.
```
public class ClassicSingleton {
   private static ClassicSingleton instance = null;
   protected ClassicSingleton() {
      // Exists only to defeat instantiation.
   }
   public static ClassicSingleton getInstance() {
      if(instance == null) {
         instance = new ClassicSingleton();
      }
      return instance;
   }
}
```
2. ##### Can it be made thread-safe?
	- Yes
	  > Create the instance variable at the time of class loading. 
      > Synchronize the getInstance() method. 
      > Use a synchronized block inside the if loop and volatile variable.

3. ##### Can the singleton instance be lazily instantiated?
	- Yes, in java a singleton can be lazily constructed requiring no memory or resources until needed.
#### Procedural programming/Functional Programming
1. ##### Does the language support procedural?
	- Yes, Java supports procedural programming.
2. ##### Does the language support functional programming?
	- Yes, java supports functional programming 
    - Lambda expressions

#### Multithreading
1. ##### Threads or thread-like abilities
	- Java supports threads:
``` 
public class HelloRunnable implements Runnable {
    public void run() {
        System.out.println("Hello from a thread!");
    }
    public static void main(String args[]) {
        (new Thread(new HelloRunnable())).start();
    }
}
```
2. ##### How is multitasking accomplished?
	- In Java, you can have multiple run() methods to have multitasking in multiple threads.
	- Program of performing two tasks by two threads:
```
class Simple1 extends Thread{  
	public void run(){  
		System.out.println("task one");  
	}  
}   
class Simple2 extends Thread{  
	public void run(){  
		System.out.println("task two");  
	}  
}    
class TestMultitasking3{  
	public static void main(String args[]){  
		Simple1 t1=new Simple1();  
		Simple2 t2=new Simple2();    
		t1.start();  
		t2.start();  
 	}  
}
```

---

## Swift
#### Language purposes/genesis
1. ##### Why was the language created/What problems was the language trying to address?
	- Chris Lattner wrote swift for Apple in 2014.  Swift was a large improvement to Objective-C, it incorporated a lot of the benefits of other languages into one package. It read like a modern language, but had the performance of C++. It also didn’t have issues with garbage collection. On Top of this it allowed programmers to incorporate swift with Objective-C so the language didn’t become obsolete

2. ##### Is the language a reaction to a previous language or a replacement for another language?
	- Yes it is a reaction to Objective-C

#### Unique features of the language
1. ##### Does the language have any particularly unique features?
	- Simple, easy to read syntax. 
	- It reads like a sentence. 
	- Optionals and nil which take down the issue of null pointer exceptions. 
	- It has lazy properties
	- Allows parameters to be named (makes passing in data to a function so much easier and more understandable)

#### Name Spaces
1. ##### How are name spaces implemented?
	- Namespacing is implicit in Swift, all classes (etc) are implicitly scoped by the module they are in. no class prefixes needed
2. ##### How are name spaces used?
	- Namespaces are not per-file; they're per-target (based on the "Product Module Name" build setting).
	- All Swift declarations are considered to be part of some module, so even when you write "NSLog" you're getting what Swift thinks of as "Foundation.NSLog". (its fully qualified package name)

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
	- Reflection is used to find methods inside code by utilizing different parameters for example.
```
	class MyClassName{
		var myNumber

		func doSomething(number: Int) -> Int{
			return number * number
		}
	}
	
	var result = doSomething(4)
	
	// pseudocode
	var m = findMethod("doSomething");
```

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
```
	func turnFamiliarIntoToad() throws -> Toad { }
```
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
```
	myTimer = Timer.scheduledTimer(timeInterval: 5, target: self, selector: #selector(runTimedCode), userInfo: nil, repeats: true)
	
	@Obj-c
	func runTimedCode() {
		//Do action that will repeat every 5 seconds here
	}
```
