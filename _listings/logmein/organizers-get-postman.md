{
  "info": {
    "name": "GoToMeeting Organizer by email",
    "_postman_id": "c6ea7955-1352-455c-b1fc-390b9c17dab8",
    "description": "Gets the individual organizer specified by the organizer's email address. If an email address is not specified, all organizers are returned. This API call is only available to users with the admin role.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "71d8f050-6e23-49cb-89c2-eb899b3e930f",
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
              "id": "d8f52791-5e06-4784-bfbe-4580c1c4aac1"
            }
          ]
        }
      ]
    },
    {
      "name": "Organizer",
      "item": [
        {
          "id": "10345779-6850-4710-b055-6f22518764ea",
          "name": "OrganizersByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "organizers/:organizerKey"
              ],
              "variable": [
                {
                  "id": "organizerKey",
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
            "description": "Gets the individual organizer specified by the organizer's email address. If an email address is not specified, all organizers are returned. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a975b7e3-2aa9-4b14-8f49-c874e36cabfb"
            }
          ]
        },
        {
          "id": "c63d506e-d38d-4ba7-a19a-135507c4a86d",
          "name": "OrganizersByOrganizerKeyPut",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "organizers/:organizerKey"
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
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
            "description": "Updates the products of the specified organizer. To add a product (G2M, G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for each product you want to add. To remove all products for the organizer, set status to 'suspended'. The call is limited to users with the admin role.\r\n\t\t\t\t\t\t\t\t\t\t\r\n\t\tfield\t\t\tvalue\t\t\tdescription\t\t\r\n\t\t\"firstName\"\t\t\t\"First\"\t\t\tString - max 25 characters\t\t\r\n\t\t\"lastName\"\t\t\t\"Last\"\t\t\tString - max 25 characters\t\t\r\n\t\t\"organizerEmail\"\t\t\t\"valid.org@email.com\"\t\t\tString with valid email syntax\t\t\r\n\t\t\"productType\"\t\t\t\"G2M\"\t\t\tMust be: G2M, G2W, G2T, OV\t\t\r\n\t\t\"status\"\t\t\t\"suspended\"\t\t\tMust be: blank or suspended"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30246064-7fb3-40fc-8196-2744311bca23"
            }
          ]
        },
        {
          "id": "e8d933b8-dc1f-4211-8c3d-5962c69c9d23",
          "name": "OrganizersByOrganizerKeyDelete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "organizers/:organizerKey"
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
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
            "description": "Deletes the individual organizer specified by the organizer key. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d1a4a754-89b9-4ce4-a6c3-543247078b7b"
            }
          ]
        },
        {
          "id": "9189446a-c3e6-4a69-821a-4e002c933644",
          "name": "OrganizersGet",
          "request": {
            "url": "http://api.getgo.com/G2M/rest/organizers?email=%7B%7D",
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
            "description": "Gets the individual organizer specified by the organizer's email address. If an email address is not specified, all organizers are returned. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2746566b-65cf-481a-8d1a-98bef981bb57"
            }
          ]
        }
      ]
    }
  ]
}