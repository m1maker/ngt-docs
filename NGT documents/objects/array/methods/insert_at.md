# array

array object

  


This method will insert a new value at a specified position in an array.  


# void insert_at(int position, ? value)

## Parameters

||| variable| description  
---|---  
position | The index at which the new element should be inserted.  
value | A value of the specified type in the array declaration to place at that index.  
  
## Return value

None.

## Remarks

The method can only insert values from element 0 to the previous return value of length, that is to say one more than the upper boundary.

## Example


```
string[] names(1);

void main()
{
names[0]="harry";
names.insert_at(1,"ngt");
for(uint counter=0; counter<names.length(); counter++)
{
alert("Names", "Element "+counter+" contains the name "+names[counter]+".");
}
}

```
