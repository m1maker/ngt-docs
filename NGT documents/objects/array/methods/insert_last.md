# array

array object

  


This method will insert a new value at the end of the array.  


# void insert_last(? value)

## Parameters

||| variable| description  
---|---  
value | A value of the specified type in the array declaration to place at that index.  
  
## Return value

None.

## Remarks

None.

## Example


```
string[] names;

void main()
{
names.insert_last("harry");
for(uint counter=0; counter<names.length(); counter++)
{
alert("Names", "Element "+counter+" contains the name "+names[counter]+".");
}
}

```
