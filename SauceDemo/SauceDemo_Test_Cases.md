# SauceDemo Test Cases

---

## TC-01: Successful user login with valid credentials

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is on the Swag Labs login page (`https://www.saucedemo.com/`)  

### Steps:
1. Open the login page.
2. Enter valid username (`standard_user`).
3. Enter valid password (`secret_sauce`).
4. Click the "Login" button.

### Expected Result:
- User is successfully authenticated and redirected to the `/inventory.html` products page.

---

## TC-02: Add a single product to the shopping cart

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is logged in as `standard_user` and located on the inventory page  

### Steps:
1. Navigate to the inventory page.
2. Click the "Add to cart" button for any product item.

### Expected Result:
- The product button changes to "Remove".
- The shopping cart icon badge updates to show "1".

---

## TC-03: Remove a product from the shopping cart

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is logged in and has 1 item in the shopping cart  

### Steps:
1. Open the inventory page or cart page (`/cart.html`).
2. Click the "Remove" button next to the added product.

### Expected Result:
- The product is removed from the cart list.
- The cart icon badge counter decreases or disappears if empty.

---

## TC-04: Complete full checkout workflow successfully

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is logged in and has at least 1 product added to the cart  

### Steps:
1. Click the shopping cart icon to open `/cart.html`.
2. Click the "Checkout" button.
3. Fill in required user information (First Name, Last Name, Zip/Postal Code).
4. Click "Continue".
5. Review the order summary on `/checkout-step-two.html` and click "Finish".

### Expected Result:
- Order is placed successfully, and user sees the order confirmation header (*"Thank you for your order!"*).

---

## TC-05: Checkout attempt with empty required fields

**Environment:** Chrome v126 (Desktop), macOS / Windows 11  
**Preconditions:** User is logged in, has 1 item in cart, and is on the Checkout Information page (`/checkout-step-one.html`)  

### Steps:
1. Leave First Name, Last Name, and Zip/Postal Code fields empty.
2. Click the "Continue" button.

### Expected Result:
- Form submission is blocked.
- An error banner appears stating: *"Error: First Name is required"*.
