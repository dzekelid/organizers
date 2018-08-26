{
  "info": {
    "name": "GoToMeeting Historical meetings by organizer",
    "_postman_id": "d069060e-aad0-49c9-97de-218f1ca51092",
    "description": "Get historical meetings for the specified organizer that started within the specified date/time range. Meetings which are still ongoing at the time of the request are not included in the result.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Historical",
      "item": [
        {
          "id": "a846b5e7-f5fa-4135-a60f-d00c507e0319",
          "name": "HistoricalMeetingsGet",
          "request": {
            "url": "http://api.getgo.com/G2M/rest/historicalMeetings?endDate=%7B%7D&startDate=%7B%7D",
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
            "description": "Get historical meetings for the currently authenticated organizer that started within the specified date/time range. Remark: Meetings which are still ongoing at the time of the request are NOT contained in the result array."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "569efacf-75c2-4174-90ab-938022b73dc3"
            }
          ]
        },
        {
          "id": "0927cf3b-401a-4dce-8101-792c8d079fbb",
          "name": "OrganizersHistoricalMeetingsByOrganizerKeyGet",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.getgo.com",
              "path": [
                "G2M",
                "rest",
                "organizers/:organizerKey/historicalMeetings"
              ],
              "query": [
                {
                  "key": "endDate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startDate",
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
            "description": "Get historical meetings for the specified organizer that started within the specified date/time range. Meetings which are still ongoing at the time of the request are not included in the result."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e4c888c-8f7f-4ad7-860f-f00e4886f552"
            }
          ]
        }
      ]
    }
  ]
}