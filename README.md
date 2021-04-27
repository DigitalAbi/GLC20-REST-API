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
    "user_balance": 1960.84,
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
    "user_balance": 400.14,
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
 
---

### Tournaments
Get custom tournament list for tournaments page.

 **Method Name:**
 tournaments

 **Parameters:**
 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES |
 game_id | INTEGER | NO | default value is 0 for all , if filter set game_id
 tournament_status_id | INTEGER | NO | default value is 0 for all , if filter set tournament_status_id
 page_number | INTEGER | NO | default value is 1 , use for paging
 page_offset | INTEGER | NO | default value is 12 , tournament count per page 

 **Response:** Data type is array. ("page_number" parameters is setted 2 on this sample response).
 ```javascript
{
  "api_version": 1.22,
  "method": "tournaments",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619387473017,
  "response_date_utc": 1619387473133,
  "response_time_millisecond": 116,
  "data": {
    "total_count": 20,
    "page_offset": 12,
    "page_number": 2,
    "listing_first": 13,
    "listing_last": 24,
    "tournament_status_id": 0,
    "game_id": 0,
    "tournaments": [
      {
        "tournament_id": 1058,
        "tournament_start_date": 1601910000,
        "tournament_name": "NİLÜFER BELEDİYESİ VALORANT C",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 3,
        "tournament_game_name": "Valorant",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/3/1.Jpg",
        "tournament_href_url": "/Tournament/1058/pogup-valorant-nilufer-belediyesi-valorant-c.html",
        "tournament_game_name_short": "VALORANT"
      },
      {
        "tournament_id": 1055,
        "tournament_start_date": 1601827200,
        "tournament_name": "NİLÜFER BELEDİYESİ VALORANT B",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 3,
        "tournament_game_name": "Valorant",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/3/1.Jpg",
        "tournament_href_url": "/Tournament/1055/pogup-valorant-nilufer-belediyesi-valorant-b.html",
        "tournament_game_name_short": "VALORANT"
      },
      {
        "tournament_id": 1054,
        "tournament_start_date": 1601744400,
        "tournament_name": "NİLÜFER BELEDİYESİ VALORANT A",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 3,
        "tournament_game_name": "Valorant",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/3/1.Jpg",
        "tournament_href_url": "/Tournament/1054/pogup-valorant-nilufer-belediyesi-valorant-a.html",
        "tournament_game_name_short": "VALORANT"
      },
      {
        "tournament_id": 1051,
        "tournament_start_date": 1601823600,
        "tournament_name": "NİLÜFER BELEDİYESİ PUBG B",
        "tournament_size": 64,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 5,
        "tournament_game_name": "Playerunknown's Battlegrounds",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/5/1.Jpg",
        "tournament_href_url": "/Tournament/1051/pogup-playerunknowns-battlegrounds-nilufer-belediyesi-pubg-b.html",
        "tournament_game_name_short": "PUBG"
      },
      {
        "tournament_id": 1047,
        "tournament_start_date": 1601740800,
        "tournament_name": "NİLÜFER BELEDİYESİ PUBG A",
        "tournament_size": 64,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 5,
        "tournament_game_name": "Playerunknown's Battlegrounds",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/5/1.Jpg",
        "tournament_href_url": "/Tournament/1047/pogup-playerunknowns-battlegrounds-nilufer-belediyesi-pubg-a.html",
        "tournament_game_name_short": "PUBG"
      },
      {
        "tournament_id": 1041,
        "tournament_start_date": 1601910000,
        "tournament_name": "NİLÜFER BELEDİYESİ LOL ( C )",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 2,
        "tournament_game_name": "League of Legends",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/2/1.Jpg",
        "tournament_href_url": "/Tournament/1041/pogup-league-of-legends-nilufer-belediyesi-lol-c-.html",
        "tournament_game_name_short": "L.O.L."
      },
      {
        "tournament_id": 1040,
        "tournament_start_date": 1601823600,
        "tournament_name": "NİLÜFER BELEDİYESİ LOL (B )",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 2,
        "tournament_game_name": "League of Legends",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/2/1.Jpg",
        "tournament_href_url": "/Tournament/1040/pogup-league-of-legends-nilufer-belediyesi-lol-b-.html",
        "tournament_game_name_short": "L.O.L."
      },
      {
        "tournament_id": 1039,
        "tournament_start_date": 1601737200,
        "tournament_name": "NİLÜFER BELEDİYESİ LOL (A )",
        "tournament_size": 32,
        "tournament_offline": 0,
        "tournament_earning": 50000,
        "tournament_fee": 0,
        "tournament_status_id": 6,
        "tournament_status_description": "Tamamlandı",
        "tournament_game_id": 2,
        "tournament_game_name": "League of Legends",
        "tournament_cover_image": "/Old____Assets/GameWallPapers/2/1.Jpg",
        "tournament_href_url": "/Tournament/1039/pogup-league-of-legends-nilufer-belediyesi-lol-a-.html",
        "tournament_game_name_short": "L.O.L."
      }
    ]
  }
}
 ```
 
 
 
 
 ---
  

### Banners
Get banners for pages.

 **Method Name:**
 banners

 **Parameters:**
 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES |
 banner_page | STRING | NO | filter banners for current page

 **Response:** Data type is array. 
 ```javascript
{
  "api_version": 1.22,
  "method": "banners",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619558606920,
  "response_date_utc": 1619558606927,
  "response_time_millisecond": 7,
  "data": [
    {
      "banner_id": 2,
      "banner_page": "Home",
      "banner_description": "Banner Açıklaması 2",
      "banner_action_url": "/?Ref=Banner_2",
      "banner_url": "https://www.pogup.com/Assets/Trash/Bayraktar_X_Drive.jpg",
      "banner_order": 1,
      "banner_countdown": 0,
      "banner_countdown_date": 1619541104
    },
    {
      "banner_id": 3,
      "banner_page": "Home",
      "banner_description": "Banner Açıklaması 3",
      "banner_action_url": "#",
      "banner_url": "https://www.pogup.com/Assets/Trash/Brawls_1_Stars.Jpg",
      "banner_order": 2,
      "banner_countdown": 0,
      "banner_countdown_date": 1619541877
    }
  ]
}
 ```
 
 
 
 
 

 
 
 ---
  

### Balance
Get pogin balance for teams or users

 **Method Name:**
 balance

 **Parameters:**
 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES |
 balance_type | INTEGER | YES | set "1" for users, "2" for teams
 balance_id | INTEGER | YES | if balance_type "1" send user_id , if balance_type = "2" send team_id

 **Response:** Data type is array. 
 ```javascript
{
  "api_version": 1.22,
  "method": "balance",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619548327437,
  "response_date_utc": 1619548327440,
  "response_time_millisecond": 3,
  "data": {
    "balance": 360.86,
    "balance_id": 1,
    "balance_type": 1
  }
}
 ```
 
 




 ---
  

### Tournament Status List
Get tournament status descriptions.

 **Method Name:**
 tournament_status

 **Parameters:**
 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES | 

 **Response:** Data type is array. 
 ```javascript
{
  "api_version": 1.22,
  "method": "tournament_status",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619559371510,
  "response_date_utc": 1619559371517,
  "response_time_millisecond": 7,
  "data": [
    {
      "tournament_status_id": 1,
      "tournament_status_description": "Başlamadı"
    },
    {
      "tournament_status_id": 2,
      "tournament_status_description": "Katılım Başladı"
    },
    {
      "tournament_status_id": 3,
      "tournament_status_description": "Maçlar Başladı"
    },
    {
      "tournament_status_id": 4,
      "tournament_status_description": "Yarı Final"
    },
    {
      "tournament_status_id": 5,
      "tournament_status_description": "Final"
    },
    {
      "tournament_status_id": 6,
      "tournament_status_description": "Tamamlandı"
    }
  ]
}
 ```
 
 
 






 ---
  

### Game List
Get game list

 **Method Name:**
 game_list

 **Parameters:**
 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 method | STRING | YES | 

 **Response:** Data type is array. 
 ```javascript
{
  "api_version": 1.22,
  "method": "game_list",
  "error": 0,
  "error_desc": "no_error",
  "request_date_utc": 1619559538847,
  "response_date_utc": 1619559538890,
  "response_time_millisecond": 43,
  "data": [
    {
      "game_id": 1,
      "game_name": "Counter-Strike:Global Offensive",
      "game_name_short": "CS:GO",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 1,
      "game_order_number": 20
    },
    {
      "game_id": 2,
      "game_name": "League of Legends",
      "game_name_short": "L.O.L.",
      "game_platform_id": 2,
      "game_platform_name": "Riot Games",
      "game_tournament_enable": 1,
      "game_order_number": 10
    },
    {
      "game_id": 3,
      "game_name": "Valorant",
      "game_name_short": "VALORANT",
      "game_platform_id": 2,
      "game_platform_name": "Riot Games",
      "game_tournament_enable": 1,
      "game_order_number": 30
    },
    {
      "game_id": 4,
      "game_name": "Zula",
      "game_name_short": "ZULA",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 0,
      "game_order_number": 40
    },
    {
      "game_id": 5,
      "game_name": "Playerunknown's Battlegrounds",
      "game_name_short": "PUBG",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 1,
      "game_order_number": 11
    },
    {
      "game_id": 6,
      "game_name": "Fifa 2020",
      "game_name_short": "FIFA2000",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 0,
      "game_order_number": 1000
    },
    {
      "game_id": 7,
      "game_name": "Rocket League",
      "game_name_short": "ROCKET LEAGUE",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 0,
      "game_order_number": 1001
    },
    {
      "game_id": 8,
      "game_name": "Fortnite",
      "game_name_short": "FORTNITE",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 1,
      "game_order_number": 1002
    },
    {
      "game_id": 9,
      "game_name": "Rainbow Six Siege",
      "game_name_short": "R6 SIEGE",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 0,
      "game_order_number": 1003
    },
    {
      "game_id": 10,
      "game_name": "Brawl Stars",
      "game_name_short": "BRAWL STARS",
      "game_platform_id": 1,
      "game_platform_name": "Steam",
      "game_tournament_enable": 0,
      "game_order_number": 1004
    },
    {
      "game_id": 11,
      "game_name": "PUBG - Mobile",
      "game_name_short": "PUBG - MOBILE",
      "game_platform_id": 10,
      "game_platform_name": "not set",
      "game_tournament_enable": 0,
      "game_order_number": 1005
    }
  ]
}
 ```
 
 







