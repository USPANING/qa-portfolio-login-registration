- Test Checklist: ParaBank Login and Registration
   - Registration Module (/register.htm)
       * Verify that all mandatory fields display appropriate inline error messages when submitted empty
       * Verify error handling when `Password` and `Confirm` fields do not match
       * Verify successful user registration using valid dummy data (First Name, Last Name, Address, City, State, Zip Code, Phone, SSN, Username, Password)
       * Verify successful redirection and welcome message after registration
   - Login & Logout Module (`/index.htm`)
       * Verify successful login with valid registered credentials
       * Verify successful redirection to `Accounts Overview` page after login
       * Verify login behavior with an incorrect password and a valid username (Check system error response)
       * Verify login behavior with an unregistered username
       * Verify login behavior with empty username and/or password fields
       * Verify successful logout functionality using the `Log Out` button
