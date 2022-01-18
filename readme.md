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

# C# String
	- Array of Characters
		- Using '+' sign to Concat the String
	- By default string is a class that has verious methods
