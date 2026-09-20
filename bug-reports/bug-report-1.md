# Bug report: Cryptic system error displayed on invalid password login

 ## BUG ID
 BUG-01
 Internal server error message is displayed when attempting login with incorrect password

 ## Environment
  * Application: ParaBank (`https://parabank.parasoft.com/`)
  * Browser: Google Chrome (version: 152.0.7977.84)
  * OS: Windows

 ## Preconditions
  1. User is on the ParaBank home page (`/parabank/index.htm`)
  2. A valid username exists in the system
 
 ## Steps to Reproduce
  1. Enter a valid registered username in the Username field
  2. Enter an incorrect (invalid) password in the Password field
  3. Click the "Log In" button

 ## Expected Result
 The system should display a clear, user-friendly validation message, such as *"The username and password could not be verified."* or *"Invalid username or password."*

 ## Actual result
 The system redirects or displays a generic, alarming error message: *"Error! An internal error has occurred and has been logged"*

 ## Severity & Priority
   Severity: Minor (or Trivial) — Core functionality (login blocking) works correctly, but user experience and error messaging are misleading  
   Priority: Low - Does not block users from testing or using the site, but represents poor practice in security/error handling
 ##  Evidence/Notes
   This error message mimics a server-side crash/exception notice rather than a standard authentication failure notification.
