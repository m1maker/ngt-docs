# Context State Enum

## Overview
The `ctxstate` enum defines the different states that a context can be in within a software application. These states indicate the current status and execution flow of the context.

## Syntax
```angelscript
enum ctxstate {
    EXECUTION_FINISHED,
    EXECUTION_SUSPENDED,
    EXECUTION_ABORTED,
    EXECUTION_EXCEPTION,
    EXECUTION_PREPARED,
    EXECUTION_UNINITIALIZED,
    EXECUTION_ACTIVE,
    EXECUTION_ERROR
};
```

## Enum Values

- **EXECUTION_FINISHED (0)**: The context has completed its execution.
- **EXECUTION_SUSPENDED (1)**: The execution of the context has been temporarily paused.
- **EXECUTION_ABORTED (2)**: The execution of the context was aborted intentionally.
- **EXECUTION_EXCEPTION (3)**: An exception occurred during the execution of the context.
- **EXECUTION_PREPARED (4)**: The context has been prepared for execution but is not yet running.
- **EXECUTION_UNINITIALIZED (5)**: The context has not been initialized and is in an undefined state.
- **EXECUTION_ACTIVE (6)**: The context is currently executing.
- **EXECUTION_ERROR (7)**: There was an error during the initialization or setup of the context.
