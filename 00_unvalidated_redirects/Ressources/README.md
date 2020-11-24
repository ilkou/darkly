the link to social media (bottom of page) is not protected and can be manipulated, for example http://{IP}/index.php?page=redirect&site=https://www.not-trusted-website.com

the attacker may send this link to users that trusts your website, your website will redirect them to the fake website "https://www.not-trusted-website.com" and maybe ask them for their crendentials !

## Explanation

* [cheatsheetseries owasp](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) - Unvalidated_Redirects_and_Forwards
