# sound

sound object

  


This method will pause the sound playback.

# bool pause()

## Parameters

None.

## Return value

true on success, false on failure.

## Remarks

This method stops the playback of the sound without resetting its position to the beginning of the file. When the "play" method is called again, the sound will resume from the exact point where it was paused. 

## Example
    
    
    // Play a sound and let the user pause and unpause it with the space bar, stop it with enter and exit with escape.
    void main()
    {
    init_engine();
    sound ambience;
    show_game_window("Sound Test");
    ambience.load("intro.wav");
    if(!ambience.is_active())
    {
    alert("Error", "The sound could not be loaded.");
    quit();
    }
    ambience.play();
    while(true)
    {
    update_game_window();
    if(key_pressed(SDLK_SPACE))
    {
    if(ambience.is_playing())
    {
    ambience.pause();
    }
    else
    {
    ambience.play();
    }
    }
    if(key_pressed(SDLK_RETURN))
    {
    ambience.stop();
    }
    if(key_pressed(SDLK_ESCAPE))
    {
    break;
    }
    }
    quit();
    }
    
