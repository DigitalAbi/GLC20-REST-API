# Pogup Rapi
*Batuhan KAHRAMAN*
*22/04/2021*

**RESPONSE STANDARTS:**
```javascript
 {
   "api_version": 1.22,
   "method": "method_name",
   "error": 0,
   "error_desc": "no_error",
   "request_date_utc": 1619048513923,
   "response_date_utc": 1619048513940,
   "response_time_millisecond": 17,
   "data": [
     YOUR RESULT IN HERE
   ]
 }
 ```
The "data" field returns as an array or an object. 
```javascript
   "data": [array]
 ```
```javascript
   "data": {object}
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
