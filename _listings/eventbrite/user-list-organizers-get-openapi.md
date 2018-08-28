---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 0
info:
  title: Eventbrite Get User List Organizers
  description: This method lists the organizers created by this user. Requires authentication.
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
    post:
      summary: Post Organizers
      description: Updates an organizer and returns it as as organizer.
      operationId: postOrganizers
      x-api-path-slug: organizersid-post
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
  /organizers/{id}/events/:
    get:
      summary: Get Organizers Events
      description: Gets events of the organizer.
      operationId: getOrganizersEvents
      x-api-path-slug: organizersidevents-get
      parameters:
      - in: query
        name: only_public
        description: Only show public events even if viewing your own events
        type: query
      - in: query
        name: order_by
        description: 'How to order the results (Valid choices are: start_asc, start_desc,
          created_asc, or created_desc)'
        type: query
      - in: query
        name: start_date.range_end
        description: Only return events with start dates before the given date
        type: query
      - in: query
        name: start_date.range_start
        description: Only return events with start dates after the given date
        type: query
      - in: query
        name: status
        description: Only return events with a specific status set
        type: query
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - Events
  /users/{id}/organizers/:
    get:
      summary: Get Users Organizers
      description: Returns a paginated response of organizer objects that are owned
        by the user.
      operationId: getUsersOrganizers
      x-api-path-slug: usersidorganizers-get
      parameters:
      - in: query
        name: hide_unsaved
        description: 'True: Will hide organizers flagged as &#8220;unsaved&#8221;False:
          Will show organizers regardless of unsaved flag (Default value)'
        type: query
      responses:
        200:
          description: OK
      tags:
      - Users
      - Organizers
  /user_list_organizers:
    get:
      summary: Get User List Organizers
      description: This method lists the organizers created by this user. Requires
        authentication.
      operationId: Get_user_list_organizers_
      x-api-path-slug: user-list-organizers-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      responses:
        200:
          description: OK
      tags:
      - User
      - List
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