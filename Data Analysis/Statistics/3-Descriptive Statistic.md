### Notation 
```
Common Math Language use to Communicate
```

```
Notation
Notation is a common language used to communicate mathematical ideas. Think of notation as a universal language used by academic and industry professionals to convey mathematical ideas. In the next videos, you might see things that seem confusing. Use the quizzes to assist with your understanding of the concepts.

You likely already know some notation. Plus, minus, multiply, division, and equal signs all have mathematical symbols that you are likely familiar with. Each of these symbols replaces an idea for how numbers interact with one another. In the coming concepts, you will be introduced to some additional ideas related to notation. Though you will not need to use notation to complete the project, it does have the following properties:

Understanding how to correctly use notation makes you seem really smart. Knowing how to read and write in notation is like learning a new language. A language that is used to convey ideas associated with mathematics.


It allows you to read documentation, and implement an idea to your own problem. Notation is used to convey how problems are solved all the time. One really popular mathematical algorithm that is used to solve some of the world's most difficult problems is known as Gradient Boosting. The way that it solves problems is explained here: https://en.wikipedia.org/wiki/Gradient_boosting. If you really want to understand how this algorithm works, you need to be able to read and understand notation.


It makes ideas that are hard to say in words easier to convey. Sometimes we just don't have the right words to say. For those situations, I prefer to use notation to convey the message. Similar to the way an emoji or meme might convey a feeling better than words, notation can convey an idea better than words. Usually those ideas are related to mathematics, but I am not here to stifle your creativity.

Supporting Materials
Wikipedia on Gradient boosting.

```
--------------

```
Before Collecting Data
Before collecting data, we usually start with a question, or many questions, that we would like to answer. The purpose of data is to help us in answering these questions.

Random Variables
A random variable is a placeholder for the possible values of some process (mostly... the term 'some process' is a bit ambiguous). As was stated before, notation is useful in that it helps us take complex ideas and simplify (often to a single letter or single symbol). We see random variables represented by capital letters (X, Y, or Z are common ways to represent a random variable).

We might have the random variable X, which is a holder for the possible values of the amount of time someone spends on our site. Or the random variable Y, which is a holder for the possible values of whether or not an individual purchases a product.

X is 'a holder' of the values that could possibly occur for the amount of time spent on our website. Any number from 0 to infinity really.

```

### Question 

```
What type of variable is the random variable X in the video in the previous concept?



Quantitive Continuous
```


```
What type of variable is the random variable Y in the video in the previous concept?


Categorical Nominal 
```
### Capital vs. Lower Case Letters

```
Random variables are represented by capital letters. Once we observe an outcome of these random variables, we notate it as a lower case of the same letter.

Example 1
For example, the amount of time someone spends on our site is a random variable (we are not sure what the outcome will be for any particular visitor), and we would notate this with X. Then when the first person visits the website, if they spend 5 minutes, we have now observed this outcome of our random variable. We would notate any outcome as a lowercase letter with a subscript associated with the order that we observed the outcome.

If 5 individuals visit our website, the first spends 10 minutes, the second spends 20 minutes, the third spends 45 mins, the fourth spends 12 minutes, and the fifth spends 8 minutes; we can notate this problem in the following way:

X is the amount of time an individual spends on the website.

\bold{x_1}x 
1
​
  = 10,       \bold{x_2}x 
2
​
  = 20       \bold{x_3}x 
3
​
  = 45       \bold{x_4}x 
4
​
  = 12       \bold{x_5}x 
5
​
  = 8.

The capital X is associated with this idea of a random variable, while the observations of the random variable take on lowercase x values.

Example 2
Taking this one step further, we could ask:

What is the probability someone spends more than 20 minutes in our website?

In notation, we would write:

P(X > 20)?

Here P stands for probability, while the parentheses encompass the statement for which we would like to find the probability. Since X represents the amount of time spent on the website, this notation represents the probability the amount of time on the website is greater than 20.

We could find this in the above example by noticing that only one of the 5 observations exceeds 20. So, we would say there is a 1 (the 45) in 5 or 20% chance that an individual spends more than 20 minutes on our website (based on this dataset).

Example 3
If we asked: What is the probability of an individual spending 20 or more minutes on our website? We could notate this as:

P(X \geq≥ 20)?

We could then find this by noticing there are two out of the five individuals that spent 20 or more minutes on the website. So this probability is 2 out of 5 or 40%.



```

### Notation for Calculating the Mean
```
We know that the mean is calculated as the sum of all our values divided by the number of values in our dataset.

In our current notation, adding all of our values together can be extremely tedious. If we want to add 3 values of some random variable together, we would use the notation:

\bold{x_1} + \bold{x_2} + \bold{x_3}x 
1
​
 +x 
2
​
 +x 
3
​
 

If we want to add 6 values together, we would use the notation:

\bold{x_1} + \bold{x_2} + \bold{x_3} + \bold{x_4} + \bold{x_5} + \bold{x_6}x 
1
​
 +x 
2
​
 +x 
3
​
 +x 
4
​
 +x 
5
​
 +x 
6
​
 

To extend this to add one hundred, one thousand, or one million values would be ridiculous! How can we make this easier to communicate?!
```

### Aggregations

```
An aggregation is a way to turn multiple numbers into fewer numbers (commonly one number).

Summation is a common aggregation. The notation used to sum our values is a greek symbol called sigma \SigmaΣ.

Example 1
Imagine we are looking at the amount of time individuals spend on our website. We collect data from nine individuals:

\bold{x_1}x 
1
​
  = 10,       \bold{x_2}x 
2
​
  = 20       \bold{x_3}x 
3
​
  = 45       \bold{x_4}x 
4
​
  = 12       \bold{x_5}x 
5
​
  = 8       \bold{x_6}x 
6
​
  = 12,       \bold{x_7}x 
7
​
  = 3       \bold{x_8}x 
8
​
  = 68       \bold{x_9}x 
9
​
  = 5

If we want to sum the first three values together in our previous notation, we write:

\bold{x_1} + \bold{x_2} + \bold{x_3}x 
1
​
 +x 
2
​
 +x 
3
​
 

In our new notation, we can write:

\sum\limits_{i = 1}^3 x_i 
i=1
∑
3
​
 x 
i
​
 .

Notice, our notation starts at the first observation (i=1i=1) and ends at 3 (the number at the top of our summation).

So all of the following are equal to one another:

\sum\limits_{i = 1}^3 x_i 
i=1
∑
3
​
 x 
i
​
  = \bold{x_1} + \bold{x_2} + \bold{x_3}x 
1
​
 +x 
2
​
 +x 
3
​
  = 10 + 20 + 45 = 75

Example 2
Now, imagine we want to sum the last three values together.

\bold{x_7} + \bold{x_8} + \bold{x_9}x 
7
​
 +x 
8
​
 +x 
9
​
 

In our new notation, we can write:

\sum\limits_{i = 7}^9 x_i 
i=7
∑
9
​
 x 
i
​
 .

Notice, our notation starts at the seventh observation (i=7i=7) and ends at 9 (the number at the top of our summation).

Other Aggregations
The \SigmaΣ sign is used for aggregating using summation, but we might choose to aggregate in other ways. Summing is one of the most common ways to need to aggregate. However, we might need to aggregate in alternative ways. If we wanted to multiply all of our values together we would use a product sign \PiΠ , capital Greek letter pi. The way we aggregate continuous values is with something known as integration (a common technique in calculus), which uses the following symbol \int∫ which is just a long s. We will not be using integrals or products for quizzes in this class, but you may see them in the future!

```
### Notation Recap


```
Notation is an essential tool for communicating mathematical ideas. We have introduced the fundamentals of notation in this lesson that will allow you to read, write, and communicate with others using your new skills!
```

### Notation and Random Variables
```
As a quick recap, capital letters signify random variables. When we look at individual instances of a particular random variable, we identify these as lowercase letters with subscripts attach themselves to each specific observation.

For example, we might have X be the amount of time an individual spends on our website. Our first visitor arrives and spends 10 minutes on our website, and we would say \bold{x_1}x 
1
​
  is 10 minutes.

We might imagine the random variables as columns in our dataset, while a particular value would be notated with the lower case letters.
```

