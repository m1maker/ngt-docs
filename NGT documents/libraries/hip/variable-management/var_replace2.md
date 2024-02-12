# functions

This method is similar to the `var_replace` method, but here you can specify the actual replacers instead of just using numbers like 1, 2, 3.

## string var_replace2(string text, string[] fir, string[] sec)
variable | description
---|---
text| the text that is to be processed.
fir | the array of replacers.
sec | another array that contains the values to be replaced.

## return value

a string with the data.

## remarks

It's important to note that the `fir` and the `sec` arrays must be of the same length for the replacement to occur; otherwise, the rest of the text will be returned without any replacements. Additionally, the order of elements in both the `fir` and `sec` arrays should be the same; otherwise, incorrect replacements may occur.

## example

```
#include"hip.ngt"
void main()
{
string r;
string[] a;
string[] b;
string t="%name% has just incountored %object% on %date%.";
a={"%name%","%object%","%date%"};
b={"titanic,","an iceberg","April 14, 1912 at 11:40 PM"};
r=var_replace2(t,a,b,"{","}");
alert("ok",r);
}
```