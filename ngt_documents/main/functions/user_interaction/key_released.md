# functions

key_released




This function checks if a particular key on the keyboard has just been released.


# bool key_released(int key)

## Parameters

variable| description
---|---
key | One of the NGT key name constants, see general/keys for a full list.

## Return value

true if the key has just been released, false if it has not or if an error occurs.

## Remarks

The key_released will return true when the user first releases the key.

## Example

```
// Speak a message when the space bar is released.
void main()
{
show_game_window("Test Game");
while(true)
{
update_game_window();
if(key_pressed(SDLK_SPACE))
{
speak("Space bar pressed.");
}
if(key_released(SDLK_SPACE))
{
speak("Space bar released.");
}
if(key_pressed(SDLK_ESCAPE))
{
quit();
}
// Other code goes here.
}
}
```
