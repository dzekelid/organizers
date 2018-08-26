---
name: LogMeIn
x-slug: logmein
description: LogMeIn, Inc. is a provider of software as a service and cloud-based
  remote connectivity services for collaboration, IT management and customer engagement,
  founded in 2003 and based in Boston, Massachusetts.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
x-kinRank: "7"
x-alexaRank: "7271"
tags: Organizers
created: "2018-08-26"
modified: "2018-08-26"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/apis.md
specificationVersion: "0.14"
apis:
- name: GoToMeeting - Organizers by group
  x-api-slug: groupsgroupkeyorganizers-get
  description: Returns all the organizers within a specific group. This API call is
    only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/groupsgroupkeyorganizers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/groupsgroupkeyorganizers-get-openapi.md
- name: GoToMeeting - Organizer
  x-api-slug: organizersorganizerkey-get
  description: Gets the individual organizer specified by the organizer's email address.
    If an email address is not specified, all organizers are returned. This API call
    is only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkey-get-openapi.md
- name: GoToMeeting - Organizer
  x-api-slug: organizersorganizerkey-put
  description: "Updates the products of the specified organizer. To add a product
    (G2M, G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for each
    product you want to add. To remove all products for the organizer, set status
    to 'suspended'. The call is limited to users with the admin role.\r\n\t\t\t\t\t\t\t\t\t\t\r\n\t\tfield\t\t\tvalue\t\t\tdescription\t\t\r\n\t\t\"firstName\"\t\t\t\"First\"\t\t\tString
    - max 25 characters\t\t\r\n\t\t\"lastName\"\t\t\t\"Last\"\t\t\tString - max 25
    characters\t\t\r\n\t\t\"organizerEmail\"\t\t\t\"valid.org@email.com\"\t\t\tString
    with valid email syntax\t\t\r\n\t\t\"productType\"\t\t\t\"G2M\"\t\t\tMust be:
    G2M, G2W, G2T, OV\t\t\r\n\t\t\"status\"\t\t\t\"suspended\"\t\t\tMust be: blank
    or suspended"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkey-put-openapi.md
- name: GoToMeeting - Organizer
  x-api-slug: organizersorganizerkey-delete
  description: Deletes the individual organizer specified by the organizer key. This
    API call is only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkey-delete-openapi.md
- name: GoToMeeting - Organizer by email
  x-api-slug: organizers-get
  description: Gets the individual organizer specified by the organizer's email address.
    If an email address is not specified, all organizers are returned. This API call
    is only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizers-get-openapi.md
- name: GoToMeeting - Attendees by organizer
  x-api-slug: organizersorganizerkeyattendees-get
  description: Lists all attendees for all meetings within a specified date range
    for a specified organizer. This API call is only available to users with the admin
    role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyattendees-get-openapi.md
- name: GoToMeeting - Historical meetings by organizer
  x-api-slug: organizersorganizerkeyhistoricalmeetings-get
  description: Get historical meetings for the specified organizer that started within
    the specified date/time range. Meetings which are still ongoing at the time of
    the request are not included in the result.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyhistoricalmeetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyhistoricalmeetings-get-openapi.md
- name: GoToMeeting - Attendees by organizer
  x-api-slug: organizersorganizerkeyattendees-get
  description: Lists all attendees for all meetings within a specified date range
    for a specified organizer. This API call is only available to users with the admin
    role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyattendees-get-openapi.md
- name: GoToMeeting - Historical meetings by organizer
  x-api-slug: organizersorganizerkeyhistoricalmeetings-get
  description: Get historical meetings for the specified organizer that started within
    the specified date/time range. Meetings which are still ongoing at the time of
    the request are not included in the result.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2M/rest
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyhistoricalmeetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizersorganizerkeyhistoricalmeetings-get-openapi.md
- name: GoToWebinar API - Get organizer sessions
  x-api-slug: organizerkeysessions-get
  description: Get organizer sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizerkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizerkeysessions-get-openapi.md
- name: GoToWebinar API - Get organizer sessions
  x-api-slug: organizerkeysessions-get
  description: Get organizer sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28873-www-logmeininc-com.jpg
  humanURL: http://www.LogMeInInc.com
  baseURL: https://api.getgo.com//G2W/rest/organizers
  tags: SaaS, Technology, Enterprise, Voice, Videoconferencing, Audio, Webinars, Relative
    Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizerkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/organizers/master/_listings/logmein/organizerkeysessions-get-openapi.md
x-common:
- type: x-github
  url: https://github.com/logmein
- type: x-openapi
  url: https://www.getpostman.com/collections/94ad52bdc3d954bad52a
- type: x-postman-collection
  url: https://www.getpostman.com/collections/00bf4391e993c3afa7b7
- type: x-postman-collection
  url: https://www.getpostman.com/collections/c35d614484f21e581775
- type: x-postman-collection
  url: https://www.getpostman.com/collections/9c6e067461f45f7faa6b
- type: x-postman-collection
  url: https://drive.google.com/open?id=16WZlBkS1i8cWSfZ3mMKOwlNP-qsE7AWy
- type: x-postman-collection
  url: https://drive.google.com/file/d/1vI11FNCKpv6WJ_70hoqPNMmPAkASiOU_/view?usp=sharing
- type: x-website
  url: http://www.LogMeInInc.com
- type: x-api-gallery
  url: http://loginradius.api.gallery.streamdata.io
- type: x-api-stack
  url: http://logmein.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/logmein
- type: x-developer
  url: https://goto-developer.logmeininc.com/
- type: x-documentation
  url: https://goto-developer.logmeininc.com/apis/apis-overview
- type: x-faq
  url: https://goto-developer.logmeininc.com/faq-page
- type: x-support
  url: https://goto-developer.logmeininc.com/api-support-request-template
- type: x-twitter
  url: https://twitter.com/LogMeIn
- type: x-website
  url: https://www.logmeininc.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---