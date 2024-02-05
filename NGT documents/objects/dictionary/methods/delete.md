# dictionary

delete

  


This method will attempt to delete a particular key and value pair.  


# bool delete(string key)

## Parameters:

||| variable| description  
---|---  
key | The key to look for.  
  
## Return value:

true on success, false on failure.

## Remarks:

None.

## Example:


```
dictionary game_board; // Declare our dictionary.

void main()
{
// Set our values.
game_board.set("1", 2);
game_board.set("2", 4);
game_board.delete("1");
}

```
