
# DVWA — Command Execution

## Overview

This lab focused on understanding command execution vulnerabilities using the **Damn Vulnerable Web Application (DVWA)** in a controlled local environment.

The objective was to understand how user-controlled input can reach operating system commands and how insufficient input validation can allow unintended command execution.

## Objectives

* Understand the concept of command execution vulnerabilities
* Identify how user input is passed to system commands
* Observe the security impact of successful command execution
* Understand how input validation can reduce the attack surface
* Learn basic defensive measures against command execution vulnerabilities

## Environment

* Application: Damn Vulnerable Web Application (DVWA)
* Vulnerability: Command Execution
* Environment: Controlled local lab
* Purpose: Educational security testing

## What I Learned

During the lab, I investigated how an application can become vulnerable when user-supplied input is incorporated into operating system commands without sufficient security controls.

I also learned that allowing untrusted input to directly influence system-level commands can potentially allow an attacker to perform unintended actions on the underlying system.

## Security Impact

Successful command execution can potentially allow an attacker to:

* Execute unintended operating system commands
* Access information available to the application's user
* Interact with the underlying operating system
* Potentially compromise the application or host depending on privileges

## Mitigation

Common defensive measures include:

* Avoiding direct operating system command execution where possible
* Using safer APIs instead of shell commands
* Strict input validation and allowlisting
* Running applications with the minimum required privileges
* Avoiding direct use of unsanitized user input in system commands
* Monitoring and logging suspicious command execution

## Key Takeaway

This lab helped me understand the relationship between application input and operating system command execution, and why strong input validation and secure application design are important for preventing command injection vulnerabilities.

## Evidence

Screenshots from the controlled lab environment are included in the `screenshots/` directory.
