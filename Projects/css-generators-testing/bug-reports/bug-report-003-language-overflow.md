## BUG-03: Language selector button text overflows boundaries on mobile viewports

**Component:** Header / Localization UI  
**Environment:** Chrome DevTools Mobile Viewport (iPhone 12 / 390x844px), Android Chrome  
**Preconditions:** User is viewing the mobile header layout  
**Severity:** Medium | **Priority:** Medium  

### Description:
When a long language label or extended string is applied to the mobile language selector button, the text overflows past the button container instead of truncating.

### Steps to Reproduce:
1. Open the site in a mobile viewport (e.g., 390x844px).
2. Locate the language selector button adjacent to the "Sign In" control.
3. Switch language or simulate a long string input (e.g., localizing to a language with longer words).
4. Observe the language button container.

### Expected Result:
* Long text is properly contained, truncated with an ellipsis (`...`), or wrapped without breaking header layout.

### Actual Result:
* Text overflows past the right border of the button, overlapping adjacent header elements.

**Evidence:** `[Screenshot](./evidence/bug-03-language-overflow.png)`
