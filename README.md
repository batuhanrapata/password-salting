# password-salting
My own Password Salting Module


This is a code snippet written in Python that includes two functions for hashing and verifying passwords.

The create_salt function generates a random salt for hashing passwords. The salt is created by selecting random characters from a string of allowed characters, SALT_CHARS.

The hash function takes a password as input, creates a new salt using the create_salt function, and concatenates the salt with the password. The resulting string is then hashed using the SHA-256 algorithm from the hashlib library. The function returns a list containing the hashed password and the salt used for hashing.

The verify function takes a hashed password and a password provided by a user as input. The function retrieves the salt used for hashing from the hashed password, concatenates the salt with the provided password, and hashes the resulting string using the SHA-256 algorithm. The function then compares the resulting hash with the hash stored in the hashed password. If the two hashes match, the function returns True, indicating that the password is correct. Otherwise, it returns False.

It's important to note that when storing passwords, it's considered a best practice to use salted hashing to protect against common attacks, such as dictionary attacks or rainbow table attacks. Salting the password adds a random string of characters to the password before hashing, making it more difficult for attackers to use precomputed hashes to crack passwords.
