# sound

sound object

# properties

variable| description  
---|---  
pan | The pan of the sound, between -100 and 100. This property can be used to get or set. 0 is default.
pitch | The pitch of the sound. This property can be used to get or set. 100 is default.
volume | The volume of the sound, where 0 is maximum and -100 is silent. This property can be used to get or set.
active | Returns whether the sound is currently associated with a sound, meaning it is active. This property cannot be modified from the script.
playing | Returns whether the sound is currently playing. This property cannot be modified from the scriptt.
paused | Returns whether the sound is currently paused. This property cannot be modified from the script.
volume_step | sets the volume step.
pan_step | sets the pan step.
pitch_step | sets the pitch step.
position | get the current position of the sound.
length | get the total length of the sound in milliseconds. this property can also be set, which means the sound will cut its length.
hrtf | sets the use of hrtf