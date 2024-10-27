## Syntax
```angelscript
enum typeid {
    VOID,
    BOOL,
    INT8,
    INT16,
    INT32,
    INT64,
    UINT8,
    UINT16,
    UINT32,
    UINT64,
    FLOAT,
    DOUBLE,
    OBJHANDLE,
    HANDLETOCONST,
    MASK_OBJECT,
    APPOBJECT,
    SCRIPTOBJECT,
    TEMPLATE,
    MASK_SEQNBR
};
}
```

## Enum Values

### Basic Types
- **VOID (0)**: Represents the void type, which indicates that no value is present.
- **BOOL (1)**: Represents a boolean type, which can have two values: true or false.
- **INT8 (2)**: Represents an 8-bit signed integer type.
- **INT16 (3)**: Represents a 16-bit signed integer type.
- **INT32 (4)**: Represents a 32-bit signed integer type.
- **INT64 (5)**: Represents a 64-bit signed integer type.
- **UINT8 (6)**: Represents an 8-bit unsigned integer type.
- **UINT16 (7)**: Represents a 16-bit unsigned integer type.
- **UINT32 (8)**: Represents a 32-bit unsigned integer type.
- **UINT64 (9)**: Represents a 64-bit unsigned integer type.
- **FLOAT (10)**: Represents a single-precision floating-point number type.
- **DOUBLE (11)**: Represents a double-precision floating-point number type.

### Object Handles
- **OBJHANDLE (1073741824)**: Represents an object handle, which is a reference to an object in the scripting environment.

### Handle Types
- **HANDLETOCONST (536870912)**: Indicates that the handle points to a constant value.

### Object Masks
- **MASK_OBJECT (469762048)**: A mask used to identify the type of object being referred to.
- **APPOBJECT (67108864)**: Represents an application-specific object type.
- **SCRIPTOBJECT (134217728)**: Represents a generic script object type.

### Template Types
- **TEMPLATE (268435456)**: Represents a template type, which is used to define generic classes or functions.

### Sequence Number Mask
- **MASK_SEQNBR (67108863)**: A mask used for sequence numbers, often found in identifiers or versioning information.
