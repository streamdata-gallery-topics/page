swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Utility APIs
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/front_page:
    get:
      summary: Show front page
      description: Show front page.
      operationId: show-front-page
      x-api-path-slug: coursescourse-idfront-page-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Front
      - Page
    put:
      summary: Update/create front page
      description: Update/create front page.
      operationId: updatecreate-front-page
      x-api-path-slug: coursescourse-idfront-page-put
      parameters:
      - in: query
        name: wiki_page[body]
        description: The content for the new page
      - in: query
        name: wiki_page[editing_roles]
        description: Which user roles are allowed to edit this page
      - in: query
        name: wiki_page[notify_of_update]
        description: Whether participants should be notified when this page changes
      - in: query
        name: wiki_page[published]
        description: Whether the page is published (true) or draft state (false)
      - in: query
        name: wiki_page[title]
        description: The title for the new page
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Front
      - Page
  /groups/{group_id}/front_page:
    get:
      summary: Show front page
      description: Show front page.
      operationId: show-front-page
      x-api-path-slug: groupsgroup-idfront-page-get
      responses:
        200:
          description: OK
      tags:
      - Groups
      - Group
      - Id
      - Front
      - Page
    put:
      summary: Update/create front page
      description: Update/create front page.
      operationId: updatecreate-front-page
      x-api-path-slug: groupsgroup-idfront-page-put
      parameters:
      - in: query
        name: wiki_page[body]
        description: The content for the new page
      - in: query
        name: wiki_page[editing_roles]
        description: Which user roles are allowed to edit this page
      - in: query
        name: wiki_page[notify_of_update]
        description: Whether participants should be notified when this page changes
      - in: query
        name: wiki_page[published]
        description: Whether the page is published (true) or draft state (false)
      - in: query
        name: wiki_page[title]
        description: The title for the new page
      responses:
        200:
          description: OK
      tags:
      - Groups
      - Group
      - Id
      - Front
      - Page
  /users/{user_id}/page_views:
    get:
      summary: List user page views
      description: List user page views.
      operationId: list-user-page-views
      x-api-path-slug: usersuser-idpage-views-get
      parameters:
      - in: query
        name: end_time
        description: The end of the time range from which you want page views
      - in: query
        name: start_time
        description: The beginning of the time range from which you want page views
      responses:
        200:
          description: OK
      tags:
      - Users
      - User
      - Id
      - Page
      - Views