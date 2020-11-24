The feddback session output received data directly to the browser without checking it for malicious code.
url: http://10.11.100.162/index.php?page=feedback

The attacker can insert a malicious string in the 'name' or 'message' that will be used within the web page and treated as source code by the victim’s browser.

## Explanation

* [acunetix web vulnerability solution](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) - Cross-site Scripting (XSS)
