# Python challenging programming exercises

## Forked from:
https://github.com/zhiwehu/Python-programming-exercises
## Description of Levels
Level 1	Beginner means someone who has just gone through an introductory Python course. He can solve some problems with 1 or 2 Python classes or functions. Normally, the answers could directly be found in the textbooks.

Level 2	Intermediate means someone who has just learned Python, but already has a relatively strong programming background from before. He should be able to solve problems which may involve 3 or 3 Python classes or functions. The answers cannot be directly be found in the textbooks.

Level 3	Advanced. He should use Python to solve more complex problem using more rich libraries functions and data structures and algorithms. He is supposed to solve the problem using several Python standard packages and advanced techniques.

## Problem Template
1. Question
2. Level
3. Hints
4. Solution

<details>
<summary><b>Question 1</b></summary>

### Question:
Write a program which will find all such numbers which are divisible by 7 but are not a multiple of 5,
between 2000 and 3200 (both included).
The numbers obtained should be printed in a comma-separated sequence on a single line.

### Level 1
### Hints:
Consider use range(#begin, #end) method

### Solution
<details>
<summary> See Solution </summary>

``` python
l=[]
for i in range(2000, 3201):
    if (i%7==0) and (i%5!=0):
        l.append(str(i))

print (','.join(l))
```
</details>
</details>

---

<details>
<summary><b>Question 2</b></summary>

### Question:
Write a program which can compute the factorial of a given numbers.
The results should be printed in a comma-separated sequence on a single line.
#### Example
Suppose the following input is supplied to the program: \
8 \
Then, the output should be: \
40320

### Level 1
### Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

### Solution
<details>
<summary> See Solution </summary>

``` python
def fact(x):
    if x == 0:
        return 1
    return x * fact(x - 1)

x=int(raw_input())
print (fact(x))
```
</details>
</details>

---

<details>
<summary><b>Question 3</b></summary>

### Question:
With a given integral number n, write a program to generate a dictionary that contains (i, i*i) such that is an integral number between 1 and n (both included). and then the program should print the dictionary.
#### Example
Suppose the following input is supplied to the program: \
8 \
Then, the output should be: \
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64}

### Level 1
### Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.
Consider use dict()

### Solution
<details>
<summary> See Solution </summary>

``` python
n=int(raw_input())
d=dict()
for i in range(1,n+1):
    d[i]=i*i

print (d)
```
</details>
</details>

---

<details>
<summary><b>Question 4</b></summary>

### Question:
Write a program which accepts a sequence of comma-separated numbers from console and generate a list and a tuple which contains every number.

#### Example
Suppose the following input is supplied to the program: \
34,67,55,33,12,98 \
Then, the output should be: \
['34', '67', '55', '33', '12', '98'] \
('34', '67', '55', '33', '12', '98')

### Level 1
### Hints:
In case of input data being supplied to the question, it should be assumed to be a console input. \
tuple() method can convert list to tuple

### Solution
<details>
<summary> See Solution </summary>

```python
values=raw_input()
l=values.split(",")
t=tuple(l)
print (l)
print (t)
```
</details>
</details>

---

<details>
<summary><b>Question 5</b></summary>

### Question:
Define a class which has at least two methods:
getString: to get a string from console input
printString: to print the string in upper case.
Also please include simple test function to test the class methods.

### Level 1
### Hints:
Use __init__ method to construct some parameters

### Solution
<details>
<summary> See Solution </summary>

``` python
class InputOutString(object):
    def __init__(self):
        self.s = ""

    def getString(self):
        self.s = raw_input()

    def printString(self):
        print self.s.upper()

strObj = InputOutString()
strObj.getString()
strObj.printString()
```
</details>
</details>

---

<details>
<summary><b>Question 6</b></summary>

### Question:
Write a program that calculates and prints the value according to the given formula:
Q = Square root of [(2 * C * D)/H]
Following are the fixed values of C and H:
C is 50. H is 30.
D is the variable whose values should be input to your program in a comma-separated sequence.

#### Example
Let us assume the following comma separated input sequence is given to the program: \
100,150,180 \
Then, the output should be: \
18,22,24

### Level 2
### Hints:
If the output received is in decimal form, it should be rounded off to its nearest value (for example, if the output received is 26.0, it should be printed as 26)
In case of input data being supplied to the question, it should be assumed to be a console input.

### Solution
<details>
<summary> See Solution </summary>

``` python
#!/usr/bin/env python
import math
c=50
h=30
value = []
items=[x for x in raw_input().split(',')]
for d in items:
    value.append(str(int(round(math.sqrt(2*c*float(d)/h)))))

print (','.join(value))
```
</details>
</details>

---

<details>
<summary><b>Question 7</b></summary>

### Question:
Write a program which takes 2 digits, X,Y as input and generates a 2-dimensional array. The element value in the i-th row and j-th column of the array should be i*j.
Note: i=0,1.., X-1; j=0,1,­Y-1.

#### Example
Let us assume the following comma separated input sequence is given to the program: \
3,5 \
Then, the output should be: \
[[0, 0, 0, 0, 0], [0, 1, 2, 3, 4], [0, 2, 4, 6, 8]]

### Level 2
### Hints:
Note: In case of input data being supplied to the question, it should be assumed to be a console input in a comma-separated form.

### Solution
<details>
<summary> See Solution </summary>

``` python
input_str = raw_input()
dimensions=[int(x) for x in input_str.split(',')]
rowNum=dimensions[0]
colNum=dimensions[1]
multilist = [[0 for col in range(colNum)] for row in range(rowNum)]

for row in range(rowNum):
    for col in range(colNum):
        multilist[row][col]= row*col

print (multilist)
```
</details>
</details>

---

<details>
<summary><b>Question 8</b></summary>

### Question:
Write a program that accepts a comma separated sequence of words as input and prints the words in a comma-separated sequence after sorting them alphabetically.


Then, the output should be:


#### Example
Let us assume the following comma separated input sequence is given to the program: \
without,hello,bag,world \
Then, the output should be: \
bag,hello,without,world

### Level 2
### Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

### Solution
<details>
<summary> See Solution </summary>

``` python
items=[x for x in raw_input().split(',')]
items.sort()
print (','.join(items))
```
</details>
</details>

---

<details>
<summary><b>Question 9</b></summary>

### Question:
Write a program that accepts sequence of lines as input and prints the lines after making all characters in the sentence capitalized.

#### Example
Let us assume the following comma separated input sequence is given to the program: \
Hello world \
Practice makes perfect \
Then, the output should be: \
HELLO WORLD
PRACTICE MAKES PERFECT

### Level 2
### Hints:
In case of input data being supplied to the question, it should be assumed to be a console input.

### Solution
<details>
<summary> See Solution </summary>

``` python
lines = []
while True:
    s = raw_input()
    if s:
        lines.append(s.upper())
    else:
        break;

for sentence in lines:
    print (sentence)
```
</details>
</details>
