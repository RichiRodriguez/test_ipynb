# Programming Assignment 1

## Polynomials - Using The ArrayList Class

### The Term Class  
Create a class to represent a term in an algebraic expression. As defined here, a term consists of the variable x, an integer coefficient, and a nonnegative integer exponent.  E.g.

* in the term $4x^2$, the coefficient is 4 and the exponent 2
* in $-6x^8$, the coefficient is -6 and the exponent 8

Your class will have a constructor that creates a Term object with a coefficient and exponent passed as parameters, and accessor methods that return the coefficient and the exponent, respectively. Your class will also override ```toString``` to return a Term in this general form:  
> ax^b	where a is the coefficient and b the exponent 

with these special cases:

| Case     |Returns|
|:--------:|:-----:|
| a=1      | x^b   |
| b=1      | ax    |
| b=0      | a     |
| a=1, b=1 | x     |

You may assume that the coefficient will not be zero.

### The Polynomial Class

A ___skeleton___ of the Polynomial class you are to use is on the class web site.  All you have to do is write the bodies of the methods.

👉 __To get credit for this assignment, your Polynomial class must use an ArrayList-of-Term as its principal data structure__ 

👉 __To get credit, you must not declare any additional instance variables or methods and must not modify any of the method declarations in any way (not necessary).__

As defined here, a polynomial is a sequence of terms.

Example:
1.  3x^2  +  4x^4  +  x6
2.  2  +  5x^2  +  6x^3  +  2x^7
3.  4x^10 

The terms of polynomial 1 are (3,2), (4,4) and (1,6).  
The terms of polynomial 2 are (2,0), (5,2), (6,3) and (2,7).  
The terms of polynomial 3 are  (4,10).  

Note that the Polynomial class has:
* A constructor that creates an empty Polynomial (a Polynomial with 0 terms)

* A method with signature  
  ```java
  public void addTerm(int coefficient, int exponent)
  ```  
  which creates a Term and places it in its proper position in the Polynomial  
  
  
   👉 __The terms of the Polynomial are stored in ascending order by exponent (see above) so you never have to “sort” the list.  Terms with the same exponent may be stored in any order but will appear after all terms with lesser exponents and before all terms with greater exponents__  
   
* A method with signature  
  ```java
  public Polynomial polyAdd(Polynomial p)
  ```  
  which adds Polynomial _p_ to __this__ Polynomial and returns the sum  
  
* A method with signature  
  ```java
  public Polynomial polyMultiply(Polynomial p)
  ```
  which multiplies __this__ Polynomial by _p_ and returns the product  
  
* An overridden ```toString``` method that returns a String representation of a polynomial as a sum of terms. For example, polynomial 1 above would have this String representation:  
      3x^2 + 4x^4 + x^6

* A private method with signature  
  ```java
  private void collectTerms()
  ```
  which “collects” like terms of __this__ Polynomial. For example:  
	  Before:	x^2 + 3x^2 + 2x^2 + 3x^3 + 5x^4 + 2x^4  
	  After: 	6x^2 + 3x^3 + 7x^4  
  👉 Polynomials must always be printed with terms collected  
  
  ### The Test Class

Test class ```PolynomialTester.java``` is available online.  Make no changes to the test class.

### Javadoc Comments

Make sure you properly document the Polynomial and Term classes and all public methods, including all parameters, and all return statements.  Then run the javadoc utility to generate the “help” pages (Polynomial.html and Term.html). 

  👉 For this assignment, the Javadoc comments and html files will count as a separate grade!


### What To Upload To Moodle

Upload a zip file containing your NetBeans project folder and the output  

  👉 See the “Submitting Your Assignments” document online
  

### Due Date

Due Date – Tuesday, January 30th


### Helpful Hints! Divide And Conquer!

1.	Begin by coding the Term class and the Polynomial methods addTerm and toString. For now, have addTerm simply add each new Term at the end of the list.  This will enable you to run the program and verify that your Term class is correct and that new Terms are indeed being added to the list. 

2.	Code the polyAdd and polyMultiply methods. These are fairly straightforward and once completed, along with the temporary version of addTerm, you will have a majority of the credit in the bank. 

3.	After doing the above, modify the addTerm method so that each new Term is inserted in its proper place in the list. An algorithm will be discussed in class. Note that none of the other methods will need to be modified in any way. More credit in the bank.

4.	Lastly, code the collectTerms method.  An algorithm will be discussed in class.

### Other Considerations

Also make sure your classes contain proper internal documentation and meet all the style considerations discussed in class and online in Unit 1.
