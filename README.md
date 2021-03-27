# Using the Tesla API with Postman

## Authentcation
The authentication sequence follows the sequence outlined [here](https://tesla-api.timdorr.com/api-basics/authentication).  Familarity with Postman is recommended.

### Step 1: Request Log In Page

USER PREPARATION: Enter the email address used to access your Telsa account in the parameter named login_hint.  Save this change.

#### Documentation

The Pre-request Script creates the code verifier and code challenge required for the API calls.

The Tests extract hidden form variables from the response and store them in the envrionment for subsequent calls.
 
