# array

array object

This method reserves memory ready for holding items in an array object.

# void reserve(uint size)

## Parameters

||| variable| description  
---|---  
size | The reserve size of the array.  
  
## Return value

None.

## Remarks

If memory is already reserved for the array, and you call it with a number greater than your previous one, it will increase the reserved memory. If the number is less than your original size, it will have no effect. 

Please note: calling the reserve method on the array only reserves the amount of memory needed internally to hold the data and is used mainly to increase performance when using the insert methods. To change the number of indexes that can be used to access the array, please use the resize method instead. 

## Example


```
// Compare performance between two arrays. One does not reserve memory, the other one does.

void main()
{
timer counter;
int[] list;
int[] list2;
for(int i=0;i<100000;i++)
list.insert_last(i);
alert("First result", "Time elapsed without reserved memory: " + counter.elapsed + " milliseconds.");
list.resize(0);
counter.restart();
list2.reserve(100000);
for(int i=0;i<100000;i++)
list2.insert_last(i);
alert("Second result", "Time elapsed with reserved memory: " + counter.elapsed + " milliseconds.");
}

```
