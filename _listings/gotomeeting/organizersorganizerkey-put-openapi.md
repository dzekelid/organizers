---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Meeting Update organizer
  description: Updates the products of the specified organizer. To add a product (G2M,
    G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for each product
    you want to add. To remove all products for the organizer, set status to 'suspended'.
    The call is limited to users with the admin role.
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
    get:
      summary: Get organizer by email / Get all organizers
      description: Gets the individual organizer specified by the organizer's email
        address. If an email address is not specified, all organizers are returned.
        This API call is only available to users with the admin role.
      operationId: gets-the-individual-organizer-specified-by-the-organizers-email-address--if-an-email-address-is-not-
      x-api-path-slug: organizers-get
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
    post:
      summary: Create organizer
      description: Creates a new organizer and sends an email to the email address
        defined in the request. This API call is only available to users with the
        admin role. You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType
        variables, creating organizers for those products. A G2W or G2T organizer
        will also have access to G2M.
      operationId: creates-a-new-organizer-and-sends-an-email-to-the-email-address-defined-in-the-request--this-api-cal
      x-api-path-slug: organizers-post
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
      - Organizers
  /organizers/{organizerKey}:
    delete:
      summary: Delete organizer
      description: Deletes the individual organizer specified by the organizer key.
        This API call is only available to users with the admin role.
      operationId: deletes-the-individual-organizer-specified-by-the-organizer-key--this-api-call-is-only-available-to-
      x-api-path-slug: organizersorganizerkey-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
    get:
      summary: Get organizer
      description: Returns the individual organizer specified by the key. This API
        call is only available to users with the admin role. Non-admin users can only
        make this call for their own organizerKey.
      operationId: returns-the-individual-organizer-specified-by-the-key--this-api-call-is-only-available-to-users-with
      x-api-path-slug: organizersorganizerkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
    put:
      summary: Update organizer
      description: Updates the products of the specified organizer. To add a product
        (G2M, G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for
        each product you want to add. To remove all products for the organizer, set
        status to 'suspended'. The call is limited to users with the admin role.
      operationId: updates-the-products-of-the-specified-organizer--to-add-a-product-g2m-g2w-g2t-openvoice-for-the-orga
      x-api-path-slug: organizersorganizerkey-put
      parameters:
      - in: body
        name: body
        description: The organizers status
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
  /organizers/{organizerKey}/attendees:
    get:
      summary: Get attendees by organizer
      description: Lists all attendees for all meetings within a specified date range
        for a specified organizer. This API call is only available to users with the
        admin role.
      operationId: lists-all-attendees-for-all-meetings-within-a-specified-date-range-for-a-specified-organizer--this-a
      x-api-path-slug: organizersorganizerkeyattendees-get
      parameters:
      - in: query
        name: endDate
        description: A required end of date range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: A required start of date range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Attendees
  /organizers/{organizerKey}/historicalMeetings:
    get:
      summary: Get historical meetings by organizer
      description: 'Get historical meetings for the specified organizer that started
        within the specified date/time range. Remark: Meetings which are still ongoing
        at the time of the request are NOT contained in the result array.'
      operationId: get-historical-meetings-for-the-specified-organizer-that-started-within-the-specified-datetime-range
      x-api-path-slug: organizersorganizerkeyhistoricalmeetings-get
      parameters:
      - in: query
        name: endDate
        description: Required end of date range, in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: Required start of date range, in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - HistoricalMeetings
  /organizers/{organizerKey}/meetings:
    get:
      summary: 'DEPRECATED: Get meetings by organizer'
      description: 'DEPRECATED: Please use the new API calls ''Get historical meetings
        by organizer'' and ''Get upcoming meetings by organizer''. Gets future (scheduled)
        or past (history) meetings for a specified organizer. Include ''history=true''
        and the past start and end dates in the URL to retrieve past meetings. Enter
        ''scheduled=true'' (without dates) to get scheduled meetings.'
      operationId: deprecated-please-use-the-new-api-calls-get-historical-meetings-by-organizer-and-get-upcoming-meetin
      x-api-path-slug: organizersorganizerkeymeetings-get
      parameters:
      - in: query
        name: endDate
        description: If history is true, required end of date range, in ISO8601 UTC
          format, e
      - in: query
        name: history
        description: When true, returns all past meetings within date range
      - in: query
        name: No Name
      - in: query
        name: scheduled
        description: When true, returns all future meetings
      - in: query
        name: startDate
        description: If history is true, required start of date range, in ISO8601
          UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Meetings
  /organizers/{organizerKey}/upcomingMeetings:
    get:
      summary: Get upcoming meetings by organizer
      description: Get upcoming meetings for a specified organizer. This API call
        is only available to users with the admin role.
      operationId: get-upcoming-meetings-for-a-specified-organizer--this-api-call-is-only-available-to-users-with-the-a
      x-api-path-slug: organizersorganizerkeyupcomingmeetings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - UpcomingMeetings
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