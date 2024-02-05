# array

array object

  


This method finds a value in the array and returns the index.

# int find(uint start_index, ? value)

## Parameters

||| variable| description  
---|---  
start_index | The index to start searching from.  
value | The value to find.  
  
## Return value

The position of the value on success, and -1 on failure.

## Remarks

This method is overloaded, and can be called omitting the start_index parameter. If this is the case, start_index will be assumed to be 0.

The value parameter must match the data type being held by the array.

Please note: To search an array of classes, it is necessary for the class to overload the comparison operator.

## Example


```
// Declare an array and find a value, displaying its index.

void main()
{
string[] names(3);
names[0] = "ngt";
names[1] = "harry";
names[2] = "developer";
names.sort_asc(0, names.length());
int index = names.find("harry");
if(index < 0)
{
alert("Uh-oh", "Why can't we find harry?");
}
else
{
alert("Names", "harry is positioned at index " + index);
}
}

```
