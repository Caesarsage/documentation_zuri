# ZURI CHESS DOCUMENTATION
- GET GENERAL PLUGIN INFORMATION
- GET SIDEBAR INFORMATION


## ZURI CHESS DOCUMENTATION - GET GENERAL PLUGIN INFORMATION

Documentation for Zuri chess plugin on getting general plugin information

###  This Endpoint returns all the information for this plugin about zuri.chess plugin

- Method : GET
- Description: Return all the information for zuri.chess plugin

#### URL LINK
[https://chess.zuri.chat/api/v1/info]

### Required Parameters: 
  None

### Responses
``` sh
Code : 200
Description: Success, return list of plugin information in JSON object format
{
  "message":"Plugin Information Retrieved",
  "data": <Object>,
  "success": true
}

Code : 500
Description: Server Error, Could not fetch plugin information
{
  "message":"",
  "data":null,
  "success": false
}
```

## ZURI CHESS DOCUMENTATION - GET SIDEBAR INFORMATION

Documentation for Zuri chess plugin on getting sidebar information

###  This Endpoint return all sidebar information about zuri.chess plugin for a given user

- Method : GET
- Description: Returns all sidebar information for a given user in the database

#### URL LINK
[https://chess.zuri.chat/api/v1/sidebar]

### Required Parameters: 
  | Name | Data Type | Description
  |------| --------- |------------ |
  | userId | string | reference a particular user
  | org | string | reference plugin organization
  | token | string | reference plugin token

### Responses
``` sh
Code : 200,
Description: Success, return list of sidebar information in JSON object format
{
  "message":"Fetched sidebar data",
  "data": <Object>,
  "success": true
}

Code : 400
Description:Server Error, Data not available
{
  "message":"Data not available",
  "data":{},
  "success": false
}

Code : 500
Description: Internal Server Error occurred
{
  "message":"",
  "data":null,
  "success": false
}