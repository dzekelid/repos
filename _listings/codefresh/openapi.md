swagger: "2.0"
x-collection-name: Codefresh
x-complete: 1
info:
  title: Codefresh API
  description: codefresh-api-swagger2-0-specification
  termsOfService: http://www.codefresh.io
  contact:
    name: Codefresh api team
    url: http://www.codefresh.io
  version: 1.0.0
host: g.codefresh.io
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repos/settings/{repoOwner}/{repoName}:
    get:
      summary: Get Repos Settings Repoowner Reponame
      description: Get repos settings repoowner reponame.
      operationId: getReposSettingsRepoownerReponame
      x-api-path-slug: repossettingsrepoownerreponame-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Settings
      - Repoowner
      - Reponame
  /repos/settings:
    post:
      summary: Post Repos Settings
      description: Post repos settings.
      operationId: postReposSettings
      x-api-path-slug: repossettings-post
      parameters:
      - in: body
        name: settings
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Settings