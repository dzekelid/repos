---
swagger: "2.0"
x-collection-name: AWS CodeCommit
x-complete: 0
info:
  title: AWS CodeCommit API List Repositories
  version: 1.0.0
  description: Gets information about one or more repositories.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=BatchGetRepositories:
    get:
      summary: Batch Get Repositories
      description: Returns information about one or more repositories.
      operationId: batchGetRepositories
      x-api-path-slug: actionbatchgetrepositories-get
      parameters:
      - in: query
        name: repositoryNames
        description: The names of the repositories to get information about
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repositories
  /?Action=CreateRepository:
    get:
      summary: Create Repository
      description: Creates a new, empty repository.
      operationId: createRepository
      x-api-path-slug: actioncreaterepository-get
      parameters:
      - in: query
        name: repositoryDescription
        description: A comment or description about the new repository
        type: string
      - in: query
        name: repositoryName
        description: The name of the new repository to be created
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repositories
  /?Action=DeleteRepository:
    get:
      summary: Delete Repository
      description: Deletes a repository.
      operationId: deleteRepository
      x-api-path-slug: actiondeleterepository-get
      parameters:
      - in: query
        name: repositoryName
        description: The name of the repository to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repositories
  /?Action=GetRepository:
    get:
      summary: Get Repository
      description: Returns information about a repository.
      operationId: getRepository
      x-api-path-slug: actiongetrepository-get
      parameters:
      - in: query
        name: repositoryName
        description: The name of the repository to get information about
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repositories
  /?Action=GetRepositoryTriggers:
    get:
      summary: Get Repository Triggers
      description: Gets information about triggers configured for a repository.
      operationId: getRepositoryTriggers
      x-api-path-slug: actiongetrepositorytriggers-get
      parameters:
      - in: query
        name: repositoryName
        description: The name of the repository for which the trigger is configured
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repository Triggers
  /?Action=ListRepositories:
    get:
      summary: List Repositories
      description: Gets information about one or more repositories.
      operationId: listRepositories
      x-api-path-slug: actionlistrepositories-get
      parameters:
      - in: query
        name: nextToken
        description: An enumeration token that allows the operation to batch the results
          of the operation
        type: string
      - in: query
        name: order
        description: The order in which to sort the results of a list repositories
          operation
        type: string
      - in: query
        name: sortBy
        description: The criteria used to sort the results of a list repositories
          operation
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repositories
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