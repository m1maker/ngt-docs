# string

string object

  


The string object is used to store text.

# string()

## Parameters

None.

## Remarks

The string object contains overloaded operators which allow it to be assigned, compared, and accessed like any other variable. Additionally, it allows access to each individual character by way of indexes specified in square brackets, similar to arrays. Strings are unique in that they can be declared and used as variables, or they can be passed back and forth as literal values. Please see the String Variables chapter in the getting started Tutorial for in-depth information regarding strings. 

## Example


```
void main()
{
string name = "NGT";
alert("example", "The name " + name + " is " + name.length() + " characters long.");
}

```
