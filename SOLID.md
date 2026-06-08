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
































 
