# functions

This method enables dynamic variable replacement, making it useful for substituting a set of variables with specified values. Additional examples will be provided in the program, such as specifying sign messages in the map using placeholders like `%1%`, `%2%`, etc can be used.

## string var_replace(string text, string[] replacers, string opening, string closing)
variable | description
---|---
text| the text to process.
replacers | array of values to be replaced. optional
opening | the opening character. % is default.
closing | the closing character. % is default.

## return value

a string with the data.

## remarks

note that this method does not accept others. It will round from 1 to the length of what you give to the array. For instance, giving 4 elements to the array, it will be replaced from `%1%` to `%4%`. Do note that the `%` character is default; you can change it to other characters. See below example.

## example

```
//In this example, we used the left and right braces for the opening and closing variables. Copy the code below and try testing it:
#include"hip.ngt"
void main()
{
string r;
string[] b;
string t="{1} has just incountored {2} on {3}.";
b={"titanic,","an iceberg","April 14, 1912 at 11:40 PM"};
r=var_replace(t,b,"{","}");
alert("ok",r);
}
```
