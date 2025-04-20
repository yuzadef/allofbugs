## What is SQL injection (SQLi)?
SQL injection (SQLi) is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. This can allow an attacker to view data that they are not normally able to retrieve. This might include data that belongs to other users, or any other data that the application can access. In many cases, an attacker can modify or delete this data, causing persistent changes to the application's content or behavior.

https://portswigger.net/web-security/sql-injection#what-is-sql-injection-sqli

## What is the impact of SQL injection (SQLi)
A successful SQL injection attack can result in unauthorized access to sensitive data, such as:

- Passwords.
- Credit card details.
- Personal user information.

SQL injection attacks have been used in many high-profile data breaches over the years. These have caused reputational damage and regulatory fines. In some cases, an attacker can obtain a persistent backdoor into an organization's systems, leading to a long-term compromise that can go unnoticed for an extended period.

https://portswigger.net/web-security/sql-injection#what-is-the-impact-of-a-successful-sql-injection-attack

## SQL injection (SQLi) vulnerable point
1. Identifiers in URLs
- `/profile/@username` → `/profile/@username'+OR+1=1--+-`
- `/organisation/<orgId>` → `/organisation/<orgId>'+OR+1=1--+-`
- `/application/<appId>` → `/applications/<appId>'+OR+1=1--+-`
