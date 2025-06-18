##  Mock Vulnerable Python Code (vulnerable_app.py)

python
import os
import sqlite3

# Hardcoded credentials
USERNAME = "admin"
PASSWORD = "123456"

# Unsafe input usage
user_input = input("Enter your username: ")
query = "SELECT * FROM users WHERE username = '" + user_input + "'"

# Dangerous function usage
eval("print('Hello " + user_input + "')")

# No input validation
age = input("Enter your age: ")
print(f"You are {age} years old.")

# Database connection
conn = sqlite3.connect('users.db')
cursor = conn.cursor()
cursor.execute(query)
results = cursor.fetchall()
print(results)


---

##  Static Code Analysis Report (Mocked Bandit Output)

| Issue                 | Location | Severity | Description                                |
| --------------------- | -------- | -------- | ------------------------------------------ |
| Use of eval()       | Line 10  | HIGH     | Allows arbitrary code execution            |
| SQL Injection Risk    | Line 8   | HIGH     | Query uses unsanitized input               |
| Hardcoded Credentials | Line 4-5 | MEDIUM   | Secrets should not be hardcoded            |
| No Input Validation   | Line 12  | LOW      | Inputs should be validated (e.g., isdigit) |

---

##  Secure Coding Review Document (Summary)

*Programming Language:* Python
*Application Type:* Mock login script
*Review Tools Used:* Manual inspection, Bandit (Python security linter)

###  Findings:

1. **Use of eval()**: Dangerous — can execute arbitrary user code.
2. *SQL Injection*: Unvalidated user input in SQL query.
3. *Hardcoded Credentials*: Sensitive data exposed in code.
4. *No Input Validation*: User inputs are used directly.

### Recommendations:

* Replace eval() with safe string formatting:

  python
  print(f"Hello {user_input}")
  
* Use parameterized SQL queries:

  python
  cursor.execute("SELECT * FROM users WHERE username = ?", (user_input,))
  
* Store credentials in environment variables:

  python
  USERNAME = os.getenv("APP_USERNAME")
  
* Validate user inputs:

  python
  if age.isdigit():
      print(f"You are {age} years old.")
  

### Remediation Steps:

* Remove eval() usage completely.
* Sanitize or parameterize all database inputs.
* Use a .env file or secrets manager.
* Add input checks for all user-provided data.
