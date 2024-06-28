# sound

sound object

  


This method will load a sound into memory for playback.

# bool load(string filename, bool hrtf)

## Parameters

Parameter| Description  
---|---  
filename | The file to open.  
hrtf | Toggle whether the sound should use HRTF.  
  
## Return value

true on success, false on failure.

## Remarks

A loaded sound is completely put into memory when it is first created, utilizing more system memory but significantly reducing CPU usage. Loaded sounds are suitable for quick and frequent playback, such as footsteps, gunshots, or character noises. 

The engine optimizes memory usage by loading multiple instances of the same sound into memory only once, even when utilized by multiple objects. For example, having 50 enemies with two footsteps each won't load 100 independent sound objects into memory. 

## Example
    
    
    // Load a sound into memory and play it.
    void main()
    {
    init_engine();
    sound test;
    test.load("c:\\windows\\media\\ding.wav", true);
    test.play_wait();
    test.close();
    }
    
