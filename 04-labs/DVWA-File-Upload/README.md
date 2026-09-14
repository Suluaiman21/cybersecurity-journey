
# DVWA — File Upload

## Overview

This lab focused on understanding file upload vulnerabilities using the **Damn Vulnerable Web Application (DVWA)** in a controlled local environment.

I tested the File Upload functionality across the available DVWA security levels to understand how different validation and security controls affect the application's security.

## Objectives

* Understand the risks associated with insecure file upload functionality
* Test file upload behavior under different security configurations
* Observe how validation controls affect uploaded files
* Understand potential security impact
* Identify defensive techniques for securing file upload functionality

## Environment

* Application: Damn Vulnerable Web Application (DVWA)
* Vulnerability: File Upload
* Security Levels: Low, Medium, High, Impossible
* Environment: Controlled local lab
* Purpose: Educational security testing

## Testing Approach

The File Upload functionality was tested across multiple DVWA security levels.

The purpose was to compare how the application handled uploaded files as security controls became more restrictive.

### Low

The low-security configuration provided minimal protection around uploaded files, making it useful for understanding the basic security weakness.

### Medium

Additional validation controls were introduced. Testing this level helped demonstrate how basic restrictions can make exploitation more difficult but may still have limitations.

### High

Stronger validation mechanisms were introduced. This level helped demonstrate the importance of robust file validation rather than relying on a single client-side or easily bypassed check.

### Impossible

The highest security configuration provided significantly stronger protection and demonstrated how secure validation can reduce the risk associated with file uploads.

## Security Impact

An improperly secured file upload feature can potentially allow attackers to upload malicious or unexpected files to a server.

Depending on the application's configuration, this could potentially result in:

* Unauthorized file storage
* Execution of malicious files
* Application compromise
* Unauthorized access to server resources
* Further exploitation of the underlying system

## Mitigation

Secure file upload functionality should include:

* Strict allowlisting of permitted file types
* Server-side validation
* File content/type verification
* Safe file renaming
* Storing uploads outside executable web directories where possible
* Restricting uploaded file permissions
* Limiting file size
* Disabling execution of uploaded files
* Applying least-privilege principles

## Key Takeaway

Testing multiple security levels helped me understand that file upload security depends on strong server-side validation and secure storage, rather than relying on a single file extension or client-side check.

## Evidence

Screenshots from the controlled DVWA lab are included in the `screenshots/` directory.
