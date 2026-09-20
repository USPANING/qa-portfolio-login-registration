# Bug report:Potential session state leak on invalid login attempt

 ## BUG ID
 BUG-02
 Previously authenticated session data remains accessible or persists when entering an incorrect password

 ## Environment
  * Application: ParaBank (`https://parabank.parasoft.com/`)
  * Browser: Google Chrome (version: 152.0.7977.84)
  * OS: Windows

  ## Preconditions
   1. User was previously logged into the application and then logged out (or attempted login).

  ## Steps to Reproduce
   1. Return to the home login page.
   2. Enter a valid username.
   3. Enter an incorrect/invalid password.
   4. Click the "Log In" button.

  ## Expected Result
   Authentication should fail, access should be denied, and the system should remain on the login page with an error notice.

  ## Actual Result
   The system bypasses authentication checks and redirects to the account overview page, exposing account data due to session persistence or server state caching.

  ## Severity & Priority
   * Severity: Major (Security / Session Integrity) — Unauthorized access to account data if session states overlap.
   * Priority: Medium — Observed in a shared training demo environment, but critical to document.

