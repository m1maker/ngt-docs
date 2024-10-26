## File Transfer Protocol (FTP)

### `void ftp_download(const string&in url, const string&in filename)`
- **Parameters**:
  - `url` (const string&): The URL of the file to download.
  - `filename` (const string&): The local path and filename where the downloaded file will be saved.
- **Description**: Downloads a file from an FTP server using the specified URL and saves it locally.

## Simple Mail Transfer Protocol (SMTP)

### `void mail_send(smtp_login_method, uint port, const string&in username, const string&in password, const string&in mailhost, const string&in sender, const string&in recipient, const string&in subject, const string&in content, const string&in attachment = "")`
- **Parameters**:
  - `login_method` (smtp_login_method): The method for logging into the SMTP server.
  - `port` (uint): The port number on which to connect to the SMTP server.
  - `username` (const string&): The username for authentication with the SMTP server.
  - `password` (const string&): The password for authentication with the SMTP server.
  - `mailhost` (const string&): The hostname of the SMTP server.
  - `sender` (const string&): The sender's email address.
  - `recipient` (const string&): The recipient's email address.
  - `subject` (const string&): The subject of the email.
  - `content` (const string&): The content of the email.
  - `attachment` (const string&): An optional attachment to include in the email.
- **Description**: Sends an email using SMTP with the specified parameters. If an attachment is provided, it will be included in the email.
