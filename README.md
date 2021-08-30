# is-your-password-safe

This python application checks if your entered password is safe and had not been exposed in previous data breaches.

Here, I have used https://haveibeenpwned.com API to check passwords previously exposed in data breaches. This exposure makes them unsuitable for ongoing use as they're at much greater risk of being used to take over other accounts.

This application ensures safety as only first 5 characters of hashed password are used to make API request which returns to local system all the matches of hashes and count of them found in leaks.

Then, remaining characters are compared with all the matches of hashes to find the required hash of our password and count of number of leaks.

In this way, it is a safe way to check safety of passwords locally without sending our complete password to https://haveibeenpwned.com

To use this application, first clone the repository in your system. You must have python installed in your system.

Then, install all the requirements using ( pip install -r requirements.txt )

And run the application using : ( python passwordchecker.py password1 password2 ...) where arguments after python passwordchecker.py are the passwords we want to check.
