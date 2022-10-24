# 1.0 Data Types & Data Structures
<br>


## 1.1 Numbers: Integers and Floating Point Number(Floats)
```
Integers: ...,-2,-1,0,1,2,...

Floats: any number with a decimal point: 1.2 , 3.22222, 2.0
```

### 1.1.0 Integers in Loops(the Code is not important, just pay attention to the concept)
```
// program to display text 5 times
const n = 5;

// looping from i = 1 to 5
for (let i = 1; i <= n; i++) {
    console.log(`I love JavaScript.`);
}// program to display text 5 times
const n = 5;

// looping from i = 1 to 5
for (let i = 1; i <= n; i++) {
    console.log(`I love JavaScript.`);
}
```

## 1.2 Strings
```
"this is a string"

"string"

"s"
```

## 1.3 Arrays
```
In programming they keep an ordered list of different data for us.

For example, if there was a race we can keep the name of the participants in order of completing the race in an array.

['Jim', 'Peter', 'George']
```
## 1.4 Objects

```
It keeps information for us but there us no order:

Example:

const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```
##
##
##
##
<br>

# 2.0 What Is An Algorithm?
<br>
<br>

An algorithm is a set of step-by-step procedures, or a set of rules to follow, for completing a specific task or solving a particular problem. 
<br>
<br>
<br>

Here’s what baking a cake might look like, written out as a list of instructions, just like an algorithm:
<br>
<br>
<br>


Preheat the oven<br>

Gather the ingredients<br>

Measure out the ingredients<br>

Mix together the ingredients to make the batter<br>

Grease a pan<br>

Pour the batter into the pan<br>

Put the pan in the oven<br>

Set a timer<br>

When the timer goes off, take the pan out of the oven<br>
<br>

##

### 2.0.1 Example: Find the largest number among three numbers
```
Step 1: Start
Step 2: Declare variables a,b and c.
Step 3: Read variables a,b and c.
Step 4: If a > b
           If a > c
              Display a is the largest number.
           Else
              Display c is the largest number.
        Else
           If b > c
              Display b is the largest number.
           Else
              Display c is the greatest number.  
Step 5: Stop
```

### 2.0.2 Check whether a number is prime or not
```
Step 1: Start
Step 2: Declare variables n, i, flag.
Step 3: Initialize variables
        flag ← 1
        i ← 2  
Step 4: Read n from the user.
Step 5: Repeat the steps until i=(n/2)
     5.1 If remainder of n÷i equals 0
            flag ← 0
            Go to step 6
     5.2 i ← i+1
Step 6: If flag = 0
           Display n is not prime
        else
           Display n is prime
Step 7: Stop 
```

## 2.1 Why is it important? 
<br>

### Beside of being the backbone of programming, algorithms give you a way of thinking.
<br>

Defining the problem clearly<br>

Breaking the problem down into small, simple parts<br>

Define the solution for each part of the problem<br>

Implementing the solution<br>

Making it efficient (eventually)<br>
##
##
##
##
### Starting from next week, I will send one or two logical problems on slack for you to solve every week. You do not require to send me the solution for these problems.
### Do not look up for the answer on Google and just try to solve it yourself. This is the way of honing your logical thinking skill. 
### Also, I will send whenever I can an example of an algorithm for you to read and reflect on.


