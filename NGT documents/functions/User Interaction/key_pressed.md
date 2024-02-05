# functions

key_pressed

  


This function checks if a particular key on the keyboard has just been pushed down.  


# bool key_pressed(int key)

## Parameters

||| variable| description  
---|---  
key | One of the NGT key name constants, see general/keys for a full list.  
  
## Return value

true if the key has just been pushed down, false if it has not or if an error occurs.

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
update_game_window();
if(key_down(SDLK_LALT) && key_pressed(SDLK_F4))
{
quit();
}
// Other code goes here.
}
}

```
