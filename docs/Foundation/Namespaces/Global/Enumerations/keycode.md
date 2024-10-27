# keycode Enum

## Overview
The `keycode` enum provides a mapping of keyboard keys to their corresponding integer values. This allows you to easily identify and handle different keys in your NGT application.

## Syntax
```angelscript
enum keycode {
    KEY_UNKNOWN,
    KEY_A = 4,
    KEY_B = 5,
    KEY_C = 6,
    KEY_D = 7,
    KEY_E = 8,
    KEY_F = 9,
    KEY_G = 10,
    KEY_H = 11,
    KEY_I = 12,
    KEY_J = 13,
    KEY_K = 14,
    KEY_L = 15,
    KEY_M = 16,
    KEY_N = 17,
    KEY_O = 18,
    KEY_P = 19,
    KEY_Q = 20,
    KEY_R = 21,
    KEY_S = 22,
    KEY_T = 23,
    KEY_U = 24,
    KEY_V = 25,
    KEY_W = 26,
    KEY_X = 27,
    KEY_Y = 28,
    KEY_Z = 29,
    KEY_1 = 30,
    KEY_2 = 31,
    KEY_3 = 32,
    KEY_4 = 33,
    KEY_5 = 34,
    KEY_6 = 35,
    KEY_7 = 36,
    KEY_8 = 37,
    KEY_9 = 38,
    KEY_0 = 39,
    KEY_RETURN = 40,
    KEY_ESCAPE = 41,
    KEY_BACK = 42,
    KEY_TAB = 43,
    KEY_SPACE = 44,
    KEY_MINUS = 45,
    KEY_EQUALS = 46,
    KEY_LEFTBRACKET = 47,
    KEY_RIGHTBRACKET = 48,
    KEY_BACKSLASH = 49,
    KEY_NONUSHASH = 50,
    KEY_SEMICOLON = 51,
    KEY_APOSTROPHE = 52,
    KEY_GRAVE = 53,
    KEY_COMMA = 54,
    KEY_PERIOD = 55,
    KEY_SLASH = 56,
    KEY_CAPSLOCK = 57,
    KEY_F1 = 58,
    KEY_F2 = 59,
    KEY_F3 = 60,
    KEY_F4 = 61,
    KEY_F5 = 62,
    KEY_F6 = 63,
    KEY_F7 = 64,
    KEY_F8 = 65,
    KEY_F9 = 66,
    KEY_F10 = 67,
    KEY_F11 = 68,
    KEY_F12 = 69,
    KEY_PRINTSCREEN = 70,
    KEY_SCROLLLOCK = 71,
    KEY_PAUSE = 72,
    KEY_INSERT = 73,
    KEY_HOME = 74,
    KEY_PAGEUP = 75,
    KEY_DELETE = 76,
    KEY_END = 77,
    KEY_PAGEDOWN = 78,
    KEY_RIGHT = 79,
    KEY_LEFT = 80,
    KEY_DOWN = 81,
    KEY_UP = 82,
    KEY_NUMLOCKCLEAR = 83,
    KEY_NUMPAD_DIVIDE = 84,
    KEY_NUMPAD_MULTIPLY = 85,
    KEY_NUMPAD_MINUS = 86,
    KEY_NUMPAD_PLUS = 87,
    KEY_NUMPAD_ENTER = 88,
    KEY_NUMPAD_1 = 89,
    KEY_NUMPAD_2 = 90,
    KEY_NUMPAD_3 = 91,
    KEY_NUMPAD_4 = 92,
    KEY_NUMPAD_5 = 93,
    KEY_NUMPAD_6 = 94,
    KEY_NUMPAD_7 = 95,
    KEY_NUMPAD_8 = 96,
    KEY_NUMPAD_9 = 97,
    KEY_NUMPAD_0 = 98,
    KEY_NUMPAD_PERIOD = 99,
    KEY_NONUSBACKSLASH = 100,
    KEY_APPLICATION = 101,
    KEY_POWER = 102,
    KEY_NUMPAD_EQUALS = 103,
    KEY_F13 = 104,
    KEY_F14 = 105,
    KEY_F15 = 106,
    KEY_F16 = 107,
    KEY_F17 = 108,
    KEY_F18 = 109,
    KEY_F19 = 110,
    KEY_F20 = 111,
    KEY_F21 = 112,
    KEY_F22 = 113,
    KEY_F23 = 114,
    KEY_F24 = 115,
    KEY_EXECUTE = 116,
    KEY_HELP = 117,
    KEY_MENU = 118,
    KEY_SELECT = 119,
    KEY_STOP = 120,
    KEY_AGAIN = 121,
    KEY_UNDO = 122,
    KEY_CUT = 123,
    KEY_COPY = 124,
    KEY_PASTE = 125,
    KEY_FIND = 126,
    KEY_MUTE = 127,
    KEY_VOLUMEUP = 128,
    KEY_VOLUMEDOWN = 129,
    KEY_NUMPAD_COMMA = 133,
    KEY_NUMPAD_EQUALSAS400 = 134,
    KEY_INTERNATIONAL1 = 135,
    KEY_INTERNATIONAL2 = 136,
    KEY_INTERNATIONAL3 = 137,
    KEY_INTERNATIONAL4 = 138,
    KEY_INTERNATIONAL5 = 139,
    KEY_INTERNATIONAL6 = 140,
    KEY_INTERNATIONAL7 = 141,
    KEY_INTERNATIONAL8 = 142,
    KEY_INTERNATIONAL9 = 143,
    KEY_LANG1 = 144,
    KEY_LANG2 = 145,
    KEY_LANG3 = 146,
    KEY_LANG4 = 147,
    KEY_LANG5 = 148,
    KEY_LANG6 = 149,
    KEY_LANG7 = 150,
    KEY_LANG8 = 151,
    KEY_LANG9 = 152,
    KEY_ALTERASE = 153,
    KEY_SYSREQ = 154,
    KEY_CANCEL = 155,
    KEY_CLEAR = 156,
    KEY_SDL_PRIOR = 157,
    KEY_RETURN2 = 158,
    KEY_SEPARATOR = 159,
    KEY_OUT = 160,
    KEY_OPER = 161,
    KEY_CLEARAGAIN = 162,
    KEY_CRSEL = 163,
    KEY_EXSEL = 164,
    KEY_NUMPAD_00 = 176,
    KEY_NUMPAD_000 = 177,
    KEY_THOUSANDSSEPARATOR = 178,
    KEY_DECIMALSEPARATOR = 179,
    KEY_CURRENCYUNIT = 180,
    KEY_CURRENCYSUBUNIT = 181,
    KEY_NUMPAD_LEFTPAREN = 182,
    KEY_NUMPAD_RIGHTPAREN = 183,
    KEY_NUMPAD_LEFTBRACE = 184,
    KEY_NUMPAD_RIGHTBRACE = 185,
    KEY_NUMPAD_TAB = 186,
    KEY_NUMPAD_BACKSPACE = 187,
    KEY_NUMPAD_A = 188,
    KEY_NUMPAD_B = 189,
    KEY_NUMPAD_C = 190,
    KEY_NUMPAD_D = 191,
    KEY_NUMPAD_E = 192,
    KEY_NUMPAD_F = 193,
    KEY_NUMPAD_XOR = 194,
    KEY_NUMPAD_POWER = 195,
    KEY_NUMPAD_PERCENT = 196,
    KEY_NUMPAD_LESS = 197,
    KEY_NUMPAD_GREATER = 198,
    KEY_NUMPAD_AMPERSAND = 199,
    KEY_NUMPAD_DBLAMPERSAND = 200,
    KEY_NUMPAD_VERTICALBAR = 201,
    KEY_NUMPAD_DBLVERTICALBAR = 202,
    KEY_NUMPAD_COLON = 203,
    KEY_NUMPAD_HASH = 204,
    KEY_NUMPAD_SPACE = 205,
    KEY_NUMPAD_AT = 206,
    KEY_NUMPAD_EXCLAM = 207,
    KEY_NUMPAD_MEMSTORE = 208,
    KEY_NUMPAD_MEMRECALL = 209,
    KEY_NUMPAD_MEMCLEAR = 210,
    KEY_NUMPAD_MEMADD = 211,
    KEY_NUMPAD_MEMSUBTRACT = 212,
    KEY_NUMPAD_MEMMULTIPLY = 213,
    KEY_NUMPAD_MEMDIVIDE = 214,
    KEY_NUMPAD_PLUSMINUS = 215,
    KEY_NUMPAD_CLEAR = 216,
    KEY_NUMPAD_CLEARENTRY = 217,
    KEY_NUMPAD_BINARY = 218,
    KEY_NUMPAD_OCTAL = 219,
    KEY_NUMPAD_DECIMAL = 220,
    KEY_NUMPAD_HEXADECIMAL = 221,
    KEY_LCTRL = 224,
    KEY_LSHIFT = 225,
    KEY_LALT = 226,
    KEY_LGUI = 227,
    KEY_RCTRL = 228,
    KEY_RSHIFT = 229,
    KEY_RALT = 230,
    KEY_RGUI = 231,
    KEY_MODE = 257,
    KEY_MEDIA_NEXT_TRACK = 267,
    KEY_MEDIA_PREVIOUS_TRACK = 268,
    KEY_MEDIA_STOP = 269,
    KEY_MEDIA_PLAY = 262,
    KEY_MEDIA_SELECT = 272,
    KEY_AC_SEARCH = 280,
    KEY_AC_HOME = 281,
    KEY_AC_BACK = 282,
    KEY_AC_FORWARD = 283,
    KEY_AC_STOP = 284,
    KEY_AC_REFRESH = 285,
    KEY_AC_BOOKMARKS = 286,
    KEY_MEDIA_EJECT = 270,
    KEY_SLEEP = 258,
    KEY_MEDIA_REWIND = 266,
    KEY_MEDIA_FAST_FORWARD = 265,
    KEY_SOFTLEFT = 287,
    KEY_SOFTRIGHT = 288,
    KEY_CALL = 289,
    KEY_ENDCALL = 290
};
```

## Enum Values
- **KEY_UNKNOWN (0)**: Represents an unknown or unspecified key.
- **KEY_A - KEY_Z (4 to 32)**: Represents the letters A through Z.
- **KEY_1 - KEY_0 (30 to 39)**: Represents the digits 1 through 0.
- **KEY_RETURN (40)**: Represents the Enter or Return key.
- **KEY_ESCAPE (41)**: Represents the Escape key.
- **KEY_BACK (42)**: Represents the Backspace key.
- **KEY_TAB (43)**: Represents the Tab key.
- **KEY_SPACE (44)**: Represents the Space key.
- **KEY_MINUS (45)**: Represents the - or _ key.
- **KEY_EQUALS (46)**: Represents the = or + key.
- **KEY_LEFTBRACKET (47)**: Represents the [ or { key.
- **KEY_RIGHTBRACKET (48)**: Represents the ] or } key.
- **KEY_BACKSLASH (49)**: Represents the \ or | key.
- **KEY_NONUSHASH (50)**: Represents an unused key on non-US keyboards.
- **KEY_SEMICOLON (51)**: Represents the ; or : key.
- **KEY_APOSTROPHE (52)**: Represents the ' or " key.
- **KEY_GRAVE (53)**: Represents the ` or ~ key.
- **KEY_COMMA (54)**: Represents the , or < key.
- **KEY_PERIOD (55)**: Represents the . or > key.
- **KEY_SLASH (56)**: Represents the / or ? key.
- **KEY_CAPSLOCK (57)**: Represents the Caps Lock key.
- **KEY_F1 - KEY_F24 (58 to 135)**: Represents the Function keys F1 through F24.
- **KEY_PRINTSCREEN (70), KEY_SCROLLLOCK (71), KEY_PAUSE (72)**: Represents the Print Screen, Scroll Lock, and Pause/Break keys.
- **KEY_INSERT (73), KEY_HOME (74), KEY_PAGEUP (75)**: Represents the Insert, Home, and Page Up keys.
- **KEY_DELETE (76), KEY_END (77), KEY_PAGEDOWN (78)**: Represents the Delete, End, and Page Down keys.
- **KEY_RIGHT (79), KEY_LEFT (80), KEY_DOWN (81), KEY_UP (82)**: Represents the Arrow keys (Right, Left, Down, Up).
- **KEY_NUMLOCKCLEAR (83), KEY_NUMPAD_DIVIDE (84), KEY_NUMPAD_MULTIPLY (85), KEY_NUMPAD_MINUS (86), KEY_NUMPAD_PLUS (87), KEY_NUMPAD_ENTER (88)**: Represents the Num Lock and Numeric keypad keys.
- **KEY_NUMPAD_0 - KEY_NUMPAD_9 (89 to 97)**: Represents the numeric keypad digits.
- **KEY_NUMPAD_PERIOD (99)**: Represents the Decimal key on the numeric keypad.
- **KEY_NONUSBACKSLASH (100), KEY_APPLICATION (101), KEY_POWER (102), KEY_NUMPAD_EQUALS (103), KEY_F13 - KEY_F24 (104 to 115)**: Represents additional keys found on non-US keyboards and on modern computers with a numeric keypad.
- **KEY_EXECUTE (116), KEY_HELP (117), KEY_MENU (118), KEY_SELECT (119), KEY_STOP (120), KEY_AGAIN (121), KEY_UNDO (122), KEY_CUT (123), KEY_COPY (124), KEY_PASTE (125), KEY_FIND (126)**: Represents various function keys and commands.
- **KEY_MUTE (127), KEY_VOLUMEUP (128), KEY_VOLUMEDOWN (129)**: Represents the Volume Control keys.
- **KEY_NUMPAD_COMMA (133), KEY_NUMPAD_EQUALSAS400 (134), KEY_INTERNATIONAL1 - KEY_INTERNATIONAL9 (135 to 143)**: Represents additional keys found on some non-US keyboards and in certain operating systems.
- **KEY_LANG1 - KEY_LANG9 (144 to 152)**: Represents language-specific function keys.
- **KEY_ALTERASE (153), KEY_SYSREQ (154), KEY_CANCEL (155), KEY_CLEAR (156), KEY_SDL_PRIOR (157), KEY_RETURN2 (158), KEY_SEPARATOR (159)**: Represents various control and function keys.
- **KEY_OUT (160), KEY_OPER (161), KEY_CLEARAGAIN (162), KEY_CRSEL (163), KEY_EXSEL (164)**: Represents additional control keys.
- **KEY_NUMPAD_00 - KEY_NUMPAD_OCTAL (176 to 219)**: Represents additional numeric keypad keys and functions.
- **KEY_NUMPAD_DECIMAL (220), KEY_NUMPAD_HEXADECIMAL (221)**: Represents the Decimal and Hexadecimal mode buttons on some numeric keypads.
- **KEY_LCTRL - KEY_RGUI (224 to 231)**: Represents the Left Control, Right Control, Left Shift, Right Shift, Left Alt, and Right Alt keys.
- **KEY_MODE (257)**: Represents the Mode or Compose key.
- **KEY_MEDIA_NEXT_TRACK (267), KEY_MEDIA_PREVIOUS_TRACK (268), KEY_MEDIA_STOP (269), KEY_MEDIA_PLAY (262), KEY_MEDIA_SELECT (272)**: Represents media control keys such as Next Track, Previous Track, Stop, Play/Pause, and Select.
- **KEY_AC_SEARCH (280), KEY_AC_HOME (281), KEY_AC_BACK (282), KEY_AC_FORWARD (283), KEY_AC_STOP (284), KEY_AC_REFRESH (285), KEY_AC_BOOKMARKS (286)**: Represents Action Center keys.
- **KEY_MEDIA_EJECT (270)**: Represents the Eject media key.
- **KEY_SLEEP (258)**: Represents the Sleep key.
- **KEY_MEDIA_REWIND (266), KEY_MEDIA_FAST_FORWARD (265)**: Represents Rewind and Fast Forward media control keys.
- **KEY_SOFTLEFT (287), KEY_SOFTRIGHT (288)**: Represents Soft Left and Right navigation buttons on some devices.
- **KEY_CALL (289), KEY_ENDCALL (290)**: Represents the Call and End Call keys.
