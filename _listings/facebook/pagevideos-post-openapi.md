---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Post Page Veos
  description: Publishes a video to the page
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{page}/videos:
    get:
      summary: Get Page Veos
      description: The videos contained on this page
      operationId: getPageVeos
      x-api-path-slug: pagevideos-get
      parameters:
      - in: path
        name: page
        description: Represents the ID of the page object
      responses:
        200:
          description: OK
      tags:
      - Page
      - Videos
    post:
      summary: Post Page Veos
      description: Publishes a video to the page
      operationId: postPageVeos
      x-api-path-slug: pagevideos-post
      parameters:
      - in: query
        name: description
        description: Video description
      - in: path
        name: page
        description: Represents the ID of the page object
      - in: query
        name: title
        description: Video title
      responses:
        200:
          description: OK
      tags:
      - Page
      - Videos
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