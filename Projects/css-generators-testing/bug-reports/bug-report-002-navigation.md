## BUG-02: Intermittent HTTP 502 Bad Gateway error during generator navigation

**Component:** Frontend Navigation / API Backend  
**Environment:** Chrome v126 (Desktop), Chrome Mobile Viewport  
**Preconditions:** User is on the "Functions" section page  
**Severity:** High | **Priority:** High  

### Description:
Rapidly switching between generator pages causes navigation failure or an intermittent HTTP `502 Bad Gateway` error response from the server.

### Steps to Reproduce:
1. Open the website and navigate to the "Functions" section.
2. Click through multiple generator options sequentially (e.g., *Grid Generator* → *Favicon Generator* → *CSS Optimization*).
3. Observe page loading behavior and DevTools Network tab.

### Expected Result:
* Each generator button smoothly navigates to its target URL without server errors or hanging requests.

### Actual Result:
* Navigation freezes on certain clicks, or the browser displays a `502 Bad Gateway` error page. Behavior is inconsistent and requires a hard refresh.

**Evidence:** `[Screenshot / Logs](./evidence/bug-02-502-error.png)`
