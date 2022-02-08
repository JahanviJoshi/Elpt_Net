# Date: 18-Jan-2022 (Show me on 19-Jan-2022)
1. Create a Console Project. IN thie project in the 'Program class', add following method
	- Add()
		- Accept 2 Integers from the Main() method and return integer as addition of 2 numbers
	- Sub()
		- For Subscration
	- Multiplication()
		- For Multiplication
	- Division()
		- For Division
	- Square()
		- For Square
2. While Performing all of the above operations make sure that each method will conditionbal statement for the following
	- If parameters to these statements are <= 0, then direcly return 0
3. Create a Method that will accept 3 Parameters as below
	- e.g.
		- static void Process(int a,int b,string c)
			- If c == "Add", then return addition of paarmeters
			- If c == "Sub", then return Substratcion  of paarmeters
			- If c == "Mult", then return Multiplication  of paarmeters
			- if c == "Div", then return division  of paarmeters
		- MAke sure that, a dn b are not negative or 0

4. Self-Study
	- Learn the Math class and try out the Trignometric methods

# Date: 31-Jan-2022
5. Using the Following String
	"James Bond is a fictional character created by novelist Ian Fleming in 1953. A British secret agent working for MI6 under the codename 007, he has been portrayed on film by actors Sean Connery, David Niven, George Lazenby, Roger Moore, Timothy Dalton, Pierce Brosnan and Daniel Craig in twenty-seven productions. All but two films were made by Eon Productions, which now holds the adaptation rights to all of Fleming's Bond novels.[1][2]

In 1961, producers Albert R. Broccoli and Harry Saltzman purchased the filming rights to Fleming's novels.[3] They founded Eon Productions and, with financial backing by United Artists, produced Dr. No, directed by Terence Young and featuring Connery as Bond.[4] Following its release in 1962, Broccoli and Saltzman created the holding company Danjaq to ensure future productions in the James Bond film series.[5] The series currently has twenty-five films, with the most recent, No Time to Die, released in September 2021. With a combined gross of nearly $7 billion to date, it is the fifth-highest-grossing film series.[6] Accounting for inflation, it has earned over $14 billion at current prices.[a] The films have won five Academy Awards: for Sound Effects (now Sound Editing) in Goldfinger (at the 37th Awards), to John Stears for Visual Effects in Thunderball (at the 38th Awards), to Per Hallberg and Karen Baker Landers for Sound Editing, to Adele and Paul Epworth for Original Song in Skyfall (at the 85th Awards) and to Sam Smith and Jimmy Napes for Original Song in Spectre (at the 88th Awards). Several of the songs produced for the films have been nominated for Academy Awards for Original Song, including Paul McCartney's "Live and Let Die", Carly Simon's "Nobody Does It Better" and Sheena Easton's "For Your Eyes Only". In 1982 Albert R. Broccoli received the Irving G. Thalberg Memorial Award.[8]"

- Perform Following Operations on the string. Use 'switch..case' constructs
	1. Find out number of 'Blank Spaces' in the string
	2. Find out nunmber of 'Words'
	3. Find out number of '.'
	4. Find out number of statements
	5. Find out number of digits
	6. Find out number of vowels (a,e,i,o,u)
	7. Find out number of 'the', 'is', 'to', 'and' and their positions (indexes)
	8. Find out number and positions of comma (,)
	9. Reverse each word in string
	10. Reverse entire string
	11. Print each statement in separate line on console from the above string
	12. Print all words decorated uasing "" e.g. "Live and Let Die"
	13. Convert first character of each word in upper case.
	15. List 'month names' from the above list e.g. January, February, etc.
- Evaluation will be done based on following criterias
	- Avoiding Code Repetation
	- Using most suoitable and applicable string standard method that will avoid unnecessary code


# Date: 01-Feb-2022 (a Mini Project Final Date of Submission is 04-Feb-2022 (Friday))

1. Modify the EmployeeOperations class with Following Method
	- UpdateEmployee(EmpNo, Employee)
		- Search Employee By EmpNo, if Employee not found then throw Employee Not Found Exception, else Update the existing Employee from the List based on the Employee object passed to the method	  
	- DeleteEmployee(EmpNo)
		- Search Employee By EmpNo, if Employee not found then throw Employee Not Found Exception, else Delete the existing Employee from the List
	- While Storing Employee Create a Seperate Dictionary to Store Employee by DeptName
	- Add a method to List Employees by DeptName
	- Add a method to List Employees by Designation
	- Write a method to Validate Employee before Add and Update based on following  Rules
		- EmpNo
			- Must be Positive Integer
			- Must not be repeated
		- EmpName
			- Must start from Uppercase Charachetr
			- Can have Blank Spaces but not Number and special Characters
			- Note: Use Regular Express (Search on Regx class (Self-Study))
		- DeptName can be any of the following
			- IT, HRD, Sales, Admin, Account
		- Designation Can be any of the following
			- Manager, Engineer, Clerk, Staff
		- Salary MUST be positive Integer	
2. Add a new class known as 'Client' that will be used by Main() method to perform Employee operations
	- The Main() method will not directly access Employee and EmployeeOperations classes 
	- The Client class Must contain method for
		- AddEmployee()
			- Access Method AddEmployee() from the EmployeeOperations
		- UpdateEmployee()
		- DeleteEmployee()
		- SearchEmployee()
3. All Operations on Employee will be done using Swich...case statements 
		
# Date: 02-Feb-2022
1. Can overloading is possible by having same method name with same number and order of parameters but different in return type?
2. Can we override the private virtual method of abstract class using public method from the deriuved class?
3. Can we have private and protected abstract and virtual methods in abstract base class?
4. Can we have method overloading across base and deried classe?
5. Can we type cast the derived class instance using the base class? 
6. Can we have public property in abstract base class?
7. Can we have same property in base and derived class?
8. Can we derive a public class from internal class?
9. Can we have internal virtual or abstract methods in abstract class?
10. Can we have private or protect class?
11. Can we have internal property?
12. Can we have virtual method in not-abstract class?
13. Can we have abstract method in not-abstract class?
14. What will happen if the derive class dows not override all abstract methods of the abstract class?
15. Can we have virtual and/or abstract methods in sealed class
16. Can we have sealed access modifier for method?

# Date: 04-Feb-2022

1. Add following methods in the Standard Math class as extension methods
	- GetPower(int x,int y); 
		- Must return x raised to y
	- Factorialofn(int n)
		- Must return factorial of n
	- CubeRootn(int n)
		- Must return Cube root of n
2. Chek if we can have 'static' constructor in class, if yes tehn how many times it is executed?

# Date: 08-Feb-2022
Complete Pending Assignments
1. Read about LINQ from docs.microsaoft.com
	- Take, Skip, OrderBy, OrderByDesc, etc
2. Read about Anonymous Type
