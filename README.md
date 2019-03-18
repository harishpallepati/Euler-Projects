# Euler-Projects

### Question 1: 
Consider a row of n dice all showing 1.
First turn every second die,(2,4,6,…), so that the number showing is increased by 1. Then turn every third die. The sixth die will now show a 3. 
Then turn every fourth die and so on until every nth die (only the last die) is turned. If the die to be turned is showing a 6 then it is changed to show a 1.

Let f(n) be the number of dice that are showing a 1 when the process finishes. You are given f(100)=2 and f(10^8)=69.
Find f(10^36).

### Mathematical Analysis: 
This is very interesting problem, the underlying concepts behind this problem is number theory(esp factors and sequences).

Let's look into the first 100 numbers to get a good idea of the problem.

Step 1: Every number on the dice is 1 at the beginnig i.e 1,1,1,1,1,1,1,1,1,1,1....
Step 2: After first iteration of increasing every second dice the series turns out to be 1,2,1,2,1,2,1,2,1,2....
Step 3: With the third iteration of increasing every third dice the series will be 1,2,3,1,2,3,1,2,3....
.
.
.
the process goes on the same way when the number is 6 and it has to increased in the next iteration, we would flip that to 1 and 
follow along the process.

Note 1: To have 1's at the completion of the process, the dice should have been turned at a multiple of 6 times. So, when does this heappen?
when the number has factors as 1,7,13...of the form 6n+1

Note 2: as we have seen above the number of factors should odd, so that means the number should a perfect square(because only perfect squares
                                                                                                                   have odd number of factors)
                                                                                                                   
So, in f(100) we have a total of 11 squares i.e 1,4,9,16,25,36,49,64,81,100  
Among them only 36 and 64 have 7 factors.(Note: Number on the first die is excluded in our counting)  

### Question 2: 
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Find the sum of all the multiples of 3 or 5 below 1000.

### Mathematical Analysis:
Multiples of 3 below 1000 are 3,6,9,12,15...........996,999
Multiples of 5 below 1000 are 5,10,15.............995

If we sum all the multiples of both of them, we would include the multiples of 15 twice in our result.
So, subtracting once the multiples of 15 does the job!!

_-> (3+6+9+12+........) + (5+10+15+20+.....) - (15+30+45.........)_
#### 233168
