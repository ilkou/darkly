## Cookies

### Definition

HTTP cookies, or internet cookies, are built specifically for Internet web browsers to track, personalize,
and save information about each user’s session.

### FLAG

if we check the BornToSec website's cookies (inspecter -> Application -> Storage -> Cookies),
we will notice a variable named `I_am_admin` with an encrypted value (in md5 for some reason),
we decrypt this md5 value to give us 'false', so we changed this value to the encrypted value of 'true'.

after refreshing the page (the browser will send the cookie back to the server with the new value) it gives us an alert with the flag !

### Problem

the name `I_am_admin` indicates that this variable is critical; admin privileges maybe !
some malicious people can use it so the server serve them pages dedicated to admins !

## Links

* [cookies definition](https://www.kaspersky.com/resource-center/definitions/cookies) -- What are Cookies
