# Booleans

![Yoda](http://i.imgur.com/CoqXZyO.png?1)

> Already know you that which you need. -[Yoda](https://en.wikipedia.org/wiki/Yoda)

## Learning Objectives

* Explain that the `Bool` is a data type where the value can only be **true** or **false**.
* Create variables using the Boolean literal values, `true` or `false`
* Explain and use all the various comparison operators:
	* Equal to (a == b)
	* Not equal to (a != b)
	* Greater than (a > b)
	* Less than (a < b)
	* Greater than or equal to (a >= b)
	* Less than or equal to (a <= b)
* Explain and use all of the various logical operators:
	* Logical NOT (!a)
	* Logical AND (a && b)
	* Logical OR (a || b)


## Boolean Type
Boolean is a fancy term meaning something that is either true or false.  While numbers and math form the backbone of any piece of software, everything (and I do mean everything) in computers, software and microchips, breaks down to ones and zeros, true and false.  While it isn't important to understand why that is and how exactly it works, it is important to understand how boolean expressions work so that your code will be able to do something interesting like this:

````Swift
let name = "Luke"
let age = 34
let lengthOfLightSaber = 32.5

// name is a constant of type String with a value of "Luke"
// age is a constant of type Int with a value of 34
// lengthOfLightSaber is a constant of type Double with a value of 32.5
````
But.. what if we want to declare a variable as being true or false (type Bool).

````Swift
let hasTheForce = true
// hasTheForce is a constant of type `Bool` with a value of true
````

Option clicking this constant in the playground file to see its type will show us this result:

![result](http://i.imgur.com/C5c1KTI.png?1)

Here is another example, except here we're creating a variable which will allow us to change the value.

````Swift
var isHungry = false
// isHungry is a variable of type Bool with a value of false

isHungry = true
// isHungry now has a value of true
````

Going with the example above, our program would like to know if isHungry is true or false and based upon that value, it will do something. If the person is hungry, it will feed them.. if not, it will do nothing.

Almost every program you write will need to take different courses of action based on boolean values, so it's important to have a really good grasp of what booleans and boolean expressions are as well as how to use them.

Swift recognizes a value as boolean if it sees ````true```` or ````false````.  You can implicitly declar a boolean variable ````let a = false```` or explicitly declare a boolean variable ````let i:Bool = true````.

````Swift
var a: Bool = true
// Explicitly declaring a variable called 'a' of type Bool to equal true

var b = false
// Implicitily delaring a variable called 'b' to equal false where 'b' is a variable
````

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
3 >= 4   // false
3 >= 3   // true
3 != 4   // true
3 != 3   // false
3  <= 4  // true
3 <= 3  // true
````

##Compound Comparison
All of the examples above have been simple expressions.  We can form complex boolean expressions, that is expressions which are the result of more than one comparison, with the logical operators "and" (&&) and "or" (||).  For example:

````Swift
(3 >= 3)  &&  (3 <= 4)   // true
(3 >= 3)  ||  (3 <= 4)   // true
(3 >= 3)  &&  (3 > 4)   // false
````
Here's another example:

````Swift
var providedPassword = true
var passedRetinaScan = false

providedPassword && passedRetinaScan  // false
providedPassword || passedRetinaScan // true


passedRetinaScan = true
providedPassword && passedRetinaScan // true
````

##Negation
You can use the "not" (!) operator to invert the value of any boolean value or expression.  Note that you can't have any space between the "!" and the value it's negating.  For example:

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
var fileExists = false
````
In our program, if ````fileExists```` is ````false````, we can show an alert to the user letting them know that ther eisn't a file and prompt them to look for another file.  If ````fileExists```` is ````true```` then we can continue on with our program and show the contents of the file to the user.
 

<a href='https://learn.co/lessons/Booleans' data-visibility='hidden'>View this lesson on Learn.co</a>

<p class='util--hide'>View <a href='https://learn.co/lessons/swift-booleans-readme'>Booleans and Operators</a> on Learn.co and start learning to code for free.</p>
