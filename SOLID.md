   									SOLID PRINCIPLE 


  - Problems ( which comes in real world )
    - Maintainibility.
    - Readability.
    - BUGS introduced. 

  - To Deal with these issues on long run, Robert C. martin creates some priciples - which combined called as SOLID principle 
                     
  				- S : Single Responsibility Principle ( SRP )
    				- O : Open - close Principle 
 				- L : Liskow Substitution Principle 
   				- I : Interface segregation principle.
				- D : Dependency Inversion Principle. 

	

  - S : SRP
  -- A class should have only one reason to change. 
  -- A class should do only one thing.

  ( Ek class ek responsibility handle kare - doesn't means ek class mai ek hih method ( this is not what it meant ) ).

  - O : Open - Close Priniciple
  -- A class should be open for extension but close for modification. 
  -- 




  - L : Liskov substitution principle 

	- Subclasses should be substitutable for their base classes.

	- koi bhi aesa client jo A class ko except krr rha hoh , magar mai glti se agar B ko refer kardu ... toh bhi code na fate. 
        - This same thing is also presented by Inheritance : which is it should extend the features of Base Class , never narrow down.

	- It seems simple : but the master said it is breaked mostly. 
	- Example : 
		Suppose we have a account : which have abstract method : deposit() withdraw() << Abstract >>
		and have two move classes Saving Acc ( is - a ) relation with account , also a current account. 

	- There is brute force , better ,best first principle screenshot. 


   - Guidlines for LSP: ( Broad - parent or ancestor && narrow - descendent )
 	1. Signature Rule : Suppose we have a parent and child class and here A -- > B ( inheritance ) .
				( method signature should be same : ( it should be equal or broader )  -- ss : 23: 48
	
	( Method Argument Rule )

	2. RETURN TYPE RULE : Covariance ( ki child class ka method ka return type either parent ke return type ke equal hoga otherwise its narrower version. 

	3. EXCEPTION RULE : Parent class ki base exception ko throw karde , or uski narrow ko. but never broader one .

	.... bunch more guidlines. 



	

    - INTERFACE SEGREGATION PRINCIPLE 

	- Many Client Specific Interface are better then one general purpose interface. 
	- Client should not be forced to implement methods they don't need. 
		
	
	Suppose we have a parent class : Shape  and it has multiple child class which are square and rectangle in all these places , we need to override the area() methods. 
 	now , let suppose i need to make a new child Cube ... which inheriets and override the area method but it has volume method too. so , when i introducs more of these clas	sses so, i should make the Shape class <<abstract >> and put volume over there. 

 	- But here we are looking at a problem , which is shapes like square and rectange doesn't have volume . but i need to put these method in the squrare and so one. 
	  and throw exception. 
	
	now, recall many client specific interface are better and client should not be forced to implement methods they don't need. 
	we should have done : made one 2-D shape and 3-D shape abstract class and then made child classes sqare and rectange are extending the 2-D one ...
	and the volume followers must inherit 3-D. 



     - DEPENDENCY INVERION PRINCIPLE 
	
	- High Level Module Shold not depend on Low level module but rather both should depend on abstraction. 
	- Har voh module that deals with business logic. 
 	- har voh moduel jo file system, network logic se deal kare. 

	- There should be an intermediate layer between them. 
	example : APPLICATION ( HLM )                     SQL DB 
		  sqlDB sd;				  MONGO DB 
		  
	- Lets introduce a persistance class. 




 	- Always remeber : These are Principles not Laws . which means they are followed upto 100% mark in all senario that not required as well as possible. ( it comes with 
		trade off with business logic ) or something else.
 




















 
