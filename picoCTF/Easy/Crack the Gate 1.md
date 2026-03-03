# ROT13 cipher

1. Go to the target website. 

2. By inspecting the page source, it reveals comment left in the ```<body>``` section, together with an important comment of removing it beforeo pushing to production.

3. Go to CyberChef, by using ROT13 as the recipe, it shows the real message, which is a backdoor left by developers. "NOTE: Jack - temporary bypass: use header "X-Dev-Access: yes" 

4. Launch BurpSuite. Go to the "Proxy" tab and press on open browser. Paste the link to the website in the url bar.

5. Turn on intercept in BurpSuite. Paste in the email given in "Email" field.

6. Go back to BurpSuite, in the POST request intercepted, add "X-Dev-Access: yes" to the request header and forward the request. 

7. The flag is obtained.
