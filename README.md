# Password Bruteforce Script

This script attempts to brute force a login page by trying different passwords from a provided password file.

## Requirements

- Python 3.x
- `requests` library
- `termcolor` library

You can install the required libraries using pip:

```sh
pip install requests termcolor
```
## Usage
1. Clone the repository or download the script.
2. Run the script using Python:
```sh
python bruteforce.py
```
3. Provide the required inputs when prompted:
    * Page URL: The URL of the login page you want to brute force.
    * Username: The username for the account you want to brute force.
    * Password File: The path to the file containing the list of passwords to try.
    * Login Failed String: The string that appears on the page when a login attempt fails.
## Example
```sh
[+] Enter Page URL: http://example.com/login
[+] Enter Username For The Account To Bruteforce: admin
[+] Enter Password File To Use: passwords.txt
[+] Enter String That Occurs When Login Fails: Login failed
```
## How It Works
1. The script reads the provided password file line by line.
2. For each password, it sends a POST request to the provided URL with the username and password.
3. If the response does not contain the login failed string, it prints the found username and password and exits.
4. If the script reaches the end of the password file without finding the correct password, it prints a message indicating that the password was not found in the list.
## Disclaimer
This script is for educational purposes only. Do not use it to attack any system without permission. Unauthorized access to computer systems is illegal and unethical. 