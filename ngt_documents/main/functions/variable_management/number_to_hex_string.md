# functions


number_to_hex_string

This function converts a number to its corresponding hexadecimal string representation.

# string number_to_hex_string(double the_number)

## Parameters

variable | description
---|---
the_number | The number to convert.

## Return value

A string containing the hexadecimal representation of the number, or an empty string on error.

## Remarks

This function only works with positive numbers, without decimals. If the number contains decimals, these will simply be removed without rounding.


## Example

```
void main()
{
alert("number_to_hex_string test", number_to_hex_string(1000)); // Output should be 3e8.
}
```