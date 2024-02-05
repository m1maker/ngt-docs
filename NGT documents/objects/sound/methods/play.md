# sound

sound object

  


This method will start the sound playback.

# bool play()

## Parameters

None.

## Return value

true on success, false on failure.

## Remarks

This method initiates the sound playback and returns immediately, not waiting for the playback to finish. To determine when the sound has stopped, utilize the "is_playing()" method. 

## Example
    
    
    // Play a sound, and then manually wait for it to stop before exiting.
    void main()
    {
    init_engine();
    sound ambience;
    ambience.load("intro.ogg");
    if(!ambience.is_active())
    {
    alert("Error", "The sound could not be loaded.");
    quit();
    }
    ambience.play();
    while(ambience.is_playing())
    {
    update_game_window();
    }
    }
    
