## Enums

### applicationtype
- **WINDOW**: Indicates that the application should run in a graphical window.
- **CONSOLE**: Indicates that the application should run in a console environment.

### msgtype
- **MESSAGE**: Generic message type.
- **WARNING**: Indicates a warning condition.
- **ERROR**: Indicates an error condition.

## Classes

### class application
This is the core class of the application. It manages initialization, logging, and running operations.

#### Members
- `iostream @output`: The stream used for outputting messages.
- `applicationtype system = applicationtype::WINDOW`: Specifies whether the application runs in a window or console.
- `@application_instance`: A singleton instance of the `application` class.

#### Methods

1. **constructor**():
   - Ensures that only one instance of `application` is created using the singleton pattern. Throws an error if more than one instance is attempted to be created.

2. **log(const string&in text, const msgtype&in message_type = msgtype::MESSAGE)**:
   - Logs a message based on the provided text and message type.
   - If the `message_type` is `WARNING`, prepends "Warning:".
   - If the `message_type` is `ERROR`, prepends "Error:".
   - Depending on the `system` type (WINDOW or CONSOLE), it either uses `screen_reader::speak()` to read the message aloud or outputs it using `cout` or `cerr`.

3. **initialize()**:
   - A placeholder method that can be overridden by subclasses for initialization tasks.

4. **uninitialize()**:
   - A placeholder method that can be overridden by subclasses for cleanup tasks.

5. **main(array<string> @args)**:
   - The entry point of the application, which should be overridden by subclasses to implement specific functionality.
   - Returns 0 by default.

6. **run()**:
   - Calls the `initialize()` method and then the `main()` method with command-line arguments.
   - Catches any exceptions that occur during initialization and logs them using the `log()` method before returning -1.
   - Finally, calls `uninitialize()` and returns the result of the `main()` method.

## Main Function

The main function (`int main()`) serves as the entry point for the application. It checks if an instance of `application` has been created and logs an error if it hasn't. It then attempts to initialize the application and run it, handling any exceptions that may occur during initialization.

### Error Handling
- If the `application_instance` is null when accessing it in the main function, it throws an exception indicating a null application instance.
- During the initialization of the application, any exceptions caught are logged using `log()` and result in the application returning -1.

## Usage

To use this code, you would typically create a subclass of `application`, override the `main()` method to implement your application logic, and potentially modify the `initialize()`, `uninitialize()`, and `run()` methods as needed. The singleton pattern ensures that there is only one instance of the application running, which can be accessed through `@application_instance`.
