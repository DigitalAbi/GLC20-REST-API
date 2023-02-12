# GLC Token Rest Api Documentation
* GLC DEVELOPER TEAM *
*12/12/2022*

## Actions 

### Token Information
Get basic token information from our developer network.

 **Action Name:**
 tokeninfo
 
  **Parameters:**

 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 action | STRING | YES |
 symbolid | INTEGER | NO |
 

 **Request Url:**
https://api.glc20dev.com/?action=tokeninfo

**Request Method:**
GET

**Response Data:**
JSON

```javascript
 {
   "api": 1.22,
   "code": 200,
   "action":"tokeninfo"
   "description": "Token Information",
   "response_time_millisecond": 17,
   "data": {
      "symbolid": 1, 
      "symbol": "GLC", 
      "name": "Gameligo Token", 
      "totalsupply": 27500000, 
      "liveprice": 0, 
      "network": "bsc20", 
      "contract": "0x1253fedb6f9e00d0b6ae88b66786aa9ab91d49a0", 
      "decimal": 8, 
      "url": "https://bscscan.com/token/0x1253fedb6f9e00d0b6ae88b66786aa9ab91d49a0",
      "exchanges":[]
   }
 }
 ```

## Methods

### User Auth
Get user authentication key for user processes.

 **Method Name:**
 auth

 **Parameters:**

 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES |
 usermail | STRING | YES |
 password | STRING | YES | 

 **Response:**
 Data type is object.
 ```javascript
 {
   "api_version": 1.22,
   "method": "auth",
   "error": 0,
   "error_desc": "no_error",
   "request_date_utc": 1619058462167,
   "response_date_utc": 1619058462190,
   "response_time_millisecond": 23,
   "data": {
     "user_auth_key": "018d2cd3bc457d7f2e2f742b86834f5faf395e0204289f77ae416f6bbcc59218e23f494e8fb9bd368120574b17fd05e26d24dcd9139241b7",
     "user_auth_key_expire": 1621640190977,
     "user_id": 1
   }
 }
 ```

---








### Auth User Private Information
Get current user information with "user_auth_key" .

 **Method Name:**
 auth_user_info

 **Parameters:**

 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES |
 user_auth_key | STRING | YES | 

 **Response:(Approved User)**
 Data type is object.
 ```javascript
 {
  "api_version": 1.22,
  "method": "auth_user_info",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619059533867,
  "response_date_utc": 1619059533927,
  "response_time_millisecond": 60,
  "data": {
    "user_id": 1,
    "user_balance": 1960.84,
    "user_mail": "usermail@mailprovider.com",
    "user_profile_card_name": "Full Name",
    "user_profile_gsm_number": "5417720199",
    "user_profile_card_nick": "Nick Name",
    "user_profile_card_location": "TR",
    "user_profile_gender": 1,
    "user_approved": true
  }
}
 ```

