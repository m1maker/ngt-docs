# dictionary

dictionary object

  


This method will delete all key and value pairs currently present in the dictionary.

# bool delete_all()

## Parameters

None.

## Return value

true on success, false on failure.

## Remarks

This method clears all key-value pairs present in the dictionary, effectively resetting it. 

## Example


```
// Set some values, then delete them all.
dictionary game_board; // Declare our dictionary.

void main()
{
// Set our values.
game_board.set("1", 2); // Sets the value 2 to a key called 1.
game_board.set("2", 4); // Sets the value 4 to a key called 2.
game_board.delete_all(); // Delete all the values.
}

```
