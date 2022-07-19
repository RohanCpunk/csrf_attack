Cross Site Request Forgery (CSRF)

Overview
Cross-Site Request Forgery (CSRF) is an attack that forces an end user to execute unwanted actions on a web application in which they’re 
currently authenticated. With a little help of social engineering (such as sending a link via email or chat), an attacker may trick the users
of a web application into executing actions of the attacker’s choosing. If the victim is a normal user, a successful CSRF attack can force the user 
to perform state changing requests like transferring funds, changing their email address, and so forth. If the victim is an administrative account, 
CSRF can compromise the entire web application.

Description
CSRF is an attack that tricks the victim into submitting a malicious request. It inherits the identity and privileges of the victim to perform 
an undesired function on the victim’s behalf (though note that this is not true of login CSRF, a special form of the attack described below).
For most sites, browser requests automatically include any credentials associated with the site, such as the user’s session cookie, IP address, 
Windows domain credentials, and so forth. Therefore, if the user is currently authenticated to the site, the site will have no way to distinguish 
between the forged request sent by the victim and a legitimate request sent by the victim.

CSRF attacks target functionality that causes a state change on the server, such as changing the victim’s email address or password, 
or purchasing something. Forcing the victim to retrieve data doesn’t benefit an attacker because the attacker doesn’t receive the response, 
the victim does. As such, CSRF attacks target state-changing requests.

An attacker can use CSRF to obtain the victim’s private data via a special form of the attack, known as login CSRF. The attacker forces 
a non-authenticated user to log in to an account the attacker controls. If the victim does not realize this, they may add personal data—such as 
credit card information—to the account. The attacker can then log back into the account to view this data, along with the victim’s activity 
history on the web application.

It’s sometimes possible to store the CSRF attack on the vulnerable site itself. Such vulnerabilities are called “stored CSRF flaws”. 
This can be accomplished by simply storing an IMG or IFRAME tag in a field that accepts HTML, or by a more complex cross-site scripting attack. 
If the attack can store a CSRF attack in the site, the severity of the attack is amplified. In particular, the likelihood is increased because the
victim is more likely to view the page containing the attack than some random page on the Internet. The likelihood is also increased because the 
victim is sure to be authenticated to the site already.

RESOURCES TO PRACTICE CSRF LABS
- PORTSWIGER 
- TRYHACKME
- KONTRA LABS
