# Test Cases: ParaBank Login & Registration

## 1. Registration Test Cases

### TC-REG-01: Successful user registration with valid data
* Preconditions: User is on the ParaBank home page
* Test Data: 
  * First Name: John
  * Last Name: Rab
  * Address: Test Street 1
  * City: Wroclaw
  * State: Dolnoslaskie
  * Zip Code: 50-001
  * Phone: 123456789
  * SSN: 111-22-3333
  * Username: testuser-johnrab
  * Password: Password123!
  * Confirm: Password123!
* Steps:
  1. Click on the "Register" link.
  2. Fill in all mandatory registration fields with valid dummy data.
  3. Enter matching passwords in "Password" and "Confirm" fields.
  4. Click the "Register" button.
* Expected Result: User is successfully registered, redirected to the welcome page, and a success message containing the username is displayed.
* Status: Passed

### TC-REG-02: Registration failure with empty mandatory fields
* Preconditions: User is on the Registration page (`/register.htm`).
* Test Data: None (leave all fields empty).
* Steps:
  1. Leave all input fields empty.
  2. Click the "Register" button.
* Expected Result: Form is not submitted. Individual inline error messages (e.g., "First name is required.", "Username is required.") appear under each empty mandatory field.
* Status: Passed

### TC-REG-03: Registration failure when passwords do not match
* Preconditions: User is on the Registration page.
* Test Data:
  * Password: Password123!
  * Confirm: Password999!
* Steps:
  1. Fill in all valid data except for the confirmation password.
  2. Enter a mismatched value in the "Confirm" field.
  3. Click the "Register" button.
* Expected Result: Form shows an error message indicating that passwords do not match.
* Status: Passed

---

## 2. Login & Logout Test Cases

### TC-LOG-01: Successful login with valid credentials
* Preconditions: A registered user account exists (e.g., `testuser_johndoe_01` / `Password123!`). User is on the home page.
* Test Data: 
  * Username: `testuser_johndoe_01`
  * Password: `Password123!`
* Steps:
  1. Enter valid username in the username field.
  2. Enter valid password in the password field.
  3. Click the "Log In" button.
* Expected Result: User is successfully authenticated and redirected to the `Accounts Overview` page (`/overview.htm`).
* **Status:** Passed

### TC-LOG-02: Unsuccessful login with incorrect password
* Preconditions: User is on the home page.
* Test Data:
  * Username: `testuser_johndoe_01`
  * Password: `WrongPassword`
* Steps:
  1. Enter a valid registered username.
  2. Enter an incorrect password.
  3. Click the "Log In" button.
* Expected Result: Login fails, and an error message is displayed (e.g., system shows an error notice).
* Status: Passed

### TC-LOG-03: Successful logout functionality
* Preconditions: User is logged into their account and viewing the dashboard.
* Test Data: None.
* Steps:
  1. Locate and click the "Log Out" link in the left navigation panel.
* Expected Result: User session is terminated, and the application redirects back to the main login home page (`/index.htm`).
* Status: Passed
