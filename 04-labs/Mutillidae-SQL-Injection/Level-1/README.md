
# OWASP Mutillidae II — SQL Injection

## Overview

I performed a hands-on SQL Injection exercise using **OWASP Mutillidae II**, an intentionally vulnerable web application designed for security training.

The objective was to understand how unsanitized user input can alter the application's SQL query and potentially allow authentication controls to be bypassed.

## Initial Testing

I first entered a single quote (`'`) into the login input.

The application returned a database-related error and exposed information about the underlying request/path. This indicated that the supplied input was being incorporated into a database query without being handled safely.

This was an initial indication that the login functionality could potentially be vulnerable to SQL Injection.

## SQL Injection — Low Security

I then tested the login functionality using SQL syntax designed to alter the application's authentication query.

The injection used a comment marker (`#`) to cause the remainder of the SQL statement to be ignored by the database.

The injected logic included a condition such as:

```text
' OR 1=1 #
```

The `1=1` expression evaluates to **TRUE**.

The `#` character acts as a comment marker in MySQL, causing the remaining portion of the SQL statement to be ignored.

As a result, the application's original password-checking logic could be bypassed in the vulnerable lab implementation.

## Result

The injection successfully bypassed the login authentication in the controlled Mutillidae II environment without providing the legitimate user's password.

This demonstrated how SQL Injection can affect authentication mechanisms when user input is directly incorporated into SQL queries.

## Why It Worked

The underlying issue was that user-controlled input was being incorporated into a SQL query without using an appropriate mechanism to separate **data from SQL instructions**.

Conceptually, the application's query could be influenced from:

```text
User input → SQL query → Database
```

Instead of treating the supplied value strictly as data, the vulnerable application allowed SQL syntax supplied through the input to influence the query's logic.

## Security Impact

Authentication-bypass SQL Injection can potentially allow an attacker to access accounts without knowing legitimate credentials.

Depending on the application's implementation and database privileges, SQL Injection may also potentially allow:

* Unauthorized access to database information
* Modification of database records
* Bypass of application controls
* Exposure of sensitive information
* Further compromise of the application

## Mitigation

The primary defense against SQL Injection is to use **parameterized queries / prepared statements**.

Additional protections include:

* Server-side input validation
* Avoiding dynamically constructed SQL queries
* Applying least-privilege database permissions
* Secure database access libraries
* Avoiding detailed database errors being exposed to users
* Proper security testing of database-driven functionality

## Key Takeaway

This exercise helped me understand SQL Injection from both an attack and defensive perspective.

I learned how a simple input such as a quote can reveal unsafe database interaction, and how SQL syntax and comment functionality can potentially alter an authentication query when user input is not properly parameterized.

## Evidence

Screenshots from the controlled Mutillidae II environment are included in the `screenshots/` directory.

All testing was performed against an intentionally vulnerable application for educational and cybersecurity training purposes.
