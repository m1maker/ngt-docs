# array

array object

  


This method will reverse the order of the array.  


# void reverse()

## Parameters

None.

## Return value

None.

## Remarks

None.

## Example


```
// Declare an array and reverse the order, displaying the results.

void main()
{
string[] names(3);
names[0] = "a";
names[1] = "b";
names[2] = "c";
names.reverse();
for (int counter = 0; counter < names.length(); counter++)
{
alert("Names", "Element " + counter + " contains the name " + names[counter] + ".");
}
}

```
