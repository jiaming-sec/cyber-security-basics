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
Policies, eg what websites use HTTPS.
## Cert transparency
Can verify certificates against public logs
## HTTP Public Key Pinning
(HPKP)
Deprecated by Google Chrome
## Cookies
httponly - cannot be accessed by javascript.
## CSRF
Cross-Site Request Forgery.
Cookies.
## XSS
Reflected XSS.
Persistent XSS.
DOM based /client-side XSS.
<img scr=””> will often load content from other websites, making a cross-origin HTTP request.
## SQLi
Person-in-the-browser (flash / java applets) (malware).
Validation / sanitisation of webforms.

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
Miners, cred stealers, adware.
## Local file inclusion
## Remote file inclusion (not as common these days)
## SSRF
Server Side Request Forgery.
## Web vuln scanners.
## SQLmap.
## Malicious redirects.
