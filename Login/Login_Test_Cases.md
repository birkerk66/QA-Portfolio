#  Login & Authentication Test Cases

---

## TC-01: Verify successful user login with valid credentials

**Component:** Authentication / Login  
**Environment:** Cross-Browser (Chrome / Firefox / Safari)  
**Preconditions:** 
* A registered active user account exists in the database.
* User is on the login page (`/login`).

### Test Steps:
1. Open the login page (`/login`).
2. Enter a valid registered username/email.
3. Enter the corresponding valid password.
4. Click the **"Login"** button.

### Expected Result:
* User is successfully authenticated.
* Session/JWT token is created.
* User is redirected to the home page or dashboard (`/dashboard`).

### Postconditions:
* User enters an authenticated session state.

---

## TC-02: Verify system behavior when attempting login with an invalid password

**Component:** Authentication / Negative Testing  
**Environment:** Cross-Browser (Chrome / Firefox / Safari)  
**Preconditions:** 
* A registered active user account exists in the database.
* User is on the login page (`/login`).

### Test Steps:
1. Open the login page (`/login`).
2. Enter a valid registered username/email.
3. Enter an incorrect/invalid password.
4. Click the **"Login"** button.

### Expected Result:
* Authentication is denied.
* System displays an explicit error notification: *"Invalid username or password"*.
* User remains unauthenticated on the login page.
* Password input field is cleared for security.

### Postconditions:
* User remains in an unauthenticated state.

---

## TC-03: Verify field validation indicators on empty form submission

**Component:** Form Validation / UI Feedback  
**Environment:** Cross-Browser (Chrome / Firefox / Safari)  
**Preconditions:** User is on the login page (`/login`).

### Test Steps:
1. Open the login page (`/login`).
2. Leave the "Username" field completely blank.
3. Leave the "Password" field completely blank.
4. Click the **"Login"** button.

### Expected Result:
* Form submission is prevented on the client side.
* Inline error indicators appear below required inputs (e.g., *"Username is required"*, *"Password is required"*).
* No network authentication payload is transmitted.

### Postconditions:
* Login form retains focus without reloading or navigating away.

---

## TC-04: Verify username input handling with leading and trailing whitespaces

**Component:** Input Sanitization / Boundary Testing  
**Environment:** Cross-Browser (Chrome / Firefox / Safari)  
**Preconditions:** 
* Active user account exists with username: `user123`.
* User is on the login page (`/login`).

### Test Steps:
1. Open the login page (`/login`).
2. Enter the username with extra leading and trailing spaces (e.g., `" user123 "`).
3. Enter the correct valid password.
4. Click the **"Login"** button.

### Expected Result:
* System automatically sanitizes (trims) surrounding whitespace prior to backend submission OR displays a clear formatting error.
* User is successfully authenticated without string format failures.

### Postconditions:
* User is redirected to the authenticated dashboard area cleanly.
