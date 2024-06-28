# sound

sound object


This method will load an URL into memory for playback.

# bool load_url(string URL, bool hrtf)

## Parameters

Parameter| Description
---|---
URL | The URL to open.
hrtf | Toggle whether the URL should use HRTF.

## Return value

true on success, false on failure.

## Remarks

A loaded URL is completely put into memory when it is first created, utilizing more system memory but significantly reducing CPU usage. Loaded URLs are suitable for quick and frequent playback, such as footsteps, gunshots, or character noises. 

The engine optimizes memory usage by loading multiple instances of the same URL into memory only once, even when utilized by multiple objects. For example, having 50 enemies with two footsteps each won't load 100 independent URL objects into memory. 

## Example

```
// Load an URL into memory and play it.
void main()
{
sound test;
test.load_url("https://test.com/test.ogg", true);
test.play_wait();
test.close();
}
```