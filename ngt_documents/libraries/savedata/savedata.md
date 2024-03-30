# savedata

savedata object

the savedata object allows you to manage your game progresses to load and save.

# savedata(string filename, string enckey, int tt)

## parameters

variable | description
---|---
filename | the filename to save and load.
key | an optional key to the file to be encrypted.
tt | an optional type of the save data, default is savedata_def

## remarks

this class provides saving and loading data, probably used on games to save the progress.

this class supports multiple save types.

by default, the savedata_def type is used.

it is however not advised to use INI for saving many data, for example in game messages, because INI is used new line and = seperater and therefore with the data with line break will potentially end up with unexpected data incorrection.

## example

```
#include"savedata.ngt"
savedata sd("config.ini","",savedata_ini);
double s=-1;
timer f;
void main()
{
s=-1;
loadsd();
if(s>-1) alert("previously","the timer is "+s);
show_game_window("test data",600,400,false);
wait(2000);
speak("press escape to exit");
while(true)
{
delay(5);
update_game_window();
if(key_pressed(SDLK_ESCAPE))
{
savesd();
alert("ok","saved");
exit();
}
}//while
exit();
}
void loadsd()
{
sd.load();
if(sd.exists("time")) s=sd.readn("time");
}
void savesd()
{
sd.clear();
sd.add("time",f.elapsed_seconds);
sd.save();
}
```