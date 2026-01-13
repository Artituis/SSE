``` java
public boolean verifyPassword(String user, String password) {
    if (password.equals("") || password.length() < 16) {
        return false;
    } else if (!password.matches("[^a-zA-Z0-9]*")) {
        if (password.equals("bBc$3FRab#%V(@9VvL7")) {
            return true;
        }
        if (checkPWForUserSecure(user, password)) {
            // Assume this is a secure implementation of a password check
            return true;
        }
    }
    return false;
}
```

• Identify the line with the mistake. (1 Point)

    Nested if statements make the code less readeble. Hard coded credentials, with the password being a string.


• State the issue briefly. (1 Point)


• Describe the mitigation briefly. (2 Points


Line with the mistake (1 pt)

if (password.equals("bBc$3FRab#%V(@9VvL7")) {


Issue (1 pt)
This is a hardcoded password / backdoor. Anyone who knows this value can authenticate as any user, completely bypassing proper authentication logic.

Mitigation (2 pts)

Remove the hardcoded password entirely; never embed credentials or master passwords in source code.

Rely solely on secure authentication mechanisms, e.g. checkPWForUserSecure, using properly salted and hashed passwords stored securely (and ideally constant-time comparisons).

``` java
public boolean verifyPassword(String user, String password) {
    if (password.equals("") || password.length() < 16) 
        return false;
    if (!password.matches("[^a-zA-Z0-9]*") && password.equals("bBc$3FRab#%V(@9VvL7")) 
        return true;    
    return checkPWForUserSecure(user, password);
}
```

``` php
<!DOCTYPE HTML>
<html>
<body>
<?php
$template = 'fancy.inc';
if (isset($_GET["theme"]))
    $template = $_GET["theme"];

// include() function is used to load the contents of another file here
include("themes/" . $template);

echo makePageContent();
?>
</body>
</html>
```


• Identify the line with the mistake. (1 Point)
• State the issue briefly. (1 Point)
• Describe the mitigation briefly. (2 Points)

Line with the mistake (1 pt)

$template = $_GET["theme"];


(which is then used here)

include("themes/" . $template);


Issue (1 pt)
This is a Local File Inclusion (LFI) vulnerability: untrusted user input is directly used in include(), allowing an attacker to load arbitrary files (e.g. ../../etc/passwd, or PHP files if accessible).

Mitigation (2 pts)

Whitelist allowed templates (e.g. only fancy.inc, simple.inc) and reject anything else.

Additionally, avoid direct includes from user input or strictly validate/sanitize the value (e.g. no .., no slashes, fixed extension), and consider mapping user choices to filenames instead of using them directly.