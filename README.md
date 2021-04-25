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


### User Public Information
Get any user information with user_id.

 **Method Name:**
 public_user_info

 **Parameters:**

 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES |
 user_id| INTEGER | YES | 
 equipments | INTEGER | NO | default value is 0, if enable set 1 , response is array
 achievements | INTEGER | NO | default value is 0, if enable set 1 , response is array
 duels | INTEGER | NO | default value is 0, if enable set 1 , response is array
 tournaments | INTEGER | NO | default value is 0, if enable set 1 , response is array
 teams | INTEGER | NO | default value is 0, if enable set 1 , response is array
 matchs | INTEGER | NO | default value is 0, if enable set 1 , response is array

 **Response:**
 Data type is object ("teams" and "tournaments" parameters is setted 1 on this sample response).
 ```javascript
{
  "api_version": 1.22,
  "method": "public_user_info",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619382898137,
  "response_date_utc": 1619382898260,
  "response_time_millisecond": 123,
  "data": {
    "user_id": 1,
    "user_profile_card_name": "Batuhan KAHRAMAN",
    "user_profile_card_nick": "BatuhanZ",
    "user_profile_card_location": "T&#252;rkiye - Kocaeli",
    "user_profile_card_desc": "Merhabalar... Benim ad&#305;m Batuhan. DigitalAbi olarakta tan&#305;yorsunuz. Oyuncuyum fakat daha &#231;ok yaz&#305;l&#305;m ile ilgiliyim. Oyun oynayaca&#287;&#305;ma bu sitenin kodlama g&#246;revini &#252;stlendim. ",
    "user_profile_gender": 1,
    "user_profile_link": "/playerunknowns-battlegrounds/users/batuhanz-1.html",
    "user_profile_image": "/Old____Assets/User/1.Jpg?Rid=28072",
    "user_profile_cover_image": "/Old____Assets/User/Cover_1.Jpg?Rid=20614",
    "user_approved": true,
    "equipments": [],
    "achievements": [],
    "duels": [],
    "tournaments": [
      {
        "tournament_id": 2083,
        "tournament_start_date": 1618245000,
        "tournament_name": "Deneme Yeni Versiyon",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 3,
        "tournament_status_description": "Maçlar Başladı",
        "tournament_game_id": 2,
        "tournament_game_name": "League of Legends",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/2/1.Jpg",
        "tournament_href_url": "/Tournament/2083/pogup-league-of-legends-deneme-yeni-versiyon.html",
        "tournament_game_name_short": "L.O.L."
      },
      {
        "tournament_id": 1048,
        "tournament_start_date": 1606158000,
        "tournament_name": "TEST CS",
        "tournament_size": 16,
        "tournament_offline": 0,
        "tournament_earning": 0,
        "tournament_fee": 100000,
        "tournament_status_id": 3,
        "tournament_status_description": "Maçlar Başladı",
        "tournament_game_id": 1,
        "tournament_game_name": "Counter-Strike:Global Offensive",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/1/1.Jpg",
        "tournament_href_url": "/Tournament/1048/pogup-counter-strike-global-offensive-test-cs.html",
        "tournament_game_name_short": "CS:GO"
      },
      {
        "tournament_id": 1046,
        "tournament_start_date": 1599955200,
        "tournament_name": "TEST 8",
        "tournament_size": 2,
        "tournament_offline": 0,
        "tournament_earning": 0,
        "tournament_fee": 100000,
        "tournament_status_id": 3,
        "tournament_status_description": "Maçlar Başladı",
        "tournament_game_id": 2,
        "tournament_game_name": "League of Legends",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/2/1.Jpg",
        "tournament_href_url": "/Tournament/1046/pogup-league-of-legends-test-8.html",
        "tournament_game_name_short": "L.O.L."
      }
    ],
    "teams": [
      {
        "team_owner": 1,
        "team_id": 6170,
        "team_owner_user_id": 1,
        "team_name": "Logitech Team",
        "team_country": "TR",
        "team_city": "Ankara",
        "team_description": "",
        "team_social_discord_url": "",
        "team_social_telegram_url": "",
        "team_social_instagram_url": "",
        "team_social_youtube_url": "",
        "team_social_facebook_url": "",
        "team_social_twitch_url": "",
        "team_social_twitter_url": "",
        "team_social_web_url": "",
        "team_create_date_utc": 1618380668
      },
      {
        "team_owner": 1,
        "team_id": 5158,
        "team_owner_user_id": 1,
        "team_name": "DigitaLOL",
        "team_country": "TR",
        "team_city": "Kocaeli",
        "team_description": "",
        "team_social_discord_url": "",
        "team_social_telegram_url": "",
        "team_social_instagram_url": "",
        "team_social_youtube_url": "",
        "team_social_facebook_url": "",
        "team_social_twitch_url": "",
        "team_social_twitter_url": "",
        "team_social_web_url": "",
        "team_create_date_utc": 1616239163
      },
      {
        "team_owner": 1,
        "team_id": 4659,
        "team_owner_user_id": 1,
        "team_name": "CS AXsss111",
        "team_country": "TR",
        "team_city": "Ankara",
        "team_description": "asdas",
        "team_social_discord_url": "7",
        "team_social_telegram_url": "8",
        "team_social_instagram_url": "6",
        "team_social_youtube_url": "5",
        "team_social_facebook_url": "4",
        "team_social_twitch_url": "3",
        "team_social_twitter_url": "2",
        "team_social_web_url": "1",
        "team_create_date_utc": 1605759553
      },
      {
        "team_owner": 1,
        "team_id": 2168,
        "team_owner_user_id": 1,
        "team_name": "Kemer Tokas&#305;",
        "team_country": "TR",
        "team_city": "Kocaeli",
        "team_description": "asdasd",
        "team_social_discord_url": "www.google.com7",
        "team_social_telegram_url": "www.google.com8",
        "team_social_instagram_url": "www.google.com6",
        "team_social_youtube_url": "www.google.com5",
        "team_social_facebook_url": "www.google.com4",
        "team_social_twitch_url": "www.google.com3",
        "team_social_twitter_url": "www.google.com2",
        "team_social_web_url": "www.google.com1",
        "team_create_date_utc": 1600490226
      }
    ],
    "matchs": []
  }
}
 ```
 


