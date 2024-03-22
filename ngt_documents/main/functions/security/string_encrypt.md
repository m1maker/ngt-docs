# functions


string_encrypt

This function encrypts a string based on a provided key.

# string string_encrypt(string the_string, string encryption_key)

## Parameters

variable | description
---|---
the_string | The string to encrypt.
encryption_key | The key that will be used to encrypt and later decrypt the data.

## Return value

The encrypted string on success, or a blank string on failure.

## Remarks

This uses the AES-Rijndel 256-bit encryption algorithm, which is one of the most secure algorithms available to date. It has never been successfully cracked, and is used to protect files stored by various governments.

The encrypted string is a few bytes longer than its decrypted equivalent.

## Example

// Encrypt a string and print it.

```
void main()
{
string test=string_encrypt("I am an encrypted string.", "testkey");
alert("Encrypted string", test);
}
```