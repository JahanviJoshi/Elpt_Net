Open Visual Studio 2019/2022 (Enterprise/Pro/Comminuty Edition)

- Two Important Concepts
	- Solution
		- A Workspace for all .NET Projects
		- Extension is '.sln'
	- Project
		- The Application developed by developer
		- Contains Source Code
			- Class Files
		- Project Types
			- Desktop Projects
				- Console Apps, WinForm, WPF, Windows Service
				- Compiled into EXE
			- Class Library Project
				- Code for distrubution in other projects
				- Compiled into DLL
			- Web Application Project
				- Compiled into DLL and Hosted into the EXE (Only for .NET Core, .NET 5/6)
					- ASP.NET Razor
					- MVC
					- WEB API
					- Blazor
			- Other Project Types
				- Mobile Apps
				- IoT Apps
				- Third-Party Apps
				- Node.js
				-... and many more

- Solution will be created directly when the Project is created
- We Can create a 'Blank Solution' and add Projects in it	

- File-->New-->Project
	--> This will open a Dialog Box, Select Blank Solution from it
		--> Next --> Name The Solution and Set the Location e.g. C:\Coditas
			--> Create 
- Right-Click on the Solution and Select 'Add New Project'
	--> From 'Add New Project' DialogBox, select the 'Console Application'	
		(Note: Select the COnsole Application with C# Linux macOS Windows Console on it)
	--> Click on 'Next' --> Provide the Project Name-->Keep the Location of the 'Solution' as it is
	--> CLick on 'Next' --> From the Dropdown select '.NET 5'
	--> Click on Create
- If a Solution Contains Multiple-Projects, then to run a spefic project from the solution 
	--> Right-Click on the Project and select the 'Set as startup project'

#===============================================================================================================
# Project Structure
	- Each Project has dependencies
		- They are the Sandard or 'Common Base Libraries' those are required to execute the Project
		- e.g.
			- Microsoft.NETCore.App
				- A .NET 5 Library that has all the .NET 5 Common Libraries inside it

# .NET EcoSystem OR Building Blocks for Application Development 
	- Common Language Specificcations (CLS)
		- Common Language Specifications, The Syntax Check in Source Code, Verify the Keywords (Semantics) e.g. Verify the Expression

		e.g. Left-Hand-Side = Right-Hand-Side; 
		e.g. If  x is declared as integer, then value in x MUST be in the Range of Integers

	- Common Type System (CTS)
		- This contains all DataTypes in it 
		- The CLS uses CTS to maske sure that the Source code have used the DataType Propertly with value Ranges
			- Numeric Types
			- Character
			- Strings
			- DateTime
			- Boolean
	- Common Language Runtime (CLR)
		- Execute the Applciation after IL is JIT Compiled
		- Memory Management	


# C# Programming Language
	- Major Language on .NET Platform
	- 100% Object Oriented Programming Language
	- The Main() method, the Entry Point of the Application
	- The 'Namespace'
		- A Logical Container for all classes
		- Each Project Name (aka Assembly-Name) is a Namespace
		- Ine One Application there can be Multiple Namespaces athe they will be
			- [PROJECT-NAME].[CUSTOM-NAMESPACE-NAME]
		- If the Source-code uses any class, then make sure that its namespace is imported in Source code file as (CLS Rule)
			- using [NAMESPACE-NAME]
	- The 'Console' class
		- A Class under the 'System' Namespace
		- The WriteLine() method that is used to print message to the console window
		- The ReadLine() meth, used to accept data from the COnsole which is always 'string'
			- To Convert the String into Integer, Short, Byte, double, decimal, float, etc.
				- use  'Convert' Class
	- To Run the Project, Press F5 button
		- To Build the Project 
			- Build Menu --> Build Project Name
		- Project Debugging
			- It is Process using which an execution of each statement is verified
			- Follwoign Steps MUST be followed for debugging
				- using 'F9' to apply the Breakpoint on the line from which code is debugged
				- Run the Project using 'F5' and that will enter into the Debug-Mode from the breakpoint line
				- Using 'F11' to debug each line in source-code, inclusing the method call by jumping into the method
				- OR If you want to skip the JUMP into the called method body, then use 'F10'
# Creating Methods
	- In a Program class, each method MUST be 'static'
	- This method can have input and output parameters
		- static [RETURN-TYPE] [METHOD-NAME](PAREMETERS)
		{
		    // METHOD-BODY
		}
		- PARAMETERS: They are called as 'Formal-Parameters'
	- If a method is returning a value, them make sure that, the method has 'return' statement
		- If there is if.. OR if...else... then these Block MUST have return statement
		- OR If the if..else... block is processng data based on condition (if/else) then out of the if..else.. block return the data with return statement. 
# C# Programming Strctures
	- Conditional Staructrure
		- if statement
		- if...else statement
		- nested if
			- if...else...if
		
		- Switch Block
			- switch(Parameter OR Value to be conditionally check)
				- case [CONDITION]:	
						{
							// EXECUTION-BLOCK		
						}
				- .... multiple cases
				- default:
					// do something if non of the condition is satisfied		
	- Condition Operators
		- > , < , >=, <=, == (Comparision), != (Not-Equal)
		- Logical Operators
			- || OR
			- && AND
			- ! NOT
	- Iterations	
		- Loops used for reading the Data
			- for..loop
			- foreach
			- while
			- do..while
		- These are index Based Loops
			- StartIndex, Condition to stop/terminate, EndIndex
	- Defining Methods parameters
		- using the 'ref'
			- it is a mechanim for passing parameter references of actual parameter to a method instead of actual parameter value
			- Syntax
				- int a=10,b=20
				- pass the parameter
					- Change(ref a, ref b);
				- void Change(ref int x, ref int y) {}
			- IMP: The declaration with 'ref' MUST be initialoized befor passing to method
		- using the 'out'
			- Like 'ref'
			- The 'out' varianble need not be initialized before passing to the method
			- Generally used when a method want to return more than a parameter (a single value) from a method
				- Change(out a, out b);
			- void Change(out int x, out int y) 
			{
				// set value for x and y and then process
				// the processed value will be set to the actual parameter over its reference
			}
		- using the 'params' a mechanism of passing flexible number of parameters to a method
			- Internally this will be treated as an 'Array' 
			- The method MUST have 'params' as a last parameter to a method
			- e.g.
				- VALID Syntax
					- Add(int a,int b, params int[]x){}
				- INVALID Syntax
					- Add(params int[]x,int z,int y){}
# C# String
	- Array of Characters
		- Using '+' sign to Concat the String
	- By default string is a class that has verious methods
	- Interpolation or String Termplates
		- Mechanism of String Concatination
			- OLD: str1 + str2
			- Interpolations: $"{str1} {str2}"
				- Internally will invoke 'String.Format()'
	- Techniacally
		- A String is an Array of Characters
# Using C# Data Structures
	- An arrangement for stroing data in well-organized manner for efficient Read/Write
		- Array
			- The Most popular
			- System.Array is a Class for defining an Array type
			- Syntax
				- DataType [] Identifier;
				- By Default an array identifier is an instance of array class 
				- THis will provides various methods to work with array 
		- Collections
			- A preferred way of storing data in memory
			- This need not to be set with UpperSize by default
			- We can keep on adding data in it
			- IMP: Each entry in collection is stored as 'an object'
			- System.Collections is a namespace having collection classes 
				- ArrayList, LinkedList, Stack, Queue, etc.
			
		- Generics
			- Data Structure Templates
				- A predefined arrangement for Storing data which is common for all data types
			- USed to store data of 'SAME-TYPE' in the Collections in the memory w/o boxing 
			- System.Collectrions.Generic
				- List<T>
				- ArrayList<T>
				- Stack<T>
				- Queue<T>
				- ..... and many more
			- The 'T' is a Template Parameter aka Type Parameter that will be stored in the Data Structure
				- If 'T' is 'int' then the data structure will have data only oif the type integer
				- E.g. List<int> will create a List of Integers, List<string> will have only strings 
				- T can be any CTS type
					- Primitive Types
					- Custom CLR types
						- Classes
						- Methods
						- Interfaces
						- Events
						- Delegates
			- Once the 'T' is set to the specific type e.g. int or string, a seperate copy of the same generic type will be created into the memory in Binary Format
			- Mukti-Type Generics
				- The Data Structure used for Multiple-Type Parameters
				- MyClass<U,V>
					- Typically used for storing Key/Value pair


# Object Oriented Programming (OOPs) with C#	
	- Class
		- Access Specifiers, used to define the scope for accessing, class and its members
			- public, private, protected
			- internal, protected internal
		- Access Modifiers, they are used to define access behavior of the class and its members 
			- static, abstract, virtual, sealed
		- Inheritance
		- Polymorphism
	- Interface

	- Class is an encapsulation for
		- Data Members 
			- They are the properties used to store data for the class
			- This is an Abstraction for the data 
		- Members Methods (functions)
			- They are the behaviors on the data members to process them
			- Methods will define logic for processing
			- Class with encapsulate Logic and its processed outoput will be returned to other method within class and/or outside of the class 
		- Instance
			- Real-Word representation of the class
			- The Memory for class will be allocated when an instance is created
			- The instance contains 'defaults' for data members
				- e.g. for 'int' data member the defaultr will be 0 or the value set bt during declaration
			- The class will be in action (in-use) is possible only after an instance is created, otherwise the application will crash
		- Access Specifiers in .NET for C#
			- public
				- Members is accessible within and outisde the class
			- private
				- Members are accessible only within the class
				- Default to all members of the class
			- protected
				- Members are accessible within class and in derived class
			- internal
				- Members are accessible with the containing namespace. The namespace in which class is declared
				- Default to class 
			- protected internal
				- Members are accessible within the class, in the derived class of same namespace and derived class of other namespace
		- The 'this' concept
			- All Class members are accessed within the class using the 'this' object
			- The 'this' is the class scope (instance) itself within the class
		- Class Members
			- Variable
			- Methods
			- Constructor
			- Properties
				- Get/Set properties
				- They are public method blocks to Read (Get) and Write (Set) values for private members of the class
			- Event
	- To make sure that the method for class work or executes successfully, handle exception
		- The 'exception' is a mechanism using which 'SOME MEANINGFUL' result is returned or provided to the called when an execution is failed because of 'SOME UNCERTAINANITY'
		- Syntax:
			- try {..... THE CODE TO BE EXECUTED.....} catch(Exception ex){...THE CODE TO BE  EXECUTED IF CODE IN TRY IS FAILED TO EXECUTE.........} finally {.....THE CODE THAT WILL ALWAYS BE EXECUTED IRRESPECTIVE OF try BLOCK OR catch BLOCK............}
			- try 
			{
			   .......
			}
			catch(Exception ex) 
			{
				..........
			}
			finally
			{
			  ........
			}
		- The 'Exception', the Top-most class for all Exceptions
			- The 'Message' proeprty will contain the Error Detail occured during an execution of 'try' block 
		- To Throw and handle exception conditinally, use the 'throw' keyword
			- if(CONDITION)
			{
			   throw new Exception("MESSAGE");
			}
			- The thrown excpetion is also habdled by 'catch' block 
- Class definition Strategies
	- Class used only for Storing Data for Read/Write Operations MUST have only 'public properties'
		- These classes as known as Data Clases aka Entities
		- Public properties are used for Performing Read/Write operations on Private Data Members
		- Auto-Implemented Properties introduced in C# 3.0
			- Access_Specifier ReturnType PROEPRTY-NAME {get;set;}
			- The private member aka 'BAcking-Field' will be defined by CLS
	- If the class used to define Business Logic aka Domain Logic then it will contian methods with required Access Specifiers 
	- Guidelines for Class Creation
		- Start Design using Abstract class
			- Design Standard that will be followed by add Class Derivations aka Inheritance	
			- Use Inheritance when a specific-type of logical funcationality is to be implemented for the application
				- e.g. Employee Management System
					- Employee Base Class can have following derivations
						- FullTime, Base Type
							- Manager
							- Engineer
							- Clerk
						- Consultant
						- DailyWages
			- The Inheritance provided Following Features in Application Development
				- Uses the Base Type Public/Protected Properties as-it-is
				- The Derived Type can additionaly add extra properties and behavior
					- AKA 'Decorattion'
		- (Observation)
			- Since the 'Object' is highest-level DataType in .NET, each type 'is of the type object' and then it has an access to public methods of the 'Object' class
			- No Multiple Inheritence allowed in .NET 
				- No Multiple Parents are allowed for the class
			- Using the 'base' keyword, the 'protected' member of the base class can be accessbile in derived class
			- Within the namespace the 'internal' member of the class is accessible

		- (Critical Observations)

			- Overloading: Having Multiple methods  with same name but differnt in any of the following in Same class or Base and derived classes
				- Number of Parameters
				- Type of parameters
				- Order of Parameters
			- What if the Base class and Derived class has 'Same method name with Same Signeture'? 

				- If a System has multiple classes with common functionalities in more than two classes then add the common functionality in base classs and extend the base classs by derived classes

					- If the Base class is a Template Functionality for all derived classes, then we need not to instantiate it, so make it as 'abstract' class using 'abstract' access modifier.

				- If any of the derive class wants to extend a behavior of the base class method, then make sure that the base class method must be set the access modifier as 'virtual'.

				- METHOD OVERRIDING (Polymorphism)
					- The class that wants to extend the method will override it using 'override' access modifier on the method of the derived class and write new implementation for it.
				- If the all derive classes wants to define complete 'new implementation' for the matching method of the abstract base class, then do not provide any implementation for the method of abstract base class, just make the method as 'abstract' method 
					- all derive classed MUST OVERRIDE all abstract method of the basse class else make the derive class as 'abstract'
			
				- METHOD SHADOWING (Polymorphism)
					- What if the derived class does not want to override the method of the base class but instead, wants to define a complete new implementation to method from the derive class?  
						- Use the Method Shadowing by using 'new' access modifier definition for the method of the derived class
		- The Sealed class
			- The class that cannot be inherited
			- Use the 'sealed' access modifier
- Interfaces	
	- it is a type in ,NET programming that is used for following
		- Establish Communication across the Objects Horizontaly
		- It contains method definition that can be inplemented by each class with their own requirements of the logic
			- Like Abstract Methods of Abstract class
	- Abstract Class Vs Intercace
		- Abstract class is mainly used to define Implementation standard within a namespace for all classed deribed from Abstract class
		- Verticle search or instance casting is fastest in a namespace while using Abstract classs
		- Interfaces are more useful to establish horizontaal communication between objects in Inter-system communication
		- Interfaces does not have any metho implementation (by default) (NOTE: Provided from C# 8.0)
		- Rule: When a class implement an interface, all methods of the interface MUST be implemented by the class
		- A Class can implement Multiple interfaces be can have only one parent/Base class
		- (IMP***)An interface can be Implicitely Implemenetd or Explicitely implemented by a class 
			- A Polymorphism using interface
	- Implicit Implementation Vs Explicit Implementation
		- Implicit Implementation: The class is Owner of methods from Interface. All methods are accessed using an instance of the class as well as using the Interface Reference 
		- Explicit Implementation
			- Although methods from interface are physically implemented by class still those methods are owned by the intarface
			- These methods are accessed using Interface Reference of which instance is created by the class
	- Facts or Observations
		- One class can implement Multiple Interfaces
		- If these interfaces are having same signeture with same name then the class MUST implement them Explicitely
		- Interfaces are not for "MULTIPLE INHERITANCE"
# Using the Delegates and Events
	- Delegate
		- A .NET Type that is used to invoke a method with its reference and execute it (Fresher's Definition')
			- Same as Pointer-to-function in C,C++
		- The 'System.Delegate' is type in CTS and the keyword is 'delegate'
		- To execute a method using delegate the signeture of the method MUST match with Signeture of the delegate
		- Define a Delegate at Namespace level sothat it can be used by all Classes under the namespace
	- Observations on Delegates
		- Since a Delegate contains the Method reference, we can directly pass the method implementation to the delegate without creating any 'Named-Method'
			- Anonymous Method in C# 2.0
				- The Implementations passed to delegate will be directly converted into Binary and executed (Better for performance)
				- E.g.
					- handler = delegate (int x, int y) { return x + y; };
					- Operand Tree
						- x,y
					- Operator Tree
						- +
					- Expression Tree for Evaluation in Binary Form
						- x + y
		- What if there exists a Method that accepts an input parameter as Delegate?
			- e.g.
				- void Process(ProcessHandler handler){......}
			- C# 2.0 To Such Method we can pass the delegate that has anonymous method implementation
				- e.g.
					- handler = delegate (int x, int y) { return x + y; };
					- Process(handler);
			- C# 2.0 To Such Method we can direcly pass the Anonymous Method  
				- e.g.	
					-   Process(delegate (int a,int b) { return a * b; });
			- C# 3.0 To Such method we can pass a very simple syntax as 'Lambda Expression'
				- e.g.
					- Process((int x,int y) => { return x * x * y * y; });
					- The Entire Lambda Expreassion will be directly Compiled and executed into Binary(Best for Perfromance) 
			- NOTE****
				- If a method accepts delegate as input parameter then to that method we can pass Lambda Expression

		- Used for establishing communication across Objects (Advanced-Definition)
		- Used for defining an Event to establish Communciation across objects (Advanced-Definition)
			- The Event is used for 'Actoin-Based-Programming'
			- Some Action Has to take place so that a Notification is generated (aka Event)
			- An Event is a Special Type of Delegate, that is Raised when an action is taken place that will trigger and event to notify 
			- The delegate that is used to define an event MUST have a return type as 'void'

		- Steps for Working with Events
			- Define a delegate that has return type as 'void'
			- Define event using the delegate inside the class (Logic / Domain class) that will be generating notifications
			- Define a NotificationListener class, this class will be responsible for listening to events raised by the domain class
			- Client class that will call the domain class for transactions as well as will subscribe to the Notification Listener class so that the Notifcations are received

		- Next Level
			- Used for Threading in .NET
			- Used for Asynchronous Programming in .NET
# C# 3.0
	- All Chganges are done by Microsoft for Supporting Language Integrated Query aka LINQ
		- The 'var' declaration
			- used for defining Local variables in a method
			- the 'var' must be initialized
			- the typof of var declaration will be set based on the Left-Hand-Side initial value
			- one the 'var' declaration is initialized, we cannot assign differnt type parameter to it
		- Auto-Implemented properties
		- Lambda Expression
		- Extension Methods
			- They are an extended funcationalities added into the 'Standard CLR classes' as well as 'Custom Defined Sealed classes' without inheritance or modifiying the code of existing class 
			- Advantages
				- We can easily add an enhanced fucntionality as per the requirements in an existing class
				- No derivation is needed
				- No code changes are required
				- Improve speed of application development by adding new functionality in an existing application without stopping the existing 'under-use' application
			- Rules
				- The class that contains extension methods MUST be 'static'
				- The method to be used as ecxtension method MUST ne  'static'
				- The first parameter of this method MUST be 'this' referred reference of the 'class' or 'interface' for which we are adding the current method as extension method
				- e.g.
					- the sealed class as
						- public sealed class MyClass{.......}
					- Writing an extension method
						public static class MyExtension 
						{
							public static void MyExtensionMethod(this MyClass obj, int x,int y,....  )
							{
							
							}
						}
					- We can access the MyExtensionMethod() using an instance of the MyClass class
						- MyClass obj = new MyClass();
						- obj.MyExtensionMethod(x,y,....);
		- Object and Collection Initializers
		- Expression Tree

	- Special Data Structure declarations
		- Tuples (C# 7.0)
		- Records (C# 9.0)
- To view an Assembly with IL and MetaInfo use 'Ildasm.exe' tool
	- Intermidiate Language Dis-Asssembler
	- This tool will be installed as Microsfot SDK in Windows OS
		- C:\Program Files (x86)\Microsoft SDKs\Windows\v10.0A\bin\NETFX 4.8 Tools
- The foreach..loop can be used only for those types who implements IEnumerable Interface
