# CommonPasswords.js

This JavaScript plugin allows you to check a user-set password against a list of the 10,000 most commonly-used passwords and reject it if desired.

**Dependencies**: None

**Installation**: Include the script normally:

```<script src="js/common-passwords.js"><script>```

**Usage**: Use the commonPasswords.isCommon() function to check if a given password is commonly used, e.g.:

```
    $('form').submit(function(e) {
        e.preventDefault();
        var password = $('#password').val();
        if (commonPasswords.isCommon(password) === true) {
            // tell the user to pick a better password
        }
    });
```

The function will return ```true``` if the password is commonly used, and ```false``` if it is not.

**Options**: You can optionally pass an integer 'cutoff' argument to the function; this argument specifies how deeply into the list you want to look. For example, 

```commonPasswords.isCommon('trustno1', 1000);```

Will return ```true``` if 'trustno1' is among the top 1000 most common passwords. 