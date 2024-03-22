# functions


string_to_hex

This function returns the hexadecimal equivalent of a string.

# string string_to_hex(string the_string)

## Parameters

variable | description
---|---
the_string | The string that will be converted.

## Return value

A string containing the hexadecimal equivalent of the given string, or an empty string on error.

## Remarks

Given the nature of a hexadecimal string, the converted string will be twice the length of the source string. Therefore care must be taken if converting considerably large strings.

## Example

```
void main()
{
alert("string_to_hex test", string_to_hex("testing stuff!"));
}
```