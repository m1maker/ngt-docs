# SMTP Login Methods Enum

## Overview
The `smtp_login_method` enum defines various authentication methods that can be used with an SMTP server. Each method corresponds to a specific way of authenticating a user.

## Syntax
```angelscript
enum smtp_login_method {
    AUTH_NONE,
    AUTH_CRAM_MD5,
    AUTH_CRAM_SHA1,
    AUTH_LOGIN,
    AUTH_PLAIN,
    AUTH_XOAUTH2,
    AUTH_NTLM
};
```

## Enum Values
- **AUTH_NONE (0)**: No authentication.
- **AUTH_CRAM_MD5 (1)**: CRAM-MD5 authentication mechanism.
- **AUTH_CRAM_SHA1 (2)**: CRAM-SHA1 authentication mechanism.
- **AUTH_LOGIN (3)**: LOGIN authentication method.
- **AUTH_PLAIN (4)**: PLAIN authentication method.
- **AUTH_XOAUTH2 (5)**: XOAUTH2 authentication method, commonly used for Gmail.
- **AUTH_NTLM (6)**: NTLM authentication method.
