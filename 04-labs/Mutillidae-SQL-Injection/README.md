
# OWASP Mutillidae II — SQL Injection

## Overview

This lab focused on understanding **SQL Injection** using **OWASP Mutillidae II**, an intentionally vulnerable web application designed for security training.

The objective was to understand how insufficiently protected user input can influence database queries and potentially allow unintended database operations.

## Objectives

* Understand the fundamentals of SQL Injection
* Identify vulnerable input points in a web application
* Observe how user-controlled input can affect database queries
* Understand the potential impact of SQL Injection
* Learn defensive techniques for preventing SQL Injection

## Environment

* Application: OWASP Mutillidae II
* Vulnerability: SQL Injection
* Environment: Controlled local lab
* Purpose: Educational security testing

## What I Learned

During this lab, I investigated how SQL Injection can occur when an application incorporates user-controlled input into database queries without properly separating data from SQL instructions.

The lab helped me understand how an application's database interaction can become vulnerable when input is not handled securely.

## Security Impact

Depending on the application's database permissions and implementation, SQL Injection can potentially allow an attacker to:

* Access unauthorized database information
* Modify or manipulate database records
* Bypass certain application controls
* Perform unintended database operations
* Potentially compromise sensitive application data

## Mitigation

Common defenses against SQL Injection include:

* Using parameterized queries / prepared statements
* Avoiding dynamically constructed SQL queries with untrusted input
* Implementing appropriate server-side input validation
* Applying least-privilege permissions to database accounts
* Using secure database access libraries and frameworks
* Properly handling database errors without exposing sensitive information

## Key Takeaway

This lab strengthened my understanding of how application input can influence database queries and why parameterized queries and secure database access practices are fundamental defenses against SQL Injection.

## Evidence

Screenshots from the controlled Mutillidae II lab environment are included in the `screenshots/` directory.
