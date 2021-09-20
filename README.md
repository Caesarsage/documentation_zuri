# ZURI CHESS DOCUMENTATION - GET SIDEBAR INFORMATION

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
Code : 200
Description: Success, return list of sidebar information in JSON object format
{
  "message":"Fetched sidebar data",
  "data": {
    name : string,
    description : string,
    plugin_id : string,
    organisation_id : string,
    user_id : string,
    group_name : string,
    show_group : boolean,
    joined_rooms: object,
    public_rooms: [
      {
        title: string,
        url: string,
        icon_url: string,
        action: string,
      },
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
Description: Internal Server Error occured
{
  "message":"",
  "data":null,
  "success": false
}