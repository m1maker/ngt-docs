# dictionary

dictionary object

  


This method will check to see if a particular key exists in the dictionary.

# bool exists(string key)

## Parameters

key - The key to look for.

## Return value

true if the key was found, false if it was not or if an error occurred.

## Remarks

None.

## Example


```
dictionary game_board; // Declare our dictionary.
void main()
{
int value; // Declare a variable for retrieving values from a dictionary.
// Set our values.
game_board.set("1", 2); // Sets the value 2 to a key called 1.
game_board.set("2", 4); // Sets the value 4 to a key called 2.
if(game_board.exists("1"))
{
game_board.get("1", value); // Retrieve value for 1.
alert("Dictionary example", "Key 1 contains value " + value);
}
else
{
alert("Error", "Key 1 does not exist in the dictionary.");
}
game_board.delete_all(); // Delete all the values.
}

```
