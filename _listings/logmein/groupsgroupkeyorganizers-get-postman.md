{
  "info": {
    "name": "GoToMeeting Organizers by group",
    "_postman_id": "d7c7e4cf-f949-4e09-a7e7-e7c3b2532d08",
    "description": "Returns all the organizers within a specific group. This API call is only available to users with the admin role.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "d046977a-bb9a-43ea-907a-529e09850dd3",
          "name": "GroupsOrganizersByGroupkeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "groups/:groupkey/organizers"
              ],
              "variable": [
                {
                  "id": "groupkey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the organizers within a specific group. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "658c5b06-45ca-44e5-b424-395c8fa43339"
            }
          ]
        }
      ]
    }
  ]
}