Category: [[Information Technology]] [[Cybersecurity]] [[Hacking]]
___
Injecting malicious SQL queries into a web app's database. 

### Example
How this is possible:
A website may have a vulnerable SQL query code in the background like:
SELECT * FROM users WHERE username = 'user123' AND password = 'password123'

An attacker could input this into the username field:
' OR '1'='1

Which makes the query:
SELECT * FROM users WHERE username = '' OR '1'='1' AND password = 'password123'

Since 1 is always = 1, the query bypasses authentication. 

