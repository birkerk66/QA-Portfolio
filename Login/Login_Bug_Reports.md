#  Login & Authentication Bug Reports

---

## BUG-01: System authenticates user and grants access despite invalid password

**Component:** Authentication / Login  
**Environment:** Chrome v126 (Desktop), Windows 11  
**Preconditions:** 
* User account exists and is registered in the system database.
* User is on the Login page (`/login`).

**Severity:** High | **Priority:** High  

### Description:
Submitting a valid username with an incorrect/invalid password bypasses authentication checks, logging the user into the platform.

### Steps to Reproduce:
1. Open the Login page (`/login`).
2. Enter a registered valid username (e.g., `john_doe@example.com`).
3. Enter an incorrect password (e.g., `WrongPassword123!`).
4. Click the "Login" button.

### Expected Result:
* Authentication fails.
* System displays an explicit error message: *"Invalid username or password"*.
* User remains unauthenticated on the login page.

### Actual Result:
* Authentication succeeds without password verification.
* User is redirected to the authenticated dashboard/home page.

---

## BUG-02: Missing field validation indicators when submitting an empty login form

**Component:** Form Validation / UI Feedback  
**Environment:** Chrome v126 (Desktop), Windows 11  
**Preconditions:** User is on the Login page (`/login`)  
**Severity:** Medium | **Priority:** Medium  

### Description:
Submitting the login form with blank "Username" and "Password" fields provides no visual error feedback or validation messages to the user.

### Steps to Reproduce:
1. Open the Login page (`/login`).
2. Leave the "Username" and "Password" input fields completely empty.
3. Click the "Login" button.

### Expected Result:
* Form submission is blocked.
* Inline validation messages appear under required fields (e.g., *"Username is required"*, *"Password is required"*).

### Actual Result:
* No error banners or validation messages are displayed; the UI remains non-responsive to the submit action.

---

## BUG-03: Login process accepts unstripped leading and trailing spaces in username input

**Component:** Input Sanitization / User Management  
**Environment:** Chrome v126 (Desktop), Windows 11  
**Preconditions:** 
* Registered username: `user123`.
* User is on the Login page (`/login`).

**Severity:** Low | **Priority:** Low  

### Description:
The login form accepts usernames containing surrounding whitespace without trimming or sanitizing the input prior to backend processing.

### Steps to Reproduce:
1. Open the Login page (`/login`).
2. Enter the username with extra spaces before and after (e.g., `" user123 "`).
3. Enter the correct valid password.
4. Click the "Login" button.

### Expected Result:
* Frontend trims leading/trailing spaces automatically before submission OR returns a format validation error.

### Actual Result:
* User is logged in successfully without input trimming, allowing dirty string payloads into authentication handling.
