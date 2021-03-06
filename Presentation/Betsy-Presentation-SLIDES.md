CUNY SPS DATA 606 Presentation

========================================================
author: Betsy Rosalen
date: March 7, 2018
autosize: true

OpenIntro Statistics - Third Edition<br>
[openintro.org](openintro.org)

Chapter 3 - Distributions of Random Variables

Exercise 3.37 - Exploring combinations

Deriving the formula for the number of ways to arrange n objects
========================================================

The formula for the number of ways to arrange n objects is $n! = n \times (n − 1) \times · · · \times 2 \times 1$.  

This exercise walks you through the derivation of this formula for a couple of special cases.

Scenario
========================================================

A small company has five employees: Anna, Ben, Carl, Damian, and Eddy. There are five
parking spots in a row at the company, none of which are assigned, and each day the employees
pull into a random parking spot. That is, all possible orderings of the cars in the row of spots are
equally likely.

Question 1
========================================================

On a given day, what is the probability that the employees park in alphabetical order?

Let's number the spots to make this easier.  
========================================================

If we numbered the spots from 1 to 5 this is the parking order that we want to determine the probability for...

Spot | Employee
--- | ---
1 | Anna
2 | Ben
3 | Carl
4 | Damian
5 | Eddy

So we are trying to find:
========================================================

$$P(\text{A in 1,  and  B in 2,  and  C in 3,  and  D in 4,  and  E in 5})$$

Probabilities for each car...
========================================================

The first employee to arrive has a 1 in 5 or $\frac{1}{5}$ chance of parking in the correct spot.  

As each of the next 4 employees arrive the probability of them parking in the correct spot to get an alphabetical parking order is reduced by one spot each time, and in each case there is only 1 spot that would satisfy the condition of alphabetical order.  

So the next employee to arrive has a $\frac{1}{4}$ chance of parking in the correct spot, 

the next a $\frac{1}{3}$ chance, 

the next a $\frac{1}{2}$ chance, 

and the last employee to arrive has a $\frac{1}{1}$ chance.

Multiplication Rule for independent processes
========================================================

Since knowing where each person parked does not affect the probability of each successive person parking in the correct spot, these are independent events and we can use the Multiplication Rule for independent processes to get the probability of all 5 events occurring.

$$\frac{1}{5} \times \frac{1}{4} \times \frac{1}{3} \times \frac{1}{2} \times \frac{1}{1} = \frac{1}{120}$$

**Note:**  The denominator in the equation above is $5!$

Question 2
========================================================

If the alphabetical order has an equal chance of occurring relative to all other possible orderings, how many ways must there be to arrange the five cars?

Deriving 5!
========================================================

If each parking order has an *equal* $\frac{1}{120}$ chance of occurring 

AND 

we know that all possible outcomes must add to a total probability of 1 

THEN 

there must be 120 possible orderings since $120 \times \frac{1}{120} = 1$.  

In other words, there are $5!$ ways of arranging the 5 cars.

Question 3
========================================================

Now consider a sample of 8 employees instead. How many possible ways are there to order these 8 employees’ cars?

Confirming our logic
========================================================

Using the same logic if there are 8 employees the probabilities of each one successively parking in the correct spot are:

$$\frac{1}{8} \times \frac{1}{7} \times \frac{1}{6} \times \frac{1}{5} \times \frac{1}{4} \times \frac{1}{3} \times \frac{1}{2} \times \frac{1}{1} = \frac{1}{40\text,320}$$


```r
# Just to confirm the multiplication...
8*7*6*5*4*3*2*1
```

```
[1] 40320
```

Conclusion
========================================================

So as in the earlier example with 5 cars, if each possible ordering has an equal probability of occurring then there must be $40\text,320$ or $8!$ ways of ordering the 8 cars.

We can conclude that for $n$ objects there are $n!$ ways of ordering them.

Of course the easy way to calculate this in R is...


```r
factorial(8)
```

```
[1] 40320
```
