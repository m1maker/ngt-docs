# functions

hide_game_window

  


This function hides the main window of your game on the user's screen.  


# void hide_game_window()

## Parameters

None

## Return value

None

## Remarks

When the game window is invisible, the user is not able to set focus to it. This means that you will not be able to accept keyboard input before you call the show_game_window function.

## Example
    
    
    // Display the window for 3 seconds, hide it for 3 seconds, display it again for 3 seconds with another title and then exit.
    void main()
    {
    show_game_window("first");
    wait(3000);
    hide_game_window();
    wait(3000);
    show_game_window("second");
    wait(3000);
    }
    
