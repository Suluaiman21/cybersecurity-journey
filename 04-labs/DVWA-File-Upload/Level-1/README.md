
# DVWA File Upload — Low Security Level

## Overview

I used the **Low security level** of Damn Vulnerable Web Application (DVWA) to investigate an insecure file upload vulnerability.

The objective was to understand what happens when a web application accepts uploaded files without adequate validation of the file type or content.

## Initial Testing

I first tested the upload functionality using files with different file formats.

The application accepted different file types without applying effective restrictions, indicating that the upload functionality lacked sufficient validation.

I then investigated the security impact of allowing server-side executable files to be uploaded.

## PHP Payload Demonstration

In the controlled DVWA environment, I used **Weevely** to generate a PHP-based payload and uploaded the resulting file through the vulnerable file-upload functionality.

The payload was configured with a password for the lab demonstration.

After the file was uploaded successfully and made accessible by the web server, I used Weevely to connect to the uploaded agent.

This provided an interactive interface through which I could interact with the vulnerable lab environment.

## What This Demonstrated

The exercise demonstrated why unrestricted file uploads can become significantly more dangerous when a web application allows executable server-side files to be uploaded.

Depending on the server configuration, an attacker may potentially:

* Upload unauthorized files
* Execute server-side code
* Access files available to the web-server process
* Enumerate the underlying environment
* Perform further actions using the privileges of the compromised application

## Root Cause

The vulnerability occurs because the application does not sufficiently validate or restrict uploaded files before storing them on the server.

Simply allowing an uploaded file based on its filename or extension is not sufficient protection.

## Mitigation

Secure file-upload functionality should include multiple layers of protection:

* Allowlist permitted file types
* Validate files on the server side
* Validate file content, not only the extension
* Rename uploaded files
* Store uploads outside executable web directories where possible
* Disable execution permissions for uploaded files
* Apply appropriate file-size restrictions
* Use least-privilege permissions
* Restrict access to uploaded files

## Key Takeaway

This lab demonstrated how an apparently simple file-upload weakness can potentially become a server-side code execution vulnerability when executable files are accepted and made accessible through the web server.

It reinforced the importance of **server-side validation, secure file storage, and preventing execution of uploaded files**.

## Evidence

Screenshots from the controlled DVWA environment are included in the `screenshots/` directory.

All testing was performed against an intentionally vulnerable application in a controlled lab environment for educational purposes.
