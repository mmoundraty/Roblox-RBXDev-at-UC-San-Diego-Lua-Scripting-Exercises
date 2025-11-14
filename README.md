# Roblox + RBXDev at UC San Diego Lua Scripting Exercises

This doc will cover:
1. Print Statements
2. Variables & DataTypes
3. Comments
4. Operators
5. Conditions (if/else)
6. Loops
7. Functions
8. Tables / Dictionaries

Each section includes examples + exercises you can try!

Also edit parts where it says -- [[ CODE HERE ]] --

## 1. Print Statements

### 1.1 Printing your First Line <br>
Print is used to show messages in the Output window. <br>
```
TODO: Try writing your first line of code by typing print("Hello, world!")
```

### 1.2 Printing more than one line <br>
You can do this repeatedly as well. <br>
<br>
```
TODO: Code 3 seperate lines where you print your Name, Major, and College.
```

### 1.3 Printing Numbers <br>
You can also print numbers in two ways <br>
e.g: `print(67)` or `print("67")` <br>
<br>
```
TODO: Try it yourself, but with negative numbers
```

### 1.4 Using multiple print statements to make a picture <br>
```
TODO: Now try printing a triangle like this
* 
** 
*** 
**** 
*****
```

### 1.5 Newline <br>
If you do not like printing multiple lines to have a new line. Then you can use the newline character `'\n'` <br>
e.g: `print("Hello \n World")` prints <br>
```
Hello
World
```
<br>

```
TODO: Print your Name, Major, and College using one line with the '\n' character
```

### 1.6 Concatenation <br>
Concatenation combines your strings into a single string. <br>
e.g `print("Hello" .. "World")` prints `HelloWorld`<br><br>
You might be wondering why there isn't a space. That is because you manually need to add a space in your string, like this: `print("Hello" .. " World")` prints `Hello World`. <br>

```
TODO: Concatenate the strings "Who is the imposter?", "Where is the imposter?", "Why is the imposter?" using '..' 
``` 

Though you might not see the use for this in this section, the next section shows why this is very helpful.

## 2. Variables & Data Types

Variables store values that can change, this is convenient because they are reuseable.

### 2.1 Naming Variables
You can name your variables anything, as long as it does not start with a number, has a space in between, or have special characters that is not an underscore "_". Violating the naming conventions will result in an error in your script output.

```
Valid variable names

var = "Hello World"
x = 1
npc_dialogue = "Sorry, We don't accept Triton Cash."
THIS_IS_ALSO_VALID = "this is also valid"

Invalid variable names

my sentence = "yadda yadda yadda"
4numbers = {1, 2, 3, 4}
$money$ = "6.99"
```

You can also print variables
```
var = "Hello World"
print(var) 
Output: Hello World

x = 1
print(x)
Output: 1
```
### 2.2 Data Types
Data Types organizes values into different types. Right now we will be discussing the four basic data types in Lua such as
- Strings: Collection of characters like words or sentences
- Numbers: Any numbers including decimals
- Booleans: True or False Values
- nil: An absence of a value

```
Example

name = "Roblox + RBXDev at UCSD"
year_started = 2024
is_active = true
empty_value = nil
``` 

### 2.3 Concatenation using Variables
Remember concatentation from the previous section? We will be doing that again but with variables!

```
TODO: 

Copy the following variables:

name_1 = "Mary"
name_2 = "Bob"
animal = "Lamb"
number = 10

Print the string "[name_1] had a little [animal] while [name_2] had [number] cows!" using concatenation and variables.
```

### 2.4 Storing variables with variables
Yes you heard that right, Variables can also store other variables.

```
Example

x = 23
y = x
print(y)
Output: 23

order = "1 Burger with Bacon"
copy_of_order = order
print(copy_of_order)
Output: 1 Burger with Bacon

copy_of_order = copy_of_order .. " with no Pickles"
print(copy_of_order)
Output: 1 Burger with Bacon with no Pickles
```
```
TODO:
Write a program using print statements and variables about John and Mary's conversation.

John: I'm going to Cotijas Taco Shop do you want anything?

Mary: Please get me 2 beef Tacos and 2 Pork Tacos.

John: Okay, going on my way now.

Mary: Wait sorry! Please get me 2 beef Tacos and 2 Pork Tacos and 2 Chicken Tacos.

John: Okay is that all?

Mary: Yes
```

## 3. Comments
Comments are used to add explanations, notes, or temporarily disable parts of the code without affecting the program's execution. Lua offers two types of comments: 
- Single Line Comments
- Multi-Line Comments

```
Example

-- This is a Single Line Comment

-- [[
    This
    is
    a
    Multi-Line
    Comment
]]
```
It is good practice as a programmer to leave comments in your code so that your program is more readable and understandable.


