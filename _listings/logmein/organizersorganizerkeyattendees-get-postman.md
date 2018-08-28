{
  "info": {
    "name": "GoToMeeting Attendees by organizer",
    "_postman_id": "de874af7-90f6-49c5-8f1d-4346687ed5cf",
    "description": "Lists all attendees for all meetings within a specified date range for a specified organizer. This API call is only available to users with the admin role.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Attendees",
      "item": [
        {
          "id": "221b72b6-9aa8-4e91-97c3-5deca99a9f31",
          "name": "MeetingsAttendeesByMeetingInstanceKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "meetings/:meetingInstanceKey/attendees"
              ],
              "variable": [
                {
                  "id": "meetingInstanceKey",
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
            "description": "List all attendees for specified meetingId of historical meeting. The historical meetings can be fetched using 'Get historical meetings', 'Get historical meetings by organizer', and 'Get historical meetings by group'. For users with the admin role this call returns attendees for any meeting. For any other user the call will return attendees for meetings on which the user is a valid organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bdd84877-8a20-45fa-bb3a-539e26042cd5"
            }
          ]
        },
        {
          "id": "324ef94b-c798-4334-ba92-faebcdcd8610",
          "name": "OrganizersAttendeesByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "organizers/:organizerKey/attendees"
              ],
              "query": [
                {
                  "key": "endDate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "starttime",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "Lists all attendees for all meetings within a specified date range for a specified organizer. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4ceb4414-69bc-42b0-a266-c64181379467"
            }
          ]
        }
      ]
    }
  ]
}