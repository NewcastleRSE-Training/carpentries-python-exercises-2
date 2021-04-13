# Programming with Python

## Exercise 1.1

After each of these lines, what is the value of the variables `mass` and `age`?

```
mass = 47.5
age = 122
mass = mass * 2.0
age = age - 20
```

<details>
<summary>Solution
</summary>

`mass` = 47.5, `age` does not exist   

`mass` = 47.5, `age` = 122    

`mass` = 95.0, `age` = 122  
 
`mass` = 95.0, `age` = 102   

</details>


## Exercise 1.2

What does this program print out?

```
first, second = 'Grace', 'Hopper'
third, fourth = second, first
print(third, fourth)
```

<details>
<summary>Solution
</summary>

Hopper Grace
</details>

## The Data

![Data table](fig/dataTable.png)

![Data csv](fig/dataCSV.png)

## Accessing data using indexes

![Data access](fig/accessData.PNG)

<strong>Unlike</strong> Cartesian co-ordinates -
[row, col] and  [0,0] is top left rather than bottom left.

 
![Slicing](fig/slicing.png)

## Accessing data across axis
![across axis](fig/acrossAxis.PNG)

## Exercise 2.1: Slicing strings

```
element = 'oxygen'
print('first three characters:', element[0:3])
print('last three characters:', element[3:6])
```

```
first three characters: oxy
last three characters: gen
```

What are the values of `element[:4]`, `element[4:]` and `element[:]`?

<details>
<summary>Solution
</summary>

```
element[:4] = oxyg
element[4:] = en
element[:] = oxygen
```

</details>

What is `element[-1]` and `element[-2]`?
 
<details>
<summary>Solution
</summary>

```
n
e
```

</details>

Given those answers, explain what element[1:-1] does.

<details>
<summary>Solution
</summary>

```
element[1:-1] = xyge
```
Creates a substring from index 1 up to (not including) the final index, effectively removing the first and last letters from ‘oxygen’

</details>

Rewrite `element[3:6]` (last 3 characters) to work with any length string.
How can we rewrite the slice for getting the last three characters of element (`element[3:6]`), so that it works even if we assign a different string to element? Test your solution with the following strings: `carpentry`, `clone`, `hi`.

<details>
<summary>Solution
</summary>

`element[3:6]` becomes `element[-3:]`

```
element = 'oxygen'
print('last three characters:', element[-3:])
element = 'carpentry'
print('last three characters:', element[-3:])
element = 'clone'
print('last three characters:', element[-3:])
element = 'hi'
print('last three characters:', element[-3:])
```

```
last three characters: gen
last three characters: try
last three characters: one
last three characters: hi
```

</details>

## Exercise 3.1 Make your own plot
We created a plot of min values like this:

```.env
min_plot = matplotlib.pyplot.plot(numpy.min(data, axis=0))
matplotlib.pyplot.show()
```

Change this code to plot the standard deviation across all patients for each day. 
(hint: `std()` is the numpy function we need here).

<details>
<summary>Solution
</summary>

![Solution 3.1](fig/ex3.1.PNG)

</details>



## Exercise 4.1 Computing powers with loops
Exponentiation is built into Python:
``` 5 ** 3``` gives `125`

Can you write a loop that would do the same? You may want to use `range`

<details>
<summary>Solution
</summary>

![Solution 4.1](fig/ex4.1.PNG)

</details>

## Exercise 4.2 Reverse a string
Two strings can be concatenated using `+` e.g. `'take' + 'away'` would give `'takeaway'`. Write a loop that takes a string and produces a new string with the characters in reverse order so `Newton` becomes `notweN`.

Hint: create two variables, one for the new string and one for the original. Concatenating adds onto the end of the string, so plan ahead what order you want to add characters from the original string to the new one.

<details>
<summary>Solution
</summary>

![Solution 4.2](fig/ex4.2.PNG)

</details>

## Exercise 5.1 Turn a string into a list
Use a for-loop to convert the string `hello` into a list of letters  `['h', 'e', 'l', 'l', 'o']`

Hint: Before your for loop, create an empty list to add characters to like this: `my_list = []`

<details>
<summary>Solution
</summary>

![Solution 5.1](fig/ex5.1.PNG)

</details>

## Exercise 5.2 Slicing from the end
You want to access the last 2 characters of this string and the last 2 entries in this list using the same square brackets. What would need to go inside the square brackets?

```.env
str = 'Observation date: 02-Feb-2013'
lst = [['fluorine', 'F'], ['chlorine', 'Cl'], ['bromine', 'Br']]

str[?:?]
lst[?:?]
```

<details>
<summary>Solution
</summary>
[-2:]
</details>

## Exercise 5.3 Non-continuous slices
You can include a third argument inside the square brackets to set the step size and only take every nth element from the list.

```.env
primes = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37]
subset = primes[0:12:3]
print('subset', subset)
```

```.env
subset [2, 7, 17, 29]
```

How would you get every other element, starting from the second element? i.e.  `subset [3, 7, 13, 19, 29, 37]`

<details>
<summary>Solution
</summary>
primes[1::2]
</details>



![comparisons](fig/comparisons.PNG)


## Exercise 7.1 How many paths?

```python
if 4 > 5:
    print('A')
elif 4 == 5:
    print('B')
elif 4 < 5:
    print('C')
```

What would be printed?

1. A

2. B

3. C

4. B and c

<details>
<summary>Solution
</summary>
C gets printed because none of the other statements are true
</details>

## Exercise 7.2 What is truth?
`True` and `False` are not the only values in Python that are true and false. Run the following code to see what happens.

```python
if '':
    print('empty string is true')
if 'word':
    print('word is true')
if []:
    print('empty list is true')
if [1, 2, 3]:
    print('non-empty list is true')
if 0:
    print('zero is true')
if 1:
    print('one is true')
```
<details>
<summary>Solution
</summary>

Zero, the empty string, and the empty list are considered false; all other numbers, strings, and lists are considered true.

</details>


## Exercise 7.3 Counting vowels
Write a loop that counts the number of vowels in a character string. Test it on as many different words and sentences as you have time for.

<details>
<summary>Solution
</summary>

![7.2 Solution](fig/ex7.2.PNG)

</details>


## Episode 8 Creating Functions


![Function demo](fig/functionDemo.PNG)


## Exercise 8.1 Combining strings
“Adding” two strings produces their concatenation: `a + b` is `ab` .  

Write a function that takes 2 parameters , `original` and `wrapper` and returns a new string that contains the wrapper either side of the original. A call to your function should look like this:
```python
print(fence('name', '*'))
```

```python
*name*
```

<details>
<summary>Solution
</summary>

![Ex 8.1](fig/ex8.1.PNG)
</details>

## Exercise 8.2 Return versus print
Note that return and print are not interchangeable. `print` is a Python function that prints data to the screen. It enables us to see the data. A `return` statement makes data visible to the program. Let’s have a look at the following function:

```python
def add(a, b):
    print(a + b)
```

What will we see if we execute the following commands?

```python
A = add(7, 3)
print(A)
```


<details>
<summary>Solution
</summary>
Python will first execute the function add with a = 7 and b = 3, and, therefore, print 10. However, because function add does not have a line that starts with return (no return “statement”), it will, by default, return nothing which, in Python world, is called None. Therefore, A will be assigned to None and the last line (print(A)) will print None. As a result, we will see:

10

None

</details>

## Exercise 8.3 Mixing default and non-default parameters
```python
def numbers(one, two=2, three, four=4):
    n = str(one) + str(two) + str(three) + str(four)
    return n

print(numbers(1, three=3))
```

Guess what will happen when this code is run:
 1. `1234`
 2.   `one2three4`
 3.  `1239`
 4.   `SyntaxError`
 
 Try it out. The result might seem a bit cryptic, can you work out what it means?


<details>
<summary>Solution
</summary>

4. Syntax error. Parameters without default values must be given before any that do. (e.g. def numbers(one, three, two=2, four=4):)
</details>


```python
def func(a, b=3, c=6):
    print('a: ', a, 'b: ', b, 'c:', c)

func(-1, 2)
```


What result is correct?
1. `a: b: 3 c: 6`
2.   `a: -1 b: 3 c: 6`
3.  `a: -1 b: 2 c: 6`
4.   `a: b: -1 c: 2`

<details>
<summary>Solution
</summary>

3. a and b are assigned and c is default.

</details>
