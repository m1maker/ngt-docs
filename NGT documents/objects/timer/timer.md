# timer

timer object

  


The timer object is used to measure elapsed time.

# timer()

## Parameters

None.

## Remarks

Timer objects are mostly used inside loops to measure elapsed time, for example, to trigger events after a certain amount of time or at regular intervals.

Timer objects have high precision and do not significantly impact script execution even when used in large quantities.

The timer starts running instantly when created, and if used as global variables, it starts during script initialization. Call the restart method if precise timing is required later in the script.

## Example
    
    
    // Simple, wait for the users to press enter to exit.
    void main()
    {
    alert("Welcome", "On the next screen, you can press enter to exit.");
    show_game_window("Test Timer");
    timer c;
    while (true)
    {
    update_game_window();
    if (key_pressed(SDLK_RETURN))
    {
    c.pause();
    alert("OK", "The timer stopped and indicates that it was elapsed to " + c.elapsed_millis());
    break;
    }
    }
    quit();
    }
    
