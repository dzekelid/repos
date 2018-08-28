---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Orgs Org Repos
  description: List repositories for the specified org.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /legacy/repos/search/{keyword}:
    get:
      summary: Get Legacy Repos Search Keyword
      description: Find repositories by keyword. Note, this legacy method does not
        follow the v3 pagination pattern. This method returns up to 100 results per
        page and pages can be fetched using the start_page parameter.
      operationId: find-repositories-by-keyword-note-this-legacy-method-does-not-follow-the-v3-pagination-pattern-this-
      x-api-path-slug: legacyrepossearchkeyword-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: keyword
        description: The search term
      - in: query
        name: language
        description: Filter results by language
      - in: query
        name: order
        description: The sort field
      - in: query
        name: sort
        description: The sort field
      - in: query
        name: start_page
        description: The page number to fetch
      responses:
        200:
          description: OK
      tags:
      - Legacy
      - Repos
      - Search
      - Keyword
  /orgs/{org}/repos:
    get:
      summary: Get Orgs Org Repos
      description: List repositories for the specified org.
      operationId: list-repositories-for-the-specified-org
      x-api-path-slug: orgsorgrepos-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: query
        name: type
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Repos
x-streamrank:
  polling_total_time_average: "0.34"
  polling_size_download_average: "155974.55"
  streaming_total_time_average: "0.18"
  streaming_size_download_average: "78054.21"
  change_yes: "4"
  change_no: "2334"
  time_percentage: "46"
  size_percentage: "50"
  change_percentage: "0"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---