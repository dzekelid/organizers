---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 1
info:
  title: Eventbrite
  description: create-manage--promote-events--add-eventmanagement-features-to-your-site--show-the-world-what-exciting-things-are-happening-around-them-
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
  /organizer_list_events:
    get:
      summary: Get Organizer List Events
      description: This method returns a list of events for a given organizer.
      operationId: Get_organizer_list_events_
      x-api-path-slug: organizer-list-events-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: id
        description: The organizer id
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - List
      - Events
  /organizer_get:
    get:
      summary: Get Organizer Get
      description: This method returns a single organizer by id.
      operationId: Get_organizer_get_
      x-api-path-slug: organizer-get-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: id
        description: The organizer profile id
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - Get
  /organizer_new:
    get:
      summary: Get Organizer New
      description: Many event creators prefer having a specific person identified
        as the point of contact for their event. This person is usually someone like
        the event emcee, or an on-site contact that can help with attendee check-ins
        or other issues during the event. This method creates a new organizer, and
        returns the organizer_id for the newly created resource.
      operationId: Get_organizer_new_
      x-api-path-slug: organizer-new-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: description
        description: The organizer description
      - in: query
        name: name
        description: The organizer name
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - New
  /organizer_update:
    get:
      summary: Get Organizer Update
      description: This method updates an existing organizer. Only the fields passed
        as arguments will be modified. It returns the ID of the updated organizer.
      operationId: Get_organizer_update_
      x-api-path-slug: organizer-update-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      - in: query
        name: description
        description: The organizer description
      - in: query
        name: id
        description: The organizer ID
      - in: query
        name: name
        description: The organizer name
      responses:
        200:
          description: OK
      tags:
      - Organizer
      - Update
---