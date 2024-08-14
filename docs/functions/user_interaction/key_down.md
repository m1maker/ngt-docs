# functions

key_down




This function checks if a particular key on the keyboard is currently being held down.


# bool key_down(int key)

## Parameters

variable| description
---|---
key | One of the NGT key name constants, see general/keys for a full list.

## Return value

true if the key is held down, false if it is not or if an error occurs.

## Remarks

The difference between key_down and key_pressed is that key_pressed will only return true when the user first pushes down the key, while key_down will continue returning true until the key is released again.

## Example

```
// Wait for the user to hold down alt and press f4 before closing the program.
void main()
{
show_game_window("Test Game");
while(true)
{
wait(5);
if(key_down(SDLK_LALT) && key_pressed(SDLK_F4))
{
exit();
}
// Other code goes here.
}
}
```
