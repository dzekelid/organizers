---
swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 0
info:
  title: GoToMeeting Organizer by email
  description: Deletes the individual organizer specified by the email address. This
    API call is only available to users with the admin role.
  version: 1.0.0
host: api.getgo.com
basePath: /G2M/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{groupkey}/organizers:
    get:
      summary: Organizers by group
      description: Returns all the organizers within a specific group. This API call
        is only available to users with the admin role.
      operationId: GroupsOrganizersByGroupkeyGet
      x-api-path-slug: groupsgroupkeyorganizers-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: groupkey
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - By
      - Group
  /organizers/{organizerKey}:
    get:
      summary: Organizer
      description: Gets the individual organizer specified by the organizer's email
        address. If an email address is not specified, all organizers are returned.
        This API call is only available to users with the admin role.
      operationId: OrganizersByOrganizerKeyGet
      x-api-path-slug: organizersorganizerkey-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      responses:
        200:
          description: OK
      tags:
      - Organizer
    put:
      summary: Organizer
      description: "Updates the products of the specified organizer. To add a product
        (G2M, G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for
        each product you want to add. To remove all products for the organizer, set
        status to 'suspended'. The call is limited to users with the admin role.\r\n\t\t\t\t\t\t\t\t\t\t\r\n\t\tfield\t\t\tvalue\t\t\tdescription\t\t\r\n\t\t\"firstName\"\t\t\t\"First\"\t\t\tString
        - max 25 characters\t\t\r\n\t\t\"lastName\"\t\t\t\"Last\"\t\t\tString - max
        25 characters\t\t\r\n\t\t\"organizerEmail\"\t\t\t\"valid.org@email.com\"\t\t\tString
        with valid email syntax\t\t\r\n\t\t\"productType\"\t\t\t\"G2M\"\t\t\tMust
        be: G2M, G2W, G2T, OV\t\t\r\n\t\t\"status\"\t\t\t\"suspended\"\t\t\tMust be:
        blank or suspended"
      operationId: OrganizersByOrganizerKeyPut
      x-api-path-slug: organizersorganizerkey-put
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      responses:
        200:
          description: OK
      tags:
      - Organizer
    delete:
      summary: Organizer
      description: Deletes the individual organizer specified by the organizer key.
        This API call is only available to users with the admin role.
      operationId: OrganizersByOrganizerKeyDelete
      x-api-path-slug: organizersorganizerkey-delete
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      responses:
        200:
          description: OK
      tags:
      - Organizer
  /organizers:
    get:
      summary: Organizer by email
      description: Gets the individual organizer specified by the organizer's email
        address. If an email address is not specified, all organizers are returned.
        This API call is only available to users with the admin role.
      operationId: OrganizersGet
      x-api-path-slug: organizers-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: email
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - By
      - Email
    post:
      summary: Organizer
      description: "Creates a new organizer and sends an email to the email address
        defined in the request. This API call is only available to users with the
        admin role. You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType,
        to create organizers for those products. A G2W or G2T organizer will also
        have access to G2M.\r\n\r\n\t\t\t\t\t\t\t\t\t\t\r\n\t\tfield\t\t\tvalue\t\t\tdescription\t\t\r\n\t\t\"firstName\"\t\t\t\"First\"\t\t\tString
        - max 25 characters\t\t\r\n\t\t\"lastName\"\t\t\t\"Last\"\t\t\tString - max
        25 characters\t\t\r\n\t\t\"organizerEmail\"\t\t\t\"valid.org@email.com\"\t\t\tString
        with valid email syntax\t\t\r\n\t\t\"productType\"\t\t\t\"G2M\"\t\t\tMust
        be: G2M, G2W, G2T, OV"
      operationId: OrganizersPost
      x-api-path-slug: organizers-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Organizer
    delete:
      summary: Organizer by email
      description: Deletes the individual organizer specified by the email address.
        This API call is only available to users with the admin role.
      operationId: OrganizersDelete
      x-api-path-slug: organizers-delete
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: email
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - By
      - Email
  /organizers/{organizerKey}/attendees:
    get:
      summary: Attendees by organizer
      description: Lists all attendees for all meetings within a specified date range
        for a specified organizer. This API call is only available to users with the
        admin role.
      operationId: OrganizersAttendeesByOrganizerKeyGet
      x-api-path-slug: organizersorganizerkeyattendees-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: endDate
      - in: path
        name: organizerKey
      - in: query
        name: starttime
      responses:
        200:
          description: OK
      tags:
      - Attendees
      - By
      - Organizer
  /groups/{groupKey}/organizers:
    post:
      summary: Organizer in group
      description: "Creates a new organizer and sends an email to the email address
        defined in request. This API call is only available to users with the admin
        role. You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType variables,
        creating organizers for those products. A G2W or G2T organizer will also have
        access to G2M.\r\n\t\t\t\t\t\t\t\t\t\t\r\n\t\tfield\t\t\tvalue\t\t\tdescription\t\t\r\n\t\t\"organizerEmail\"\t\t\t\"valid.org@email.com\"\t\t\tString
        with valid email syntax\t\t\r\n\t\t\"firstName\"\t\t\t\"First\"\t\t\tString
        - max 25 characters\t\t\r\n\t\t\"lastName\"\t\t\t\"Last\"\t\t\tString - max
        25 characters\t\t\r\n\t\t\"productType\"\t\t\t\"G2M\"\t\t\tMust be: G2M, G2W,
        G2T, OV"
      operationId: GroupsOrganizersByGroupKeyPost
      x-api-path-slug: groupsgroupkeyorganizers-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: groupKey
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - In
      - Group
  /organizers/{organizerKey}/historicalMeetings:
    get:
      summary: Historical meetings by organizer
      description: Get historical meetings for the specified organizer that started
        within the specified date/time range. Meetings which are still ongoing at
        the time of the request are not included in the result.
      operationId: OrganizersHistoricalMeetingsByOrganizerKeyGet
      x-api-path-slug: organizersorganizerkeyhistoricalmeetings-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: endDate
      - in: path
        name: organizerKey
      - in: query
        name: startDate
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Meetings
      - By
      - Organizer
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