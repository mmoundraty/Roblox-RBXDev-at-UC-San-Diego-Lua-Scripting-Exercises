# Roblox + RBXDev at UC San Diego Lua Scripting Exercises

This doc will cover:
1. Print Statements
2. Comments
3. Variables & DataTypes
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
<br>
`TODO: Try writing your first line of code by typing print("Hello, world!")`

### 1.2 Printing more than one line <br>
You can do this repeatedly as well. <br>
<br>
`TODO: Code 3 seperate lines where you print your Name, Major, and College.`

### 1.3 Printing Numbers <br>
You can also print numbers in two ways <br>
e.g: `print(67)` or `print("67")` <br>
<br>
`TODO: Try it yourself, but with negative numbers`

### 1.4 Using multiple print statements to make a picture <br>
```
TODO: Now try printing a triangle like this
* 
** 
*** 
**** 
*****
```
<br>

### 1.5 Newline <br>
If you do not like printing multiple lines to have a new line. Then you can use the newline character `'\n'` <br>
e.g: `print("Hello \n World")` prints <br>
```
Hello
World
```
<br>

`TODO: Print your Name, Major, and College using one line with the '\n' character`

### 1.6 Concatenation <br>
Concatenation combines your strings into a single string. <br>
e.g `print("Hello" .. "World")` prints `HelloWorld`<br><br>
You might be wondering why there isn't a space. That is because you manually need to add a space in your second string, like this: `print("Hello" .. " World")` prints `Hello World`. <br><br>
Great! Now you know how to concatenate strings using the `..` operator but there is another way to concatenate strings by doing `,` which automatically adds a space for you. <br>
e.g `print("Hello", "World")` prints `Hello World` <br>
<br>
`TODO: Print your Name, Major, and College using Concatenation with either '..' or ',' `<br><br>
Though you might not see the use for this in this section, the next section shows why this is very helpful.


