---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 0
info:
  title: Eventbrite Get Organizers
  description: Gets an organizer by ID as organizer.
  version: 1.0.0
host: www.eventbrite.com
basePath: /%7Bdata-type%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizers/:
    post:
      summary: Post Organizers
      description: Makes a new organizer. Returns an organizer as organizer.
      operationId: postOrganizers
      x-api-path-slug: organizers-post
      parameters:
      - in: query
        name: organizer.description.html
        description: The description of the organizer
        type: query
      - in: query
        name: organizer.facebook
        description: The Facebook URL ID for the organizer
        type: query
      - in: query
        name: organizer.instagram
        description: The Instagram numeric ID for the organizer
        type: query
      - in: query
        name: organizer.logo.id
        description: The logo id of the organizer
        type: query
      - in: query
        name: organizer.long_description.html
        description: The long description of the organizer
        type: query
      - in: query
        name: organizer.name
        description: The name of the organizer
        type: query
      - in: query
        name: organizer.twitter
        description: The Twitter handle for the organizer
        type: query
      - in: query
        name: organizer.website
        description: The website for the organizer
        type: query
      responses:
        200:
          description: OK
      tags:
      - Organizers
  /organizers/{id}/:
    get:
      summary: Get Organizers
      description: Gets an organizer by ID as organizer.
      operationId: getOrganizers
      x-api-path-slug: organizersid-get
      responses:
        200:
          description: OK
      tags:
      - Organizers
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---