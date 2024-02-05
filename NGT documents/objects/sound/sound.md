# sound

sound

  


The sound object is used to play audio stored either as Wav or Ogg.

# sound()

## Parameters

None

## Remarks

When a sound object is first created, it will not be active. To activate it, you must call the "load" method on the object, specifying a file that should be associated, and specifying whether HRTF should apply. You may call these methods again at any time if you wish to associate another sound with the object, at which point the old association (if any) will be cleared. This, in short, allows you to reuse the same sound object for playing more than one sound.

## Example
    
    
    // Load a sound into memory and play it.
    
    void main()
    {
    init_engine();
    sound test;
    test.load("c:\\windows\\media\\ding.wav",false);
    test.play_wait();
    test.close();
    }
    
