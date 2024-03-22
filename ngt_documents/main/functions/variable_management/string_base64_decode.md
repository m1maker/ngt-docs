# functions


string_base64_decode

This function returns a string decoded from its base64 representation.

# string string_base64_decode(string base64_string)

## Parameters

variable | description
---|---
base64_string | The base64 string that will be decoded.

## Return value

A string containing the decoded content on success, or an empty string on error.

## Remarks

Base64 is a way in which to represent binary data in a textual format. This means that the NULL character, ASCII code 0, will never be present in a base64 encoded string and it may therefore be used to store binary data in situations where only text content is supported. Converting binary data to a hexadecimal representation accomplishes the same thing, but base64 encoded strings are shorter than hexadecimal strings and are thus more suitable when space is an issue.

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