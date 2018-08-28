---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Meeting Delete organizer by email
  description: Deletes the individual organizer specified by the email address. This
    API call is only available to users with the admin role.
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2M/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{groupKey}/organizers:
    get:
      summary: Get organizers by group
      description: Returns all the organizers within a specific group. This API call
        is only available to users with the admin role.
      operationId: returns-all-the-organizers-within-a-specific-group--this-api-call-is-only-available-to-users-with-th
      x-api-path-slug: groupsgroupkeyorganizers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - Organizers
    post:
      summary: Create organizer in group
      description: Creates a new organizer and sends an email to the email address
        defined in request. This API call is only available to users with the admin
        role. You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType variables,
        creating organizers for those products. A G2W or G2T organizer will also have
        access to G2M.
      operationId: creates-a-new-organizer-and-sends-an-email-to-the-email-address-defined-in-request--this-api-call-is
      x-api-path-slug: groupsgroupkeyorganizers-post
      parameters:
      - in: body
        name: body
        description: The details of the organizer to be created
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - Organizers
  /organizers:
    delete:
      summary: Delete organizer by email
      description: Deletes the individual organizer specified by the email address.
        This API call is only available to users with the admin role.
      operationId: deletes-the-individual-organizer-specified-by-the-email-address--this-api-call-is-only-available-to-
      x-api-path-slug: organizers-delete
      parameters:
      - in: query
        name: email
        description: The email address of the organizer
      - in: query
        name: No Name
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