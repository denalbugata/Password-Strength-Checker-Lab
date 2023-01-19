<h1>Password Strength Checker Lab</h1>

<h2>Description</h2>
This is a script that checks the strength of a given password. The script first imports the regular expression library (re) and defines the minimum password length. Next, it defines a function called "check_password_strength" which takes in a password as a parameter. The function checks the length of the password and makes sure it's at least 8 characters long. If the password is too short it returns "Too short". If the length is ok, it uses regular expressions to check if the password contains at least one uppercase letter, one lowercase letter, one digit and one special character, If any of these conditions is not met, it returns the corresponding message. If all the conditions passed, it returns "Strong". Finally, the script tests the function by taking a password as input and check the strength of the password by calling the function and printing the result.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 11</b>

<h2>Program Code:</h2>

```python
import re

# Step 1: Define the minimum password length
MIN_LENGTH = 8

# Step 2: Define the password checking function
def check_password_strength(password):
    # Step 2.1: Check the password length
    if len(password) < MIN_LENGTH:
        return "Too short"
    # Step 2.2: Check for the presence of at least one uppercase letter
    elif not re.search("[A-Z]", password):
        return "Missing uppercase letter"
    # Step 2.3: Check for the presence of at least one lowercase letter
    elif not re.search("[a-z]", password):
        return "Missing lowercase letter"
    # Step 2.4: Check for the presence of at least one digit
    elif not re.search("[0-9]", password):
        return "Missing digit"
    # Step 2.5: Check for the presence of at least one special character
    elif not re.search("[!@#\$%^&\*]", password):
        return "Missing special character"
    else:
        return "Strong"

# Step 3: Test the password checking function
password = input("Enter a password: ")
result = check_password_strength(password)
print(result)
```
