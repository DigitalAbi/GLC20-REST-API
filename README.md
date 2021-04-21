# Pogup Rapi

## Description

** Response Standarts :**
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
   "request_date_utc": 1619048513923,
   "response_date_utc": 1619048513940,
   "response_time_millisecond": 17,
   "data": [
     {
       "user_auth_key": "018d2cd3bc457d7f74c65fc7b72b082dab371a08bfad877b083728ba83294157e9678828cec8197dda4d37b9ba0dbaea3d3460719eeaf0a9",
       "user_auth_key_expire": 1621640190977
     }
   ]
 }
 ```

---
