{
  "info": {
    "name": "GoToMeeting Organizer",
    "_postman_id": "295bdca7-ed82-425a-b258-81d23c8b3442",
    "description": "Deletes the individual organizer specified by the organizer key. This API call is only available to users with the admin role.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizers",
      "item": [
        {
          "id": "a219fcd1-1b89-4495-8772-bba5c22f61cb",
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
              "id": "24d7b401-185d-4ea4-9e71-520f8737c491"
            }
          ]
        }
      ]
    },
    {
      "name": "Organizer",
      "item": [
        {
          "id": "47c8e60b-99bf-4d97-8967-e7330190801e",
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
              "id": "0ff12af7-9a67-4fa4-9637-25cd30f97056"
            }
          ]
        },
        {
          "id": "ec374ba4-57af-4f4a-b2f8-2fc35daf33be",
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
              "id": "e87fa550-12e6-4f37-86b4-cef7b15d1b5f"
            }
          ]
        },
        {
          "id": "8a9ade6c-2348-4ace-9f25-bace25a0bea2",
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
              "id": "9452bfc0-b57e-44da-9b6c-bc9a03cffeb2"
            }
          ]
        }
      ]
    }
  ]
}