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
  | token | integer | reference plugin token

### Responses
``` sh
Code : 200
Description: Success, return list of sidebar information in JSON object format
{
  "message":"Fetched sidebar data",
  "data": {
    name,
    description,
    plugin_id,
    organisation_id,
    user_id,
    group_name,
    show_group,
    joined_rooms,
    public_rooms: [
      {
        title,
        url,
        icon_url,
        action,
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