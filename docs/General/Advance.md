# NGT Advance Tutorial
Once you have read the getting started tutorial, here is the Tutorial with more advance engine knowledge. I made 2 parts so any of you can decide whether to stop at getting started Tutorial or to take your engine knowledge to the advance level.

## Engine exceptions
engine exceptions are errors that catched using runtime error. You cannot possibly imagine that you can catch any runtime errors and avoid from being stopped execution, however here you really can!

### Throwing errors
The first thing we gonna learn is how to throw an exception, meaning to execute a runtime error.

To execute a heavy attack, I mean, the exception, you will use the throw function, like this.

```NGT copy
void main()
{
	throw("Engine died so go away");
}
```

After execution of the code, you will see that a runtime error had occured. To avoid this, we will catch it with try catch block.

```
void main()
{
	try
	{
		vector@ v;
		@v = null;
		alert("vector",""+v.x);
	}
	catch
	{
		alert("error", get_exception_info());
	}
	alert("engine","now exiting...");
}
```

Without try catch block, this will throw runtime error, because we're accessing the null object. But as you can see, the engine does not cause the runtime error and stop execution. Instead, it skippeds to the next code, more like continue we learned in the loops chapter, and manually exits the program.

## Any, datatype
An `any` type is used to point to any type of value. This is best to use in areas where you don't know exactly what type or value will be stored.

An `any` is an object

The following functions should be note before you read into examples.

* `void store(?value);` which stores the value of any kind.
* `bool retrieve(?&out value);` which trys to retrieve the value of the object.

Constructor

`any(?value);`

Now, lets dive into example. Lets say we have to use the speak function provided by NGT, but we stuck here because you want to speak many types, including strings, ints, floats, or possibly objects.

We will first implement the custom_speak function that supports string, int, float, bool.
Please note that in latest development, string accepts numbers passing too, so you don't have to actually implement this logic.

Note. If you want numbers of all types, using int and double is enough.

```
void custom_speak(any@ t, bool interrupt=false)
{
	if(t is null) return; //Null shouldn't even used here.
	string text; //Actual variable of a converted string, since the speak function accepts string.
	string r_str; //Lets retrieve the string.
	if(t.retrieve(r_str)) text=r_str;
	//If the string fail to retrieve, lets go to int and double, one after the other.
	int r_int;
	if(t.retrieve(r_int)) text=""+r_int;
	double r_db;
	if(t.retrieve(r_db)) text=""+r_db;
	//If either of above types is failed, lets retrieve bool.
	bool r_bool;
	if(t.retrieve(r_bool)) text=(r_bool?"true":"false");
	screen_reader::speak(text, interrupt); //Finally speaks the text.
}
```

Now, we've defined the speak custom function, with supporting string, bool, intiger and floatingpoint. Next, we'll use `any` object before specifying the t parameter in that speak function.

```
void main()
{
	custom_speak(any("hello"),true); //String.
	custom_speak(any(233),false); //Int
	custom_speak(any(23.21),false); //Floatingpoint.
	custom_speak(any(true),false); //Bool.
}
```

Yep, you found that useful, aren't you?

