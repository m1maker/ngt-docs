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
		sound@ s;
		@s = null;
		alert("Active",""+s.active);
	}
	catch
	{
		alert("error", get_exception_info());
	}
	alert("engine","now exiting...");
}
```

Without try catch block, this will throw runtime error, because we're accessing the null object. But as you can see, the engine does not cause the runtime error and stop execution. Instead, it skippeds to the next code, more like continue we learned in the loops chapter, and manually exits the program.
