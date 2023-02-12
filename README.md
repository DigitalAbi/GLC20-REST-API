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

