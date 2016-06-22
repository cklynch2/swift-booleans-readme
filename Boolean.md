##Boolean Type
Boolean is a fancy term meaning something that is either true or false.  While numbers and math form the backbone of any piece of software, everything (and I do mean everything) in computers, software and microchips, breaks down to ones and zeros, true and false.  While it isn't important to understand why that is and how exactly it works, it is important to understand how boolean expressions work so that your code will be able to do something interesting like this:

````Swift
func finishCourse() {
    if gradeIsPassing() {
    	print("Hooray!")
   } else {
      print("Doh!")
   }
}
````

The ````gradeIsPassing()```` function takes one course of action if a true value is returned and a different course of action if a false value is returned.
Almost every program you write will need to take different courses of action based on boolean values, so it's important to have a really good grasp of what booleans and boolean expressions are as well as how to use them.

Swift recognizes a value as boolean if it sees ````true```` or ````false````.  You can implicitly declar a boolean variable ````let a = false```` or explicitly declare a boolean variable ````let i:Bool = true````.

##Comparison
The three main comparisons are "greater than" (>), "less than" (<), and "equals" (==).  For exampe:

````Swift
3 > 1    (true)
3 < 1    (false)
3 == 1   (false)
3 == 3   (true)
````
There is a special operator "not" (!) which is kind of like mathematical sarcasm (e.g. "Just Bieber is cool...  Not!).  These operators can be combined to create three additional operators "greater than or equals" (>=), "less than or equals" (<=), and "not equals" (!=):

````Swift
3 >= 4   (false)
3 >= 3   (true)
3 != 4   (true)
3 != 3   (false)
3  <= 4  (true)
3 <= 3  (true)
````

##Compound Comparison
All of the examples above have been simple expressions.  We can form complex boolean expressions, that is expressions which are the result of more than one comparison, with the logical operators "and" (&&) and "or" (||).  For example:

````Swift
(3 >= 3)  &&  (3 <= 4)   (true)
(3 >= 3)  ||  (3 <= 4)   (true)
(3 >= 3)  &&  (3 > 4)   (false)
````

##Negation
You can use the "not" (!) operator to invert the value of any boolean value or expression.  Not that you can't have any space between the "!" and the value it's negating.  For example:

````Swift
! true  (syntax error)
!true   (false)
!false   (true)
!(3 < 4)   (false)
!(3 > 4)   (true)
!((3 >= 3)  &&  (3 <= 4))   (false)
!((3 >= 3)  ||  (3 <= 4) )  (false)
!((3 >= 3)  &&  (3 > 4))   (true)
````

You can mix-and-match these operators in all kinds of different ways:

````Swift
(3 < 4)  &&  !(3 <= 4)   (false)
````

##Real World Usage
When it comes to "real world" programming boolean expressions are used to check conditions so that you know how to proceed and/or what kind of UI to provide.   For example:

````Swift
if !fileExists {
	showAlert("No such file")
	askForFileName()
} else {
	doRestOfTheProgram()
}
````


	
	


