# dictionary

dictionary object

  


This method will retrieve a value based on the specified key.

# bool get(string key, ? &out value)

## Parameters

key - The key to look for.  
value - This should be the name of a variable of any type which will receive the value if it is found (see remarks).

## Return value

true on success, false on failure.

## Remarks

The value parameter is declared with the &out keyword since it is a parameter that the function will write to, not read from. Make certain that the value that you stored in the dictionary has the same type as the variable into which you tell the function to write the value, as a mismatch here will cause the function to fail.

## Example


```
dictionary game_board; // Declare our dictionary.
void main()
{
int value; // Declare a variable for retrieving values from the dictionary.
// Set our values.
game_board.set("1", 2); // Sets the value 2 to a key called 1.
game_board.set("2", 4); // Sets the value 4 to a key called 2.
game_board.get("1", value); // Retrieve value for 1.
alert("Dictionary example", "current value=" + value);
game_board.get("2", value); // Retrieve value for 2.
alert("Dictionary example", "current value=" + value);
game_board.delete_all(); // Delete all the values.
}

```
