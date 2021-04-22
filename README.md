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
    "user_mail": "batuhanz@game.com.tr",
    "user_profile_card_name": "Batuhan KAHRAMAN",
    "user_profile_gsm_number": "5417720199",
    "user_profile_card_nick": "BatuhanZ",
    "user_profile_card_location": "T&#252;rkiye - Kocaeli",
    "user_profile_card_desc": "Merhabalar... Benim ad&#305;m Batuhan. DigitalAbi olarakta tan&#305;yorsunuz. Oyuncuyum fakat daha &#231;ok yaz&#305;l&#305;m ile ilgiliyim. Oyun oynayaca&#287;&#305;ma bu sitenin kodlama g&#246;revini &#252;stlendim. ",
    "user_profile_gender": 1,
    "user_profile_link": "/playerunknowns-battlegrounds/users/batuhanz-1.html",
    "user_profile_image": "/Old____Assets/User/1.Jpg?Rid=42083",
    "user_profile_cover_image": "/Old____Assets/User/Cover_1.Jpg?Rid=34626",
    "user_approved": true
  }
}
 ```



 **Response:(Non Approved User)**
 Data type is object.
 ```javascript
{
  "api_version": 1.22,
  "method": "auth_user_info",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619059741867,
  "response_date_utc": 1619059741910,
  "response_time_millisecond": 43,
  "data": {
    "user_id": 13227,
    "user_mail": "lider2135@hotmail.com",
    "user_profile_card_name": "",
    "user_profile_gsm_number": "",
    "user_profile_card_nick": "",
    "user_profile_card_location": "",
    "user_profile_card_desc": "",
    "user_profile_gender": 0,
    "user_profile_link": "/pogup/users/user-13227.html",
    "user_profile_image": "/Old____Assets/User/0.Jpg",
    "user_profile_cover_image": "/src/assets/img/profile.png",
    "user_approved": false,
    "user_approve_fields": {
      "user_bio": false,
      "user_tck": false,
      "user_gsm": false,
      "user_mail": true
    }
  }
}
 ```








---






