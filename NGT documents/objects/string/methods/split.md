# string

string object

  


This method returns an array with the split parts.

# string[] split(string split_text)

## Parameters

||| variable| description  
---|---  
split_text | The text you want to split the part with. For instance, \r\n for a new line, any text and any character to split. An instance would be using this method to split words.  
  
## Return Value

An array with the splitted items on success, an empty array on failure.

## Remarks

None.

## Example


```
// Split words with spaces.
void main()
{
string a = "hello world";
string[] list = a.split(" ");
// We now have an array of splitted items divided with space.
}

```
