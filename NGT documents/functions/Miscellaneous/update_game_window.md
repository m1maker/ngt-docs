# functions

update_game_window

  


This function updates the game window. See remarks.  


# void update_game_window()

## Parameters

None

## Return value

None

## Remarks

This function updates the game window, particularly useful within loops that run for extended periods, such as main game loops or while loops. It aids in normalizing CPU usage for your game. Failing to utilize this function may lead to your game consuming 100 percent of the CPU at all times.

## Example


```
void main()
{
show_game_window("game");
while(true)
{
update_game_window();
}
}

```
