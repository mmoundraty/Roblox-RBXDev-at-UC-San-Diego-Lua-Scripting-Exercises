# Roblox + RBXDev at UC San Diego Lua Scripting Exercises

This doc will cover:
1. Print Statements
2. Variables & DataTypes
3. Comments
4. Tables/Dictionaries
5. Operators
6. Conditions (if/else)
7. Loops
8. Functions

Each section includes examples + exercises you can try!

Also edit parts where it says -- [[ CODE HERE ]] --

## 1. Print Statements 

### 1.1 Printing your First Line 
Print is used to show messages in the Output window. 

**Exercise**
```
TODO: Try writing your first line of code by typing print("Hello, world!")
```

### 1.2 Printing more than one line 
You can do this repeatedly as well. 

**Exercise**
```
TODO: Code 3 seperate lines where you print your Name, Major, and College.
```

### 1.3 Printing Numbers 
You can also print numbers in two ways <br>
e.g: `print(67)` or `print("67")` 

**Exercise**
```
TODO: Try it yourself, but with negative numbers
```

### 1.4 Using multiple print statements to make a picture 

**Exercise**
```
TODO: Now try printing a triangle like this
* 
** 
*** 
**** 
*****
```

### 1.5 Newline 
If you do not like printing multiple lines to have a new line. Then you can use the newline character `'\n'` <br>
e.g: `print("Hello \n World")` prints <br>
```
Hello
World
```

**Exercise**
```
TODO: Print your Name, Major, and College using one line with the '\n' character
```

### 1.6 Concatenation <br>
Concatenation combines your strings into a single string. <br>
e.g `print("Hello" .. "World")` prints `HelloWorld`<br><br>
You might be wondering why there isn't a space. That is because you manually need to add a space in your string, like this: `print("Hello" .. " World")` prints `Hello World`. <br>

**Exercise**
```
TODO: Concatenate the strings "Who is the imposter?", "Where is the imposter?", "Why is the imposter?" using '..' 
``` 

Though you might not see the use for this in this section, the next section shows why this is very helpful.

## 2. Variables & Data Types

Variables store values that can change, this is convenient because they are reuseable.

### 2.1 Naming Variables
You can name your variables anything, as long as it does not start with a number, has a space in between, or have special characters that is not an underscore "_". Violating the naming conventions will result in an error in your script output.

**Example**
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

**Example**
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

**Example**
```
name = "Roblox + RBXDev at UCSD"
year_started = 2024
is_active = true
empty_value = nil
``` 

### 2.3 Concatenation using Variables
Remember concatentation from the previous section? We will be doing that again but with variables!

**Exercise**
```
TODO: Copy the following variables, and then Print the string "[name_1] had a little [animal] while [name_2] had [number] cows!" using concatenation and variables.

name_1 = "Mary"
name_2 = "Bob"
animal = "Lamb"
number = 10
```

### 2.4 Storing variables with variables
Yes you heard that right, Variables can also store other variables.

**Example**
```
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


## 3. Comments
Comments are used to add explanations, notes, or temporarily disable parts of the code without affecting the program's execution. Lua offers two types of comments: 
- Single Line Comments
- Multi-Line Comments

**Example**
```
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

## 4. Tables and Dictionaries

Tables and Dictionaries are very useful for storing values into a list such as integers, strings, booleans, functions (Something that we will cover later), and even tables itself. This helps prevent repetitiveness of writing your programs.

### 4.1 Constructing Tables

Tables are constructed with curly braces {}

**Example**
```
str = {"Jim", "Joe", "Bob"} -- A table that stores string types
nums = {5, 6, 7, 8} -- A table that stores number types
bools = {true, false, true, false} -- A table that stores boolean types
tables = {{"Jim", "Joe", "Bob"}, {5, 6, 7, 8}, {true, false, true, false}} -- A table that stores tables
```

A cool thing about Lua is that a table can store more than one data type like this:

**Example**
```
testArray = {"A string", 3.14159, true} -- A table that stores multiple types
```

**Exercise**
```
TODO: Make a Table about your favorite class at UCSD

- Class Name (String)
- Class Rating out of 5 (Number)
- Is it being offered next quarter (Boolean)
```

### 4.2 Printing a Table
You can print a table to see it's contents.

**Example**
```
testArray = {"A string", 3.14159, true}
print(testArray)
Output: {
            [1] = "A string",
            [2] = 3.14159,
            [3] = true
        }
```
An explanation of the output, the right side are the contents of your table while the left side is the index of the contents.

**Exercise**
```
TODO: Print out the table that you created about your favorite class at UCSD
```

### 4.3 Indexing a table

You can access a element in a table using square brackets []. Lua uses 1-based indexing.

**Example**
```
str = {"Jim", "Joe", "Bob"}
var = str[1] -- Accesses the element "Jim"
print(var) 
Output: Jim

nums = {5, 6, 7, 8}
print(nums[2]) -- Accesses the element 6
Output: 6

bools = {true, false, true, false}
var = bools[4] -- Accesses the element false
print(var)
Output: false
```

**Exercise**
```
TODO: Print this statement using table indexing and concatenation

1. "My favorite class at UCSD is [insert favorite class]"
2. "I would rate the class [insert rating] out of 5"
3. "It is [insert boolean] that this class is being offered next quarter"
```

You'll see that you get an error trying to concatenate a string with a boolean. To fix this use the tostring() method, this converts booleans and numbers into strings.

**Example**
```
value = tostring(class[3])
print("It is " .. value .. " that this class is being offered next quarter")
```

### 4.4 Changing a Table's item

You can change a specific element in a table by specifying the index.

**Example**
```
testArray = {"A string", 3.14159, true}
testArray[2] = 23
print(testArray)
Output: {
            [1] = "A string",
            [2] = 23,
            [3] = true
        }
```

### 4.5 Inserting items

You can insert elements in a table using the table.insert() method. In the first parameter add your table, and in the second parameter add the element that you want to insert. This inserts an element at the end of the list.

**Example**
```
nums = {1, 2}
table.insert(nums, 3)
print(nums)
Output: {
            [1] = 1,
            [2] = 2,
            [3] = 3
        }
```

**Exercise**
```
TODO: Insert the grade that you got from your favorite class
```

If you wanted to insert an element at a specific position. Pass the table in the first parameter, specify the index in the second parameter, add the element in the third parameter.

**Example**
```
nums = {1, 2, 4}
table.insert(nums, 3, 3)
print(nums)
Output: {
            [1] = 1,
            [2] = 2,
            [3] = 3,
            [4] = 4
        }
```

### 4.6 Removing items

You can remove elements in a table using the table.remove() method. In the first parameter add your table, and in the second parameter specify the index.

**Example**
```
nums = {6, 9, 7}
table.remove(nums, 2)
print(nums)
Output: {
            [1] = 6,
            [2] = 7
        }
```

**Exercise**
```
TODO: Remove the grade that you got from your favorite class
```

### 4.7 Finding the Index of a Value

You can find elements in a table using the table.find() method. In the first parameter add your table, and in the second parameter specify the element that you want to find.

**Example**
```
testArray = {"A string", 3.14159, true}
index = table.find(testArray, "A string")
print(index)
Output: 1
```

### 4.8 Copying a Table

A naive way to think about copying a table is to create a variable that stores another table like our example here.

**Example**
```
arr_1 = {"A string", 3.14159, true}
arr_2 = arr_1
```

If you are not planning to change the elements of either tables then this is fine. But if you are, then this is problematic.

**Example**
```
arr_1 = {"A string", 3.14159, true}
arr_2 = arr_1
arr_1[1] = "Changed"
print(arr_2[1])
Output: Changed
```
Why did the contents of the second table change even though we only changed the first table? This is because of Reference Aliasing, meaning that the second table is sharing contents with the first table, you can't change the contents of one table without affecting the other table.

One way to avoid reference aliasing when copying tables in Lua is to use the table.clone() method, which creates a shallow copy of a table.

**Example**
```
arr_1 = {"A string", 3.14159, true}
arr_2 = table.clone(arr_1)
arr_1[1] = "Changed"
print(arr_2[1])
Output: A string
```
Cool! Now we know how to make a copied table without worrying about affecting other tables. This works correctly because the table contains only primitive data types such as strings, numbers, and booleans. These values are immutable, so copying their references behaves the same as copying their values.

However, table.clone() does not create a deep copy. If a table contains non-primitive, mutable values (such as other tables), those nested tables are still shared between the original table and the cloned table.

**Example**
```
arr_1 = {{"Jim", "Joe", "Bob"}, {5, 6, 7, 8}, {true, false, true, false}}
arr_2 = table.clone(arr_1)
arr_1[1][1] = "Him"
print(arr_2[1])
Output: {
            [1] = "Him",
            [2] = "Joe",
            [3] = "Bob"
        }
```
Even though we modified the first table it still affected the second table, a frustration that we faced previously. This happens because table.clone() only copies the top-level table. The inner tables are copied by reference, which leads to aliasing and shared mutable state. As a result, modifying a nested table in one copy also affects the other.

Another way that we can copy a table is a deep-copy by directly inserting each element from one table onto another table.

**Example**
```
arr_1 = {"A string", 3.14159, true}
arr_2 = {}
arr_2[1] = arr_1[1]
arr_2[2] = arr_1[2]
arr_2[3] = arr_1[3]
arr_1[1] = "New String"
print(arr_2[1])
Output: A string

arr_1 = {{"Jim", "Joe", "Bob"}, {5, 6, 7, 8}, {true, false, true, false}}
arr_2 = {{}, {}, {}}
arr_2[1][1] = arr_1[1][1]
arr_2[1][2] = arr_1[1][2]
arr_2[1][3] = arr_1[1][3]
arr_2[2][1] = arr_1[2][1]
arr_2[2][2] = arr_1[2][2]
arr_2[2][3] = arr_1[3][3]
arr_2[3][1] = arr_1[3][1]
arr_2[3][2] = arr_1[3][2]
arr_2[3][3] = arr_1[3][3]
arr_1[1][1] = "Him"
print(arr_2[1])
```
Doing a deep-copy of a table is fool-proof, you can change elements of one table without affecting another. Although doing it this way is very repetitive, especially if there are a lot of values in the list... If only there is a way to make this less repetitive (loops).

### 4.9 Dictionaries

Dictionaries are an extension of arrays. Dictionaries store a set of key-value pairs, where the keys can be any number, string, or object. This is very similar to a table except the indexes are not just limited to numbers but also strings and objects.

To create a Dictionary, name your indexes and set it equal to the value that you want.

**Example**
```
testDictionary = {
	fruitName = "Lemon",
	fruitColor = "Yellow",
	sour = true
}
```

There are to ways to access an element. One way is to use square brackets [] like tables and type the name of the index inside quotes. The other way is to add a dot after the list and type the name of the index.

**Example**
```
-- Example 1
testDictionary["fruitName"]

-- Example 2
testDictionary.fruitName
```

Changing an element

**Example**
```
-- Example 1
testDictionary["fruitColor"] = "Orange" 

-- Example 2
testDictionary.fruitColor = "Orange"
```

Adding an element

**Example**
```
testDictionary.fruitCount = 10
```

Removing an element

**Example**
```
testDictionary.sour = nil
```

### 4.10 Length of a List

If we wanted to know the length of a table or dictionary, we can use the `#` operator in front of the table/dictionary name.

**Example**
```
testArray = {"A string", 3.14159, true}
length = #testArray
print(length)
Output: 3
```

## 5. Operators

An operator is a symbol for performing an operation or conditional evaluation. If you have not noticed, using `..` is an operation itself for concatenating strings and using `#` is an operation for returning the length of a list. We will be going over the basic operations.

### 5.1 Arithmetic Operations

| Operator | Description    | Example     |
| -------- | -------------- | ----------- |
| +        | Addition       | 1 + 1 = 2   |
| -        | Subtraction    | 1 - 1 = 0   |
| *        | Multiplication | 5 * 5 = 25  |
| /        | Division       | 10 / 5 = 2  |
| //       | Floor Division | 10 // 4 = 2 |
| ^        | Exponent       | 2 ^ 4 = 16  |
| %        | Modulus        | 13 % 7 = 6  |

You can even perform arithmetic operations on variables

**Example**
```
num_1 = 1
num_2 = 2

result_1 = num_1 + num2
print(result_1)
Output: 3

result_2 = num1 - num2
print(result_2)
Output: -1
```

Lua also does PEMDAS when doing arithmetic Operations

**Example**
```
result = ((5 + 2 * 4) / 2) ^ 2
print(result)
Output: 42.25
```

**Exercise**
```
TODO: Try these operations yourself!
```

### 5.2 Compound assignment

You can use compound assignment operators to set a variable equal to the result of an operation where the first parameter is the variable's current value. This is a cool shortcut for performing operations with variables.

In the following examples, suppose local x = 3.

| Operator | Description    | Example       | New Value of x |
| -------- | -------------- | ------------- | -------------- |
| +=       | Addition       | x += 2        | 5              |
| -=       | Subtraction    | x -= 2        | 1              |
| *=       | Multiplication | x *= 2        | 6              |
| /=       | Division       | x /= 2        | 1.5            |
| //=      | Floor Division | x //= 2       | 1              |
| ^=       | Exponent       | x ^= 2        | 1              |
| %=       | Modulus        | x %= 2        | 9              |
| ..=      | Concatenation  | x ..= " Way!" | "3 Way!"       |

**Exercise**
```
TODO: Try it yourself with a different variable!
```

### 5.3 Relational Operators

Relational operators compare two parameters and return a boolean: true or false.

| Operator | Description              | Example | Output |
| -------- | ------------------------ | ------- | ------ |
| ==       | Equal to                 | 3 == 5  | false  |
| ~=       | Not equal to             | 3 ~= 5  | true   |
| >        | Greater than             | 3 > 5   | false  |
| <        | Less than                | 3 < 5   | true   |
| >=       | Greater than or equal to | 3 >= 5  | false  |
| <=       | Less than or equal to    | 3 <= 5  | true   |

**Exercise**
```
TODO: Try it yourself with a different variable!
```

### 5.4 Logic Operators

Logical operators return values depending on the boolean values of the given arguments. Unlike many other languages, Luau considers both zero and the empty string as true. The following table summarizes how logical operators behave in conditionals. This will be useful when we will cover conditionals.

| Operator | Description                                        |
| -------- | -------------------------------------------------- |
| and      | Evaluates as true only if both conditions are true |
| or       | Evaluates as true if either condition is true      |
| not      | Evaluates as the opposite of the condition         |

**Example of AND**
```
a = true
b = false

print(a and a)
Output: True

print(a and b)
Output: False

print(b and a)
Output: False

print(b and b)
Output: False
```

**Example of OR**
```
Example

a = true
b = false

print(a or a)
Output: True

print(a or b)
Output: True

print(b or a)
Output: True

print(b or b)
Output: False
```

**Example of NOT**
```
a = true
b = false

print(not a)
Output: False

print(not b)
Output: True
```

## 6. Conditionals

In scripting, we will often want to check if a value or object satisfies some criteria. This can be accomplished by using conditionals, which come in the form of if statements, along with the elseif and else statements. For example, if it's 8am `drink coffee`, otherwise `drink water`.

### 6.1 If Statements

The `if` statement is the simplest form of a conditional. It will only run if the specified condition evaluates to true.

**Example**
```
x = 5
y = 10
if x <= y then
    print(x)
end

Output: 5
```

```
TODO: Try this with the other relational operators from the previous section.
```

### 6.2 Else Statements

The `else` statement is used to run alternative code when the initial condition evaluates to false.

**Example**
```
x = true
y = false

if x and y == true then
    print("both statements are true")
else
    print("one or both statements are false")
end

Output: one or both statements are false
```

**Exercise**
```
TODO: See what outputs you get by setting x for each ingredient.

ingredients = {lettuce, tomatoe, onion}
x = ?

if(ingredients[x] == "lettuce") then
    print("That's the right ingredient")
else
    print("That's the wrong ingredient")
end
```

### 6.3 Else If Statements

The `elseif` statement allows for multiple condition checks, given that any preceding if/elseif statements are false. 

**Example**
```
team_1 = "red"
team_2 = "blue"
player = team_2
if player == team_1 then
    print("Player is in Red Team")
elseif player == team_2 then
    print("Player is in Blue Team")
else
    print("Player is not in any Team")
end

Output: Player is in Blue Team
```

**Exercise**
```
TODO: Make a program that determines of a year is a leap year or not
```

## 7. Loops

Loops are a common feature in many scripts, often used to repeat sets of code. If you remember from our Table's section there were repetitive lines of code that could have used a loop to make the lines of code shorter. We will be covering the two main types of loops: `while` and `for` loops. 

### 7.1 While Loops

