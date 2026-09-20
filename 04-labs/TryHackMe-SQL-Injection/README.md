
# TryHackMe — SQL Injection

## Overview

Completed a TryHackMe room focused on understanding and exploiting SQL Injection vulnerabilities in a controlled lab environment.

**Platform:** TryHackMe
**Topic:** SQL Injection
**Status:** Completed — 100%

## Topics Covered

* Database fundamentals
* SQL fundamentals
* SQL Injection fundamentals
* In-Band SQL Injection
* Blind SQL Injection
* Authentication bypass
* Boolean-based Blind SQL Injection
* Time-based Blind SQL Injection
* Out-of-Band SQL Injection
* SQL Injection remediation

## What I Practiced

Throughout the room, I explored how improperly handled user input can affect SQL queries and how different SQL Injection techniques can be used depending on how the application responds.

I practiced:

* Understanding the structure of SQL queries
* Identifying SQL Injection opportunities
* Performing In-Band SQL Injection
* Understanding authentication bypass scenarios
* Using Boolean-based techniques when useful application output is limited
* Understanding Time-based Blind SQL Injection
* Learning the purpose of Out-of-Band SQL Injection
* Understanding defensive techniques for preventing SQL Injection

## Key Learning

One of the main things I learned was that SQL Injection is not limited to a single technique.

The approach depends heavily on how the vulnerable application responds to injected input. When database output is directly returned, In-Band techniques may be possible. When useful output is not returned, Blind SQL Injection techniques such as Boolean-based or Time-based approaches can provide alternative ways to infer information.

I also learned the importance of understanding the underlying SQL query rather than relying only on memorized payloads.

## Remediation

Key defensive measures include:

* Using parameterized queries / prepared statements
* Avoiding unsafe construction of SQL queries with user input
* Applying appropriate input validation
* Following least-privilege principles for database accounts
* Properly handling database errors
* Using secure frameworks and database access libraries

## Evidence

Screenshots from the completed lab are stored in the `screenshots/` directory.

> This work was performed in the authorized TryHackMe lab environment for educational and cybersecurity training purposes.
