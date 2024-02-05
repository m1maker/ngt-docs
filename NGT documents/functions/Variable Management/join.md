# functions

join

  


this function returns a string joined from array based on the seperater

# string join(string[] array, string sep)

## parameters

||| variable| description  
---|---  
array | an array to base  
sep | the seperater, such as \r\n for new line  
  
## return value

a string with the joined data on success, an empty string on failure

## remarks

none

## example


```
void main()
{
string[] a={"hello","world"};
string final=join(a, " ");
alert("final",final); //output should be hello world
}

```
