# SauceDemo Bug Reports

---

## BUG-01: Login error message remains displayed after submitting valid credentials

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is on the Swag Labs login page (`https://www.saucedemo.com/`)  
**Severity:** Medium | **Priority:** Medium  

### Steps to Reproduce:
1. Click the "Login" button with empty Username and Password fields.
2. Verify the error message appears (*"Epic sadface: Username is required"*).
3. Enter valid credentials (`standard_user` / `secret_sauce`).
4. Click the "Login" button again.

### Expected Result:
- The error message banner disappears, and the user is redirected to the `/inventory.html` products page.

### Actual Result:
- The error message banner remains visible on screen after submitting valid credentials.

---

## BUG-02: Shopping cart items are cleared upon browser page refresh

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is logged in as `standard_user` and located on the `/inventory.html` page  
**Severity:** Medium | **Priority:** Medium  

### Steps to Reproduce:
1. Click "Add to cart" on any product (e.g., *Sauce Labs Backpack*).
2. Confirm the cart icon badge displays "1".
3. Refresh the browser page (F5 or Ctrl+R / Cmd+R).

### Expected Result:
- The shopping cart state is preserved after page refresh, and added items remain in the cart.

### Actual Result:
- The shopping cart resets to 0 items after page refresh, and added products disappear from the cart.

---

## BUG-03: First Name and Last Name fields accept special characters without validation during checkout

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User has added at least 1 item to the cart and navigated to the Checkout step (`/checkout-step-one.html`)  
**Severity:** Low | **Priority:** Low  

### Steps to Reproduce:
1. Navigate to the Checkout page.
2. Enter special characters (e.g., `<script>`, `!@#$%^&*()`) into the "First Name" and "Last Name" fields.
3. Enter a valid Zip/Postal Code.
4. Click "Continue".

### Expected Result:
- An inline validation error message is displayed indicating invalid name characters.

### Actual Result:
- The system accepts special characters without validation and proceeds to the Checkout Overview page (`/checkout-step-two.html`).
