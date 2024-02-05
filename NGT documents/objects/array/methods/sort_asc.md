# array

array object

  


This method sorts the items in an array in ascending order.  


# void sort_asc(uint start_index, uint count)

## Parameters

||| variable| description  
---|---  
start_index | The index to begin sorting from.  
count | The number of elements to sort.  
  
## Return value

None.

## Remarks

This method is overloaded, and can be called with no parameters. If this is the case, the entire array will be sorted.

The start_index parameter is 0-based.

Please note: To sort an array of classes it is necessary for the class to overload the comparison operator.

## Example


```
// Declare an array, sort its values and display them. We will use the extended declaration to show how to manually sort the array.

void main()
{
string[] names(2);
names[0] = "harry";
names[1] = "ngt";
names.sort_asc(0, names.length());
for (int counter = 0; counter < names.length(); counter++)
{
alert("Names", "Element " + counter + " contains the name " + names[counter] + ".");
}
}

```
