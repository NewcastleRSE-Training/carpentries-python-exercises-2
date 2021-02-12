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
![across axis](fig/acrossAxis.png)

## Exercise 2.1 Slicing strings

```.env
element = 'oxygen'
print('first three characters:', element[0:3])
print('last three characters:', element[3:6])
```

```.env
first three characters: oxy
last three characters: gen
```
What are the values of:
 a. `element[:4]`, `element[4:]` and `element[:]`?
 
 b. `element[-1]` and `element[-2]`?
 
 c. `element[1:-1]`

Rewrite `element[3:6]` (last 3 characters) to work with any length string.


<details>
<summary>Solution
</summary>

 a. `element[:4]` = oxyg, `element[4:]` = en, `element[:]` = oxygen
 
 b. `element[-1]` = n `element[-2]` = e
 
 c. `element[1:-1]` = xygen (index 1 up to but not including last index)

`element[3:6]` becomes `element[-3:]`

</details>


## Exercise 3.1 Make your own plot
We created a plot of min values like this:

```.env
min_plot = matplotlib.pyplot.plot(numpy.min(data, axis=0))
matplotlib.pyplot.show()
```

Change this code to plot the standard deviation across all patients for each day. 
(hint: `std()` is the numpy function we need here).

## Exercise 4.1 Computing powers with loops
Exponentiation is built into Python:
``` 5 ** 3``` gives `125`

Can you write a loop that would do the same? You may want to use `range`

<details>
<summary>Solution
</summary>

result = 1

for number in range(0, 3):

    result = result * 5
    
print(result)

</details>

## Exercise 4.2 Reverse a string
Two strings can be concatenated using `+` e.g. `'take' + 'away'` would give `'takeaway'`. Write a loop that takes a string and produces a new string with the characters in reverse order so `Newton` becomes `notweN`.

Hint: create two variables, one for the new string and one for the original. Concatenating adds onto the end of the string, so plan ahead what order you want to add characters from the original string to the new one.

<details>
<summary>Solution
</summary>
newstring = '' 

oldstring = 'Newton'

for char in oldstring:

    newstring = char + newstring
    
print(newstring)

</details>

## Exercise 5.1 Turn a string into a list
Use a for-loop to convert the string `hello` into a list of letters  `['h', 'e', 'l', 'l', 'o']`

Hint: Before your for loop, create an empty list to add characters to like this: `my_list = []`

<details>
<summary>Solution
</summary>

my_list = []
for char in 'hello':
    my_list.append(char)
print(my_list)
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



![comparisons](fig/comparisons.png)


