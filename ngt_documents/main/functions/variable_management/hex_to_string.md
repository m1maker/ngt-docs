# functions

hex_to_string

This function converts a string of hexadecimal numbers into standard text.

# string hex_to_string(string the_hexadecimal_sequence)

## Parameters

variable | description
---|---
the_hexadecimal_sequence | The string of hexadecimal numbers that will be converted.

## Return value

A string containing the standard text equivalent of the given hexadecimal data, or an empty string on error.

## Remarks

Hexadecimal numbers range from 0 to 9, and then a (or A) to f (or F) to represent numbers 10 to 15. If other characters are used then a blank string is returned.

The converted string will be half the length of the given data.

## Example

```
void main()
{
alert("hex_to_string test", hex_to_string("412066726F6720697320626F756E63696E6720696E206D7920666F6F6421"));
}
```