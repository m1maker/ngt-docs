# NGT Getting Started Tutorial

this tutorial will talk ngt, the new game toolkit, which is an easy programming tool.

# what is NGT?

NGT, New Game Toolkit, is an easy tool to develop your games from the ground up, without having prior programming knowledge at all. built with easy coding and rich features access, NGT is a tool which makes you a developer of your game.

built with powerful features and endless possibilities, NGT is a great yet powerful audiogame engine.

not enough features as you want? NGT is an open source, you could contribute. you may find the useful resources section at the bottom of this document.


## the process

NGT is a scripting language, meaning the code that you write turns into a language that computers can understand. Once the code is translated into the computer's understandable language, the computer executes the commands exactly as instructed through the code. Additionally, let's distinguish between programming and scripting languages.

The primary difference between programming and scripting languages lies in their execution. Programming languages usually need to be compiled before they can be executed, converting the code into an executable form. On the other hand, scripting languages are interpreted line by line during runtime without the need for a separate compilation step.

## the engine

NGT is an engine, meaning that you don't need special programs to build your games. All you need is the kit and a text editor, both of which you already have.

# start off (language syntax)

to start off, I may tell you important things. only then will you be able to take your coding skills to the next level of learning.

## statements

a statement is simply an instruction that the ngt will follow. each statement is followed by a semicolon (;). it can then be further sepret with a new line If you wish.

## blocks

Blocks execute code only if specific conditions are met. It's encapsulated by curly braces (`{` and `}`).

## Expressions

Expressions typically serve as specialized statements and often mark the starting point for a code block. An expression commonly comprises a keyword followed by the expression code, enclosed in parentheses. Keywords, such as 'if' and 'while', instruct the engine to perform specific actions. For instance, 'if' directs the engine to verify whether a given expression is true, while 'while' prompts the compiler to iterate a block of code until the expression conditions are satisfied.

It's essential to note that expressions do not conclude with a semicolon. They represent conditions rather than direct instructions to the engine. These conditions dictate when the instructions should be executed.

## Comments

A comment serves various purposes such as displaying author information, dates, or any relevant details. There are no strict rules for comments; you can write in English, include personal information, or jot down notes that may or may not aid others' understanding.

For a short comment, use `//` (two slashes). Anything written on that line will not be executed.

For a longer comment, use `/*` (forward slash followed by an asterisk) to begin your comment. You may include multiple lines for your comments, and once finished, close it with `*/` (asterisk followed by a forward slash).

# first script, printing text

One of the initial steps in programming is to display text on the screen. Consider the following example:

first create the file test.ngt. then, you can start testing with codes.



```{ngt} test.ngt
void main()
{
alert("hello","hello, world!");
}
```




The first time might be confusing, but let's dissect it piece by piece.




`void main()`




This line signifies the start of the `main` function. You'll need to call this function at the beginning of your script.




`{`




This curly brace represents the beginning of a block. The code within this block is executed under specific conditions or circumstances.




`alert(`




a function which ngt provides by default.




`"hello",`




This represents the title of the window and serves as a parameter for the `alert` function. Each parameter is separated by a comma (,).




`"hello, world!");`




This text is what will be displayed. A right parenthesis indicates the end of the function call, and a semicolon ; indicates the conclusion of a statement.




`}`




This closing curly brace signifies the end of the main function, indicating to the engine that the main function concludes here.




# Variables

## Variables; What Are They?

If you've ever used a container to hold something—a box for your favorite toys, a jar for cookies—understanding variables is quite similar. In programming, a variable acts like one of these containers; it stores information like a player's health in a game, the price of a commodity, or even a profound truth like the answer to life, the universe, and everything being 42.

Think of variables as flexible containers; they can hold different types of information, and you can change or use that information as needed while programming.

## Declaring and Assigning Variables

Declaring a variable in programming is like naming a container. You specify the type of information it will hold, followed by a name for easy identification later. Every container—here, a variable—needs a name, and it follows certain rules: it can contain letters (both upper and lower case), numbers (except as the first character), and underscores.

Here's an example:




```
int playerScore;
float fishPrice;
```




In this code snippet, we've created two containers: `playerScore` to hold whole numbers (an `int`), and `fishPrice` to contain numbers with decimal points (a `float`).

## Integer Variables

Integer variables store whole numbers, such as -5, 0, or 100, without any fractional parts. They can represent a wide range of values, including negative and positive numbers.

example:




```
int a = 2;
int b = 5;
int c = a + b;
```




We've declared three integer variables: `a`, `b`, and `c`.

First, we set `a` to have the value of 2, then `b` to 5.

Next, we perform addition and assign the result to variable `c`, so `c` will hold the value of `a + b`, which is 7.

## Floating-Point Variables

Floating-point variables, often referred to as "floats" or "doubles," store decimal numbers. They can represent values like 3.14, -0.001, or 10.5. These variables include both the integer and fractional parts of a number.

example:




```
float x = 3.5;
float y = 1.25;
float z = x * y;
```




We've declared three floating-point variables: `x`, `y`, and `z`.

Initially, `x` is assigned the value 3.5, and `y` is assigned 1.25.

Then, we perform multiplication and assign the result to variable `z`, so `z` will hold the value of `x * y`, which is 4.375.

If you're unsure about the value range that will be assigned to a variable, it's advisable to use the `double` data type for floating-point numbers. `double` variables support a broader range of values, including those with decimals or fractions. In case the engine encounters a situation where the value exceeds the supported range, the variable will default to the minimum supported value, possibly causing unexpected behavior. Using `double` ensures a broader range of values and mitigates such potential issues.

supported types:




* **int:** Holds integer numbers within a defined range.
* **int64:** Holds integer numbers within a more defined range.
* **short:** Holds a smaller range of integer values than int, using less memory.
* **uint:** Holds only positive whole numbers (zero and above).
* **long:** Holds a larger range of integer values compared to int.
* **float:** Holds decimal fractions with limited precision.
* **double:** Holds decimal fractions with higher precision and a wider range of values than float.



## String Variables

String variables hold sequences of characters, like text or words. Unlike integers and floating-point numbers, strings are not treated as numerical values. Instead, they are treated as sequences of individual characters that can include letters, numbers, symbols, and spaces.

example:




```
string name = "Harry";
alert("My name is", name);
```




Here, We've created a string variable named `name` that stores the name "Harry". When We pass `name` as the second parameter to `alert`, the message box will display "My name is Harry". Simple, right?




Now, let's get a bit fancier:



```
string name = "Harry";
string message = "My name is " + name + ". Remember it!";
alert("Remember me", message);
```




The `"+variable_name+"` operator here combines the strings together. The resulting message in the box will be: "My name is Harry. Remember it!". I can combine different strings or variables in many ways to create meaningful messages or content.




Strings aren't just for text; they're versatile enough to handle numbers too:




```
string name = "Harry";
int age = random(10, 50);
string info = "I'm " + name + " and I'm " + age + " years old.";
alert("Important info", info);
```




In this example, `random(10, 50)` generates a random age between 10 and 50 for "Harry". The message displayed might say: "I'm Harry and I'm 30 years old.", or any age within that range.

`random` function is provided by the NGT engine, which generates random numbers within a given minimum and maximum range.


Strings also offer ways to handle special characters like new lines or tabs:




```
string multiline = "This is a\r\nmultiline\r\nstring.";
string directory = "The directory is \"c:\\path\\to\\folder\".";
```




The `\r\n` sequence creates new lines, while the backslash `\"` lets me include double quotes inside a string without confusing the compiler.




list of special characters:

* `\"`: Represents a double quote `"`.
* `\\`: Represents a backslash `\`.
* `\r`: Represents a carriage return.
* `\n`: Represents a new line.
* `\t`: Represents a tab `	`.



## Constants

A constant in NGT is akin to a regular variable but with a fundamental distinction. Once a constant is assigned a value, it remains fixed throughout the program's execution, unlike a variable that can vary during runtime.

Constants primarily serve readability and save time in code maintenance. You declare a constant similarly to a variable, but with the addition of the keyword `const` preceding the data type.

Consider the following example:




```
const string audio_ext = ".ogg";
sound beep;
beep.load("sounds/beep" + audio_ext);
```




The advantage is evident when scaling your project. If transitioning to a different audio format like `.wav`, modifying the `audio_ext` constant suffices. All sound assignments using this constant will adapt accordingly, eliminating the need to modify each individual sound reference.




Another type of constant is an enum, short for enumeration, capable of holding only numeric, integer values. Enums are beneficial for grouping constants, streamlining code management. Here's an example:




```
enum direction
{
left = -1,
right = 1
}

enum players
{
jon,
alex
}
```




This code demonstrates two sets of enumerations: `direction` and `players`. In `direction`, we assign `-1` to `left` and `1` to `right`. In `players`, values are not explicitly assigned, so they increment automatically starting from `0`. This approach simplifies adding new players in the future without needing to reassign values.




**Note:** Enums must be defined globally and cannot be declared within a function.

# Functions

In programming, functions are like mini-programs within a larger program. They're blocks of code designed to perform a specific task, making the code more organized and manageable.

To use a function, you need to declare it first. The declaration includes the function's name, return type (like `void` for functions that don't return anything, or data types like `int`, `float`, etc., for functions that do return values), and any parameters it expects. Here's an example:




```
void greet()
{
// Code for the greeting function
alert("Hello","hello world!");
}
```




In this example, `greet` is a function that doesn't take any parameters (`()`) and doesn't return any value (`void`). When called, it displays a message saying "Hello  dialog  hello world!".

To call or use a function, you simply write its name followed by parentheses. If the function returns a value, you can assign that value to a variable or use it directly. If it doesn't return anything, you just invoke the function by its name:




```
// Calling the greet function
void main()
{
greet();
}
```


If a function expects parameters, you need to provide them inside the parentheses when calling the function. For instance:




```{NGT} test.ngt
int add(int a, int b)
{
return a+b;
}
void main()
{
int result = add(3, 5);
}
// Now, 'result' will hold the value 8
```



In this example, the `add` function takes two integers (`a` and `b`) as parameters and returns their sum. When called with `add(3, 5)`, it returns the sum of 3 and 5, which is assigned to the variable `result`.

Functions play a crucial role in programming by allowing code reusability, modularization, and making complex tasks more manageable.

# Conditional Statements

Conditional statements are the backbone of decision-making in programming. They allow your code to make choices based on certain conditions.

## if Statements

The `if` statement evaluates a condition and executes a block of code if that condition is true. If the condition is false, the code inside the `if` block is skipped. You can also have `else if` and `else` blocks to handle alternative conditions.

the `if` statement is as the natural language. for instance, 

`If I become an engineer in the future, I would develop softwares that would be useful for everyone regardless of their disabilities.`

as you can see, we use the word if in the text. although the language cannot do as complecated as this one, it can do based on the codes.

```
int x = 10;

if (x > 5)
{
alert("information","x is greater than 5");
}
else if (x == 5)
{
alert("information","x is equal to 5");
}
else
{
alert("information","x is less than 5");
}
```


In this example, if the value of `x` is greater than 5, it triggers the first alert. If `x` is equal to 5, the second alert is triggered. Otherwise, if none of the previous conditions are met, it triggers the third alert.

* `if (x == y)` \- This is true if x is equal to y. You can perform this check on any type of variable.
* `if (x != y)` \- This is true if x is not equal to y. You can perform this check on any type of variable.
* `if (x < y)` \- This is true if x is lower than y. You can perform this check only on numeric variables.
* `if (x <= y)` \- This is true if x is lower than or equal to y. You can perform this check only on numeric variables.
* `if (x > y)` \- This is true if x is higher than y. You can perform this check only on numeric variables.
* `if (x >= y)` \- This is true if x is higher than or equal to y. You can perform this check only on numeric variables.
* `if (!x)` \- This is true if x is false. This can only be used on boolean variables.




These operators are commonly used in conditions to compare values and make decisions based on the comparison result. For instance, `x > 5` checks if `x` is greater than 5.

## Switch and Case

Switch...case statements function akin to if statements but excel when handling multiple or complex checks.

Let's explore an example:




```
int playerScore;
double bonusPoints;

switch(playerScore)
{
case 1000:
bonusPoints = 200.5;
break;
case 750:
bonusPoints = 150.75;
break;
case 500:
bonusPoints = 100.25;
break;
case 250:
bonusPoints = 50.1;
break;
}
```




The switch keyword initiates the case statement, followed by the variable within parentheses. Each condition begins with the case keyword, enclosed in braces. Typically, a break statement concludes each case, halting further execution.

Omitting the break statement enables execution to flow into the subsequent case, occasionally advantageous but necessitating caution.




Another keyword, default, handles conditions not met by the case statement. For instance:




```
switch(playerScore)
{
case 1000:
bonusPoints = 200.5;
break;
case 750:
bonusPoints = 150.75;
break;
// Additional cases go here
default:
bonusPoints -= 5.0;
}
```




In this scenario, when the player's score doesn't match any defined cases, it decrements the bonusPoints by 5.0.

Note that even the default case incorporates a break. You have flexibility in arranging the cases.

The switch condition accepts any expression yielding a numeric value. For instance:




```
switch(number % 50)
{
// Cases based on remainders go here
}
```




Each case within the switch must be a constant value; using expressions like `case n < 5:` or `case number:` will trigger a compiler error.

A switch cannot contain duplicate case values or multiple default cases.

Switch...case statements allow nesting if required.

# Loops

After experimenting with if statements, it's time to delve into the concept of loops. Loops are sections of code that execute repeatedly until a specific condition is met. They are commonly used in games for tasks like continuously checking keystrokes and events.

## While Loops

Take a look at the following code example:

```
while (key_pressed(SDLK_ESCAPE)==false)
{
delay(5);
update_game_window();
}
```

The loop runs as long as the escape key is not pressed. The code inside the loop is executed repeatedly.

`delay(5);` is necessary for CPU usage optimization.

If you want to perform a task a specific number of times, you can use a while loop. Here's an example that runs a code block 1000 times:

```
int x=0;
while(x<1000)
{
// Put your code here.
x++;
}
```

## Do While Loops

Do while loops are similar but ensure that the code block is executed at least once. Here's an example:

```
do
{
update_game_window();
}
while(!key_pressed(SDLK_ESCAPE));
```

Unlike while loops, the condition is checked at the end of the loop. The exclamation mark before the condition indicates the loop should repeat as long as the condition is false.

## For Loops

For loops are powerful and mainly used for counting. They combine loop control elements into one statement. Here's an example:

```
for(uint x=0; x<=10; x++)
{
//loop code goes here.
}
```

The for statement includes initialization, loop continuation condition, and reassignment in a single line.

Here's another example with a different reassignment expression:

```
for(x=1; x<1000; x*=2)
{
//code goes here
}
```

## Break and Continue

There are scenarios where you might want to break out of a loop for various reasons. The following example shows the use of break and continue:

```
while(true)
{
if(something==true)
{
break;
}
if(something_else==true)
{
break;
}
if(yet_another_variable==true)
{
continue;
}
// more code here...
update_game_window();
}
```

The loop has no specific condition (while(true)), creating an endless loop. The break statement terminates the loop based on certain conditions, and the continue statement skips the rest of the cycle and moves to the next iteration.


# `file` and `filesystem` class

the `file` object is useful to read and write files on the disk. the `filesystem` object, on the other hand, is useful for performing additional actions on the files and folders.

## file

in this chapter, we'll explore the file class to read / write files on the disk.

### reading files

the simplest way to read the files is using the `read` method within the file object. consider the following example.

```
void main()
{
file f;
f.open("hello.txt","r");
string content=f.read(f.get_size());
f.close();
}
```

wait, wait, many new things here. lets get explained.

as you already know the usage of the main function, we'll skip the part.


`file f;`

this specifys the object as f.

`f.open("hello.txt","r");`

this tells the file object (f) in this case, to open `hello.txt`. the `r` character within the quotes tells the object to open as read mode.

`string content=f.read(f.get_size());`

this tells the object to read the contents from the file that is opened. the `get_size` method tells the read method to read all contents defined by its size. would you usually do this to read all contents from the file.

`f.close();`

this tells the object to close the current file, allowing to be used the object again. in short, the file object can be used over and over to read from file to file. you do not need to declare each object for each file. declaring each object for each file is not generally recommended as it reduces the over all performance of the script.


### writing to the files.

after we learned how to read from a file, lets continue on how to write into the file.

```
void main()
{
file f;
f.open("hello.txt","w");
f.write("hello world!");
f.close();
}
```

now, we used the open method to specify the file name. however, we now used the `w` character as open mode instead of the `r` character that we previously used. the `r` character means write.

next, we used the `write` method, specifying the contents that is to be written.

after executing the codes, move back to your disk window and you'll be able to see the `hello.txt` and content `hello world!` in it.

### file object methods

here are the list of methods of the file object. this could be out of date, so you should read the documentation on the file object.

function | description return value
---|---
open | opens the file to be read or write. it requires the filename, and the open mode(`r` or `w`) | 0 on success, -1 otherwise.
close | this function closes the file object. | 0 on success, -1 otherwise.
read | this function reads the contents from the currently opened file. it requires the length of the contents to be read, and using `get_size` method to read all contents otherwise. | the content of the file on success, an empty string otherwise.
write | this function writes the contents into the opened file. it requires the content that is to be written. this method can only work on the file opened in write mode. | 0 on success, -1 otherwise
get_size | this function returns the size of the file. | the size of the currently opened file on success, 0 otherwise.


## filesystem

after having we learned the file object, lets explore the filesystem object!

for the basics, the filesystem object can perform additional actions, such as checking the current path where the script is being executed, create / remove / copy / move directories and files.


# Using Multiple Scripts

As your game grows larger, managing everything within a single script becomes unmanageable. Hence, the necessity to utilize multiple scripts arises.

To begin, create several scripts. For example, consider two scripts: `game.ngt` and `dlg.ngt`:

* `game.ngt`: The main script for your game.
* `dlg.ngt`: Contains functionalities for dialog management.



Note: Only the main script (`game.ngt`) should contain the `void main()` function. Duplication of this function in other scripts could lead to engine failure.

Using multiple scripts involves importing functionalities from one script to another using the `#include "scriptname"` or `#include "path/to/scriptname"` directives. For instance, to import the `dlg` script into your `game` script:

```
#include "dlg.ngt"
```
After importing, you can utilize functions from the imported script within your main script. However, take caution to avoid conflicts. Do not create identical functions in multiple scripts. If a function exists in an imported script and is replicated in another, the engine will encounter conflicts and potentially fail.

Utilizing multiple scripts helps in organizing code, enhancing readability, and efficiently managing complex game structures in NGT.

# useful resources

[official website](https://ngtcode.dev)

[ngt official development repository](https://github.com/m1maker/NGT)

[ngt custom libraries repository](https://github.com/harrymkt/ngt-includes)

[ngt documentation repository](https://github.com/harrymkt/ngt-docs)
