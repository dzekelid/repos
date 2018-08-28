---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Repos Owner Repo Assignees Assignee
  description: |-
    Check assignee.
    You may also check to see if a particular user is an assignee for a repository.
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
    post:
      summary: Add Orgs Org Repos
      description: |-
        Create a new repository for the authenticated user. OAuth users must supply
        repo scope.
      operationId: create-a-new-repository-for-the-authenticated-user-oauth-users-must-supplyrepo-scope
      x-api-path-slug: orgsorgrepos-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Repos
  /repos/{owner}/{repo}:
    delete:
      summary: Delete Repos Owner Repo
      description: |-
        Delete a Repository.
        Deleting a repository requires admin access. If OAuth is used, the delete_repo
        scope is required.
      operationId: delete-a-repositorydeleting-a-repository-requires-admin-access-if-oauth-is-used-the-delete-reposcope
      x-api-path-slug: reposownerrepo-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
    get:
      summary: Get Repos Owner Repo
      description: Get repository.
      operationId: get-repository
      x-api-path-slug: reposownerrepo-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
    patch:
      summary: Patch Repos Owner Repo
      description: Edit repository.
      operationId: edit-repository
      x-api-path-slug: reposownerrepo-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
  /repos/{owner}/{repo}/assignees:
    get:
      summary: Get Repos Owner Repo Assignees
      description: |-
        List assignees.
        This call lists all the available assignees (owner + collaborators) to which
        issues may be assigned.
      operationId: list-assigneesthis-call-lists-all-the-available-assignees-owner--collaborators-to-whichissues-may-be
      x-api-path-slug: reposownerrepoassignees-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Assignees
  /repos/{owner}/{repo}/assignees/{assignee}:
    get:
      summary: Get Repos Owner Repo Assignees Assignee
      description: |-
        Check assignee.
        You may also check to see if a particular user is an assignee for a repository.
      operationId: check-assigneeyou-may-also-check-to-see-if-a-particular-user-is-an-assignee-for-a-repository
      x-api-path-slug: reposownerrepoassigneesassignee-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: assignee
        description: Login of the assignee
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Assignees
      - Assignee
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