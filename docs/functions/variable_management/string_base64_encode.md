# functions


string_base64_encode

This function returns the base64 representation of a string.

# string string_base64_encode(string the_string)

## Parameters

variable | description
---|---
the_string | The string that will be encoded.

## Return value

A string containing the base64 representation of the given string on success, or an empty string on error.

## Remarks

Base64 is a way in which to represent binary data in a textual format. This means that the NULL character, ASCII code 0, will never be present in a base64 encoded string, and thus it may be used to store binary data in situations where only text content is supported. Converting binary data to a hexadecimal representation accomplishes the same thing but base64 encoded strings are shorter than hexadecimal strings, and are thus more suitable when space is an issue.

## Example

```
void main()
{
string original="testing stuff!";
alert("Original", original);
string encoded=string_base64_encode(original);
alert("Encoded", encoded);
string decoded=string_base64_decode(encoded);
alert("Decoded", decoded);
}
```