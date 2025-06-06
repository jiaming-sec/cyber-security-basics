## Same origin policy (SOP)
Only accept requests from the same origin domain.
-  A fundamental security mechanism in browsers that restricts how scripts from one origin can interact with content from another origin.
-  **"Origin"** = scheme (http/https) + domain + port.
-  **Example**: JavaScript running on https://example.com cannot access content (like cookies, DOM, or local storage) from https://evil.com.
-  **Purpose**: Prevent cross-site attacks (e.g., stealing data from another site).
## CORS  (Cross-Origin Resource Sharing)
Cross-Origin Resource Sharing. Can specify allowed origins in HTTP headers. Sends a preflight request with options set asking if the server approves, and if the server approves, then the actual request is sent (eg. should client send auth cookies).
- Why it exists: SOP blocks cross-origin requests by default, but CORS provides a safe way to allow them.
- Browser sends a preflight request (OPTIONS) to the server asking: "Hey, can I access this resource?"
- Server responds with headers like Access-Control-Allow-Origin: https://example.com.
- If allowed, browser proceeds with the actual request.
- **Use case**: Frontend hosted on app.example.com wants to access an API on api.example.com.
## HSTS (HTTP Strict Transport Security)
- **What it does**: Tells browsers to only interact with a site over HTTPS, never HTTP.
- **Prevents:** SSL stripping attacks (downgrade attacks).
- **Sent via**: Strict-Transport-Security response header.
- **Example**: Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
## Cert transparency
- **What it is**: A public log of all TLS certificates issued by Certificate Authorities (CAs).
- **Why**: Helps detect rogue or mistakenly issued certs.
- **Tool example**: crt.sh lets you look up certificates for any domain.
## HTTP Public Key Pinning (HPKP)
- **Goal**: Prevent fake certificates from being trusted.
- **How**: A site would tell the browser: "Only trust certs signed by this public key."
- **Why Deprecated**: Misuse could brick a site if not handled correctly.
Deprecated by Google Chrome
## Cookies
httponly - cannot be accessed by javascript.
## CSRF (Cross-Site Request Forgery)
- **What it is**: Tricks a user into making an unwanted request (e.g., transferring money).
- **Relies on**: Authenticated cookies automatically sent by the browser.
- **Prevention:** Use CSRF tokens / Set SameSite on cookies / Use custom headers (e.g., X-CSRF-TOKEN).

## XSS (Cross-Site Scripting)
Web security vulnerability that allows attackers to inject malicious scripts (usually JavaScript) into legitimate websites or web applications.
The malicious code runs in the context of the victim’s browser, not the attacker’s.
- Reflected XSS.
- Persistent XSS.
- DOM based /client-side XSS.
- **Example**: &lt;img src=x onerror=alert(1)&gt;
- &lt;img scr=””&gt;will often load content from other websites, making a cross-origin HTTP request.
- **Prevention**:
- Encode output (<%= escapeHTML(input) %>)
- Use Content Security Policy (CSP)
## SQLi (SQL Injection)
- **What it is:** Injecting SQL commands into input fields to manipulate databases.
- **Example**: ' OR 1=1 --
- **Prevention:** Validation/sanitisation / Use parameterized queries

## The HTTP method tells the server what action the user wants to perform on the resource identified by the URL path. 
## POST
Sends data to the server, usually to create or update something.
- Form data.
- Always validate and clean the input to avoid attacks like SQL injection or XSS.
## GET
Used to fetch data from the server without making any changes.
- Queries.
- Visible from URL.
## Directory traversal
Find directories on the server you’re not meant to be able to see.
There are tools that do this.
## APIs
Think about what information they return.
And what can be sent.
## Beefhook
Get info about Chrome extensions.
## User agents
Is this a legitimate browser? Or a botnet?
## Browser extension take-overs
Malicious actors can hijack or replace browser extensions to perform:
Miners, cred stealers, adware.
## Local file inclusion
## Remote file inclusion (not as common these days)
## SSRF
Server Side Request Forgery.
## Web vuln scanners.
- Tools that automatically scan web apps for known issues.
## SQLmap.
- A powerful automated tool for SQL injection testing.
## Malicious redirects.
