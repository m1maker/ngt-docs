# functions


string_decrypt

This function decrypts a string previously encrypted by string_encrypt.

# string string_decrypt(string the_string, string encryption_key)

## Parameters

variable | description
---|---
the_string | The string to decrypt.
encryption_key | The key that will be used to decrypt the data. This must be the same key given when the string was encrypted.

## Return value

The decrypted string on success, or a blank string on failure.

## Remarks

The input string must match the string returned by string_encrypt. If you have converted the string to hexadecimal for printing, it is essential that you use hex_to_string to convert it back before using string_decrypt.

## Example

// Decrypt a string and print it.

```
void main()
{
string test=string_encrypt("testing string","testkey");
test=string_decrypt(test,"testkey");
alert("Decrypted string", test);
}
```