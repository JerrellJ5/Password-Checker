# Password Checker Program 
<p align="center">
<img src="https://i.imgur.com/ue4lZNt.png" alt="Traffic Examination"/>
</p>

<h1>Password Checker Code</h1>


import re

password = input("Enter Your Password:   ")
errors = []

# Check if the password is at least 8 characters long
if len(password) < 8:
    errors.append("Password must be at least 8 characters long.")

# Check if the password contains at least one uppercase letter
if not re.search("[A-Z]", password):
    errors.append("Password must contain at least one uppercase letter.")

# Check if the password contains at least one lowercase letter
if not re.search("[a-z]", password):
    errors.append("Password must contain at least one lowercase letter.")

# Check if the password contains at least one number
if not re.search("[0-9]", password):
    errors.append("Password must contain at least one number.")

# Output the result
if errors:
    print("Your password has the following issues:")
    for error in errors:
        print("- " + error)
else:
    print("Password is strong.")
