# Using the Tesla API with Postman

## Authentcation
The authentication sequence follows the sequence outlined [here](https://tesla-api.timdorr.com/api-basics/authentication).  Familarity with [Postman](https://www.postman.com/) is recommended.

### Step 1: Request Log In Page

USER PREPARATION: Enter the email address used to access your Telsa account in the parameter named login_hint.  Save this change before clicking Send.

#### Documentation

All parameters have been defined.  Update the login_hint as described in USER PREPARATION.

The Pre-request Script creates the code verifier and code challenge required for the API calls.

The Tests extract hidden form variables from the response and store them in the envrionment for subsequent calls.

### Step 2: Obtain Authorization Code

### Step 3: Exchange Authentication Code for Bearer Token

### Step 4: Exchange Bearer Token for Access Token

## Using the APIs

The APIs make use of the Bearer Token that was provided through the steps executed in Authentication.  If the Bearer Token is not available, API calls will fail.

### Get Vehicles

NOTE: Use Get Vehicles first.

The Get Vehicles call retrieves a list of vehicles on your Tesla account.  It extracts the id_s variable for the first vehicle and stores it in the teslaVehicleIdS environment variable.  Without this value, other API calls will fail.  Once id_s has been retrieved, Get Vehicles should not be needed again.

### Wake Vehicle

The Wake Vehicle call wakes a sleeping vehicle.

### Get Vehicle Data

The Get Vehicle Data call retrieves all available data for the vehicle defined by the teslaVehicleIdS environment variable.

