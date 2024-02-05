# array

array object

  


This method returns the length of the array.  


# uint length()

## Parameters

None.

## Return value

The length of the array, or 0 if the array is empty or if an error occurs.

## Remarks

Please note that the value returned is the length of the array rather than the last element index in the array. Therefore when using the length method as a basis for a loop it is important that you check that any variable counting through the array stops when the counter reaches the length mark, not beyond it. This is because the index is 0 based. In other words, with an array containing 3 entries you may access elements 0, 1 and 2.

## Example


```
// Declare an array and display its values.

void main()
{
string[] names(2);
names[0]="harry";
names[1]="ngt";
alert("Count", "The array contains " + names.length() + " elements.");
for(int counter=0; counter<names.length(); counter++)
{
alert("Names", "Element "+counter+" contains the name "+names[counter]+".");
}
}

```
