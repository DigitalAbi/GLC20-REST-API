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
   "api": 1.xx,
   "code": 200,
   "action":"tokeninfo"
   "description": "Token Information",
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
 
 
 
 ### User Information
Get basic token information from our developer network.

 **Action Name:**
 userinfo
 
  **Parameters:**

 Name | Type | Mandatory | Description
 ------------ | ------------ | ------------ | ------------
 action | STRING | YES |
 key | STRING | YES | User UID
 pkey | STRING | YES | Platform Id
 
**Request Url:**
https://api.glc20dev.com/?action=userinfo&key=DF2EFA01-C933-4D51-AF65-9D6FE57F4ERT&pkey=A9D2C619-19E5-4179-A6B5-BF3E1D881E2A

**Request Method:**
GET

**Response Data:**
JSON
 

```javascript
{
   "api":1.12,
   "code":200,
   "action":"userinfo",
   "description":"Public User Information",
   "data":{
      "AuthId":5,
      "AuthPlatformId":1,
      "AuthKey":"DF2EFA01-C933-4D51-AF65-9D6FE57F4ERT",
      "AuthKeyResponse":"12F9309C-AC85-4B5F-B87F-C88C18DB4607",
      "Deposit_Wallets":[
         {
            "Wallet_Id":5029,
            "Wallet_Symbol":"USDT.TRC20",
            "Wallet_Provider_Id":1,
            "Wallet_Address":"TEe2KQZYBpsgdkFvCcJTN5uTDVUvLsvwUZ",
            "Wallet_Tag_1":"",
            "Wallet_Tag_2":""
         },
         {
            "Wallet_Id":5053,
            "Wallet_Symbol":"LTCT",
            "Wallet_Provider_Id":1,
            "Wallet_Address":"mypxqrReyCgdnUPqFps21TA24t1hPZmKW6",
            "Wallet_Tag_1":"",
            "Wallet_Tag_2":""
         }
      ]
   }
}
 ```
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

