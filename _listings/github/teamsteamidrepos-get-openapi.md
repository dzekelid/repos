---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Teams Team Repos
  description: List team repos
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
  /repos/{owner}/{repo}/branches:
    get:
      summary: Get Repos Owner Repo Branches
      description: Get list of branches
      operationId: get-list-of-branches
      x-api-path-slug: reposownerrepobranches-get
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
      - Branches
  /repos/{owner}/{repo}/branches/{branch}:
    get:
      summary: Get Repos Owner Repo Branches Branch
      description: Get Branch
      operationId: get-branch
      x-api-path-slug: reposownerrepobranchesbranch-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: branch
        description: Name of the branch
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
      - Branches
      - Branch
  /repos/{owner}/{repo}/collaborators:
    get:
      summary: Get Repos Owner Repo Collaborators
      description: |-
        List.
        When authenticating as an organization owner of an organization-owned
        repository, all organization owners are included in the list of
        collaborators. Otherwise, only users with access to the repository are
        returned in the collaborators list.
      operationId: listwhen-authenticating-as-an-organization-owner-of-an-organizationownedrepository-all-organization-
      x-api-path-slug: reposownerrepocollaborators-get
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
      - Collaborators
  /repos/{owner}/{repo}/collaborators/{user}:
    delete:
      summary: Delete Repos Owner Repo Collaborators User
      description: Remove collaborator.
      operationId: remove-collaborator
      x-api-path-slug: reposownerrepocollaboratorsuser-delete
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
      - in: path
        name: user
        description: Login of the user
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Collaborators
      - User
    get:
      summary: Get Repos Owner Repo Collaborators User
      description: Check if user is a collaborator
      operationId: check-if-user-is-a-collaborator
      x-api-path-slug: reposownerrepocollaboratorsuser-get
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
      - in: path
        name: user
        description: Login of the user
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Collaborators
      - User
    put:
      summary: Put Repos Owner Repo Collaborators User
      description: Add collaborator.
      operationId: add-collaborator
      x-api-path-slug: reposownerrepocollaboratorsuser-put
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
      - in: path
        name: user
        description: Login of the user
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Collaborators
      - User
  /repos/{owner}/{repo}/comments:
    get:
      summary: Get Repos Owner Repo Comments
      description: |-
        List commit comments for a repository.
        Comments are ordered by ascending ID.
      operationId: list-commit-comments-for-a-repositorycomments-are-ordered-by-ascending-id
      x-api-path-slug: reposownerrepocomments-get
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
      - Comments
  /repos/{owner}/{repo}/comments/{commentId}:
    delete:
      summary: Delete Repos Owner Repo Comments Comment
      description: Delete a commit comment
      operationId: delete-a-commit-comment
      x-api-path-slug: reposownerrepocommentscommentid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: Id of comment
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
      - Comments
      - Comment
    get:
      summary: Get Repos Owner Repo Comments Comment
      description: Get a single commit comment.
      operationId: get-a-single-commit-comment
      x-api-path-slug: reposownerrepocommentscommentid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: Id of comment
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
      - Comments
      - Comment
    patch:
      summary: Patch Repos Owner Repo Comments Comment
      description: Update a commit comment.
      operationId: update-a-commit-comment
      x-api-path-slug: reposownerrepocommentscommentid-patch
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
        name: commentId
        description: Id of comment
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
      - Comments
      - Comment
  /repos/{owner}/{repo}/commits:
    get:
      summary: Get Repos Owner Repo Commits
      description: List commits on a repository.
      operationId: list-commits-on-a-repository
      x-api-path-slug: reposownerrepocommits-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: author
        description: GitHub login, name, or email by which to filter by commit author
      - in: path
        name: owner
        description: Name of repository owner
      - in: query
        name: path
        description: Only commits containing this file path will be returned
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: sha
        description: Sha or branch to start listing commits from
      - in: query
        name: since
        description: 'The time should be passed in as UTC in the ISO 8601 format:
          YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: until
        description: ISO 8601 Date - Only commits before this date will be returned
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
  /repos/{owner}/{repo}/commits/{ref}/status:
    get:
      summary: Get Repos Owner Repo Commits Ref Status
      description: |-
        Get the combined Status for a specific Ref
        The Combined status endpoint is currently available for developers to preview. During the preview period, the API may change without advance notice. Please see the blog post for full details.
        To access this endpoint during the preview period, you must provide a custom media type in the Accept header:
        application/vnd.github.she-hulk-preview+json
      operationId: get-the-combined-status-for-a-specific-refthe-combined-status-endpoint-is-currently-available-for-de
      x-api-path-slug: reposownerrepocommitsrefstatus-get
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
        name: ref
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
      - Commits
      - Ref
      - Status
  /repos/{owner}/{repo}/commits/{shaCode}:
    get:
      summary: Get Repos Owner Repo Commits Shacode
      description: Get a single commit.
      operationId: get-a-single-commit
      x-api-path-slug: reposownerrepocommitsshacode-get
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
      - in: path
        name: shaCode
        description: SHA-1 code of the commit
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Shacode
  /repos/{owner}/{repo}/commits/{shaCode}/comments:
    get:
      summary: Get Repos Owner Repo Commits Shacode Comments
      description: List comments for a single commitList comments for a single commit.
      operationId: list-comments-for-a-single-commitlist-comments-for-a-single-commit
      x-api-path-slug: reposownerrepocommitsshacodecomments-get
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
      - in: path
        name: shaCode
        description: SHA-1 code of the commit
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Shacode
      - Comments
    post:
      summary: Add Repos Owner Repo Commits Shacode Comments
      description: Create a commit comment.
      operationId: create-a-commit-comment
      x-api-path-slug: reposownerrepocommitsshacodecomments-post
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
      - in: path
        name: shaCode
        description: SHA-1 code of the commit
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Commits
      - Shacode
      - Comments
  /repos/{owner}/{repo}/compare/{baseId}...{headId}:
    get:
      summary: Get Repos Owner Repo Compare Base ... Head
      description: Compare two commits
      operationId: compare-two-commits
      x-api-path-slug: reposownerrepocomparebaseid---headid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: baseId
      - in: path
        name: headId
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
      - Compare
      - Base
      - '...'
      - Head
  /repos/{owner}/{repo}/contents/{path}:
    delete:
      summary: Delete Repos Owner Repo Contents Path
      description: |-
        Delete a file.
        This method deletes a file in a repository.
      operationId: delete-a-filethis-method-deletes-a-file-in-a-repository
      x-api-path-slug: reposownerrepocontentspath-delete
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
        name: path
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
      - Contents
      - Path
    get:
      summary: Get Repos Owner Repo Contents Path
      description: |-
        Get contents.
        This method returns the contents of a file or directory in a repository.
        Files and symlinks support a custom media type for getting the raw content.
        Directories and submodules do not support custom media types.
        Note: This API supports files up to 1 megabyte in size.
        Here can be many outcomes. For details see "http://developer.github.com/v3/repos/contents/"
      operationId: get-contentsthis-method-returns-the-contents-of-a-file-or-directory-in-a-repositoryfiles-and-symlink
      x-api-path-slug: reposownerrepocontentspath-get
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
        name: path
      - in: query
        name: path
        description: The content path
      - in: query
        name: ref
        description: The String name of the Commit/Branch/Tag
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
      - Contents
      - Path
    put:
      summary: Put Repos Owner Repo Contents Path
      description: Create a file.
      operationId: create-a-file
      x-api-path-slug: reposownerrepocontentspath-put
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
        name: path
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
      - Contents
      - Path
  /repos/{owner}/{repo}/contributors:
    get:
      summary: Get Repos Owner Repo Contributors
      description: Get list of contributors.
      operationId: get-list-of-contributors
      x-api-path-slug: reposownerrepocontributors-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: anon
        description: Set to 1 or true to include anonymous contributors in results
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
      - Contributors
  /repos/{owner}/{repo}/deployments:
    get:
      summary: Get Repos Owner Repo Deployments
      description: Users with pull access can view deployments for a repository
      operationId: users-with-pull-access-can-view-deployments-for-a-repository
      x-api-path-slug: reposownerrepodeployments-get
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
      - Deployments
    post:
      summary: Add Repos Owner Repo Deployments
      description: Users with push access can create a deployment for a given ref
      operationId: users-with-push-access-can-create-a-deployment-for-a-given-ref
      x-api-path-slug: reposownerrepodeployments-post
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
      - Deployments
  /repos/{owner}/{repo}/deployments/{id}/statuses:
    get:
      summary: Get Repos Owner Repo Deployments  Statuses
      description: Users with pull access can view deployment statuses for a deployment
      operationId: users-with-pull-access-can-view-deployment-statuses-for-a-deployment
      x-api-path-slug: reposownerrepodeploymentsidstatuses-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
        description: The Deployment ID to list the statuses from
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
      - Deployments
      - ""
      - Statuses
    post:
      summary: Add Repos Owner Repo Deployments  Statuses
      description: |-
        Create a Deployment Status
        Users with push access can create deployment statuses for a given deployment:
      operationId: create-a-deployment-statususers-with-push-access-can-create-deployment-statuses-for-a-given-deployme
      x-api-path-slug: reposownerrepodeploymentsidstatuses-post
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
        name: id
        description: The Deployment ID to list the statuses from
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
      - Deployments
      - ""
      - Statuses
  /repos/{owner}/{repo}/downloads:
    get:
      summary: Get Repos Owner Repo Downloads
      description: Deprecated. List downloads for a repository.
      operationId: deprecated-list-downloads-for-a-repository
      x-api-path-slug: reposownerrepodownloads-get
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
      - Downloads
  /repos/{owner}/{repo}/downloads/{downloadId}:
    delete:
      summary: Delete Repos Owner Repo Downloads Download
      description: Deprecated. Delete a download.
      operationId: deprecated-delete-a-download
      x-api-path-slug: reposownerrepodownloadsdownloadid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: downloadId
        description: Id of download
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
      - Downloads
      - Download
    get:
      summary: Get Repos Owner Repo Downloads Download
      description: Deprecated. Get a single download.
      operationId: deprecated-get-a-single-download
      x-api-path-slug: reposownerrepodownloadsdownloadid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: downloadId
        description: Id of download
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
      - Downloads
      - Download
  /repos/{owner}/{repo}/events:
    get:
      summary: Get Repos Owner Repo Events
      description: Get list of repository events.
      operationId: get-list-of-repository-events
      x-api-path-slug: reposownerrepoevents-get
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
      - Events
  /repos/{owner}/{repo}/forks:
    get:
      summary: Get Repos Owner Repo Forks
      description: List forks.
      operationId: list-forks
      x-api-path-slug: reposownerrepoforks-get
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
      - in: query
        name: sort
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Forks
    post:
      summary: Add Repos Owner Repo Forks
      description: |-
        Create a fork.
        Forking a Repository happens asynchronously. Therefore, you may have to wai
        a short period before accessing the git objects. If this takes longer than 5
        minutes, be sure to contact Support.
      operationId: create-a-forkforking-a-repository-happens-asynchronously-therefore-you-may-have-to-waia-short-period
      x-api-path-slug: reposownerrepoforks-post
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
      - Forks
  /repos/{owner}/{repo}/git/blobs:
    post:
      summary: Add Repos Owner Repo Git Blobs
      description: Create a Blob.
      operationId: create-a-blob
      x-api-path-slug: reposownerrepogitblobs-post
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
      - Git
      - Blobs
  /repos/{owner}/{repo}/git/blobs/{shaCode}:
    get:
      summary: Get Repos Owner Repo Git Blobs Shacode
      description: |-
        Get a Blob.
        Since blobs can be any arbitrary binary data, the input and responses for
        the blob API takes an encoding parameter that can be either utf-8 or
        base64. If your data cannot be losslessly sent as a UTF-8 string, you can
        base64 encode it.
      operationId: get-a-blobsince-blobs-can-be-any-arbitrary-binary-data-the-input-and-responses-forthe-blob-api-takes
      x-api-path-slug: reposownerrepogitblobsshacode-get
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
      - in: path
        name: shaCode
        description: SHA-1 code
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Git
      - Blobs
      - Shacode
  /repos/{owner}/{repo}/git/commits:
    post:
      summary: Add Repos Owner Repo Git Commits
      description: Create a Commit.
      operationId: create-a-commit
      x-api-path-slug: reposownerrepogitcommits-post
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
      - Git
      - Commits
  /repos/{owner}/{repo}/git/commits/{shaCode}:
    get:
      summary: Get Repos Owner Repo Git Commits Shacode
      description: Get a Commit.
      operationId: get-a-commit
      x-api-path-slug: reposownerrepogitcommitsshacode-get
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
      - in: path
        name: shaCode
        description: SHA-1 code
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Git
      - Commits
      - Shacode
  /repos/{owner}/{repo}/git/refs:
    get:
      summary: Get Repos Owner Repo Git Refs
      description: Get all References
      operationId: get-all-references
      x-api-path-slug: reposownerrepogitrefs-get
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
      - Git
      - Refs
    post:
      summary: Add Repos Owner Repo Git Refs
      description: Create a Reference
      operationId: create-a-reference
      x-api-path-slug: reposownerrepogitrefs-post
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
      - Git
      - Refs
  /repos/{owner}/{repo}/git/refs/{ref}:
    delete:
      summary: Delete Repos Owner Repo Git Refs Ref
      description: "Delete a Reference\nExample: Deleting a branch: DELETE /repos/octocat/Hello-World/git/refs/heads/feature-a
        \nExample: Deleting a tag:        DELETE /repos/octocat/Hello-World/git/refs/tags/v1.0"
      operationId: delete-a-referenceexample-deleting-a-branch-delete-reposoctocathelloworldgitrefsheadsfeaturea-exampl
      x-api-path-slug: reposownerrepogitrefsref-delete
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
        name: ref
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
      - Git
      - Refs
      - Ref
    get:
      summary: Get Repos Owner Repo Git Refs Ref
      description: Get a Reference
      operationId: get-a-reference
      x-api-path-slug: reposownerrepogitrefsref-get
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
        name: ref
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
      - Git
      - Refs
      - Ref
    patch:
      summary: Patch Repos Owner Repo Git Refs Ref
      description: Update a Reference
      operationId: update-a-reference
      x-api-path-slug: reposownerrepogitrefsref-patch
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
        name: ref
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
      - Git
      - Refs
      - Ref
  /repos/{owner}/{repo}/git/tags:
    post:
      summary: Add Repos Owner Repo Git Tags
      description: |-
        Create a Tag Object.
        Note that creating a tag object does not create the reference that makes a
        tag in Git. If you want to create an annotated tag in Git, you have to do
        this call to create the tag object, and then create the refs/tags/[tag]
        reference. If you want to create a lightweight tag, you only have to create
        the tag reference - this call would be unnecessary.
      operationId: create-a-tag-objectnote-that-creating-a-tag-object-does-not-create-the-reference-that-makes-atag-in-
      x-api-path-slug: reposownerrepogittags-post
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
      - Git
      - Tags
  /repos/{owner}/{repo}/git/tags/{shaCode}:
    get:
      summary: Get Repos Owner Repo Git Tags Shacode
      description: Get a Tag.
      operationId: get-a-tag
      x-api-path-slug: reposownerrepogittagsshacode-get
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
      - in: path
        name: shaCode
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Git
      - Tags
      - Shacode
  /repos/{owner}/{repo}/git/trees:
    post:
      summary: Add Repos Owner Repo Git Trees
      description: |-
        Create a Tree.
        The tree creation API will take nested entries as well. If both a tree and
        a nested path modifying that tree are specified, it will overwrite the
        contents of that tree with the new path contents and write a new tree out.
      operationId: create-a-treethe-tree-creation-api-will-take-nested-entries-as-well-if-both-a-tree-anda-nested-path-
      x-api-path-slug: reposownerrepogittrees-post
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
      - Git
      - Trees
  /repos/{owner}/{repo}/git/trees/{shaCode}:
    get:
      summary: Get Repos Owner Repo Git Trees Shacode
      description: Get a Tree.
      operationId: get-a-tree
      x-api-path-slug: reposownerrepogittreesshacode-get
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
      - in: query
        name: recursive
        description: Get a Tree Recursively
      - in: path
        name: repo
        description: Name of repository
      - in: path
        name: shaCode
        description: Tree SHA
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Git
      - Trees
      - Shacode
  /repos/{owner}/{repo}/hooks:
    get:
      summary: Get Repos Owner Repo Hooks
      description: Get list of hooks.
      operationId: get-list-of-hooks
      x-api-path-slug: reposownerrepohooks-get
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
      - Hooks
    post:
      summary: Add Repos Owner Repo Hooks
      description: Create a hook.
      operationId: create-a-hook
      x-api-path-slug: reposownerrepohooks-post
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
      - Hooks
  /repos/{owner}/{repo}/hooks/{hookId}:
    delete:
      summary: Delete Repos Owner Repo Hooks Hook
      description: Delete a hook.
      operationId: delete-a-hook
      x-api-path-slug: reposownerrepohookshookid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: hookId
        description: Id of hook
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
      - Hooks
      - Hook
    get:
      summary: Get Repos Owner Repo Hooks Hook
      description: Get single hook.
      operationId: get-single-hook
      x-api-path-slug: reposownerrepohookshookid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: hookId
        description: Id of hook
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
      - Hooks
      - Hook
    patch:
      summary: Patch Repos Owner Repo Hooks Hook
      description: Edit a hook.
      operationId: edit-a-hook
      x-api-path-slug: reposownerrepohookshookid-patch
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
        name: hookId
        description: Id of hook
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
      - Hooks
      - Hook
  /repos/{owner}/{repo}/hooks/{hookId}/tests:
    post:
      summary: Add Repos Owner Repo Hooks Hook Tests
      description: |-
        Test a push hook.
        This will trigger the hook with the latest push to the current repository
        if the hook is subscribed to push events. If the hook is not subscribed
        to push events, the server will respond with 204 but no test POST will
        be generated.
        Note: Previously /repos/:owner/:repo/hooks/:id/tes
      operationId: test-a-push-hookthis-will-trigger-the-hook-with-the-latest-push-to-the-current-repositoryif-the-hook
      x-api-path-slug: reposownerrepohookshookidtests-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: hookId
        description: Id of hook
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
      - Hooks
      - Hook
      - Tests
  /repos/{owner}/{repo}/issues:
    get:
      summary: Get Repos Owner Repo Issues
      description: List issues for a repository.
      operationId: list-issues-for-a-repository
      x-api-path-slug: reposownerrepoissues-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
      - in: query
        name: filter
        description: Issues assigned to you / created by you / mentioning you / youresubscribed
          to updates for / All issues the authenticated user can see
      - in: query
        name: labels
        description: String list of comma separated Label names
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: since
        description: 'Optional string of a timestamp in ISO 8601 format: YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: sort
      - in: query
        name: state
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Issues
    post:
      summary: Add Repos Owner Repo Issues
      description: |-
        Create an issue.
        Any user with pull access to a repository can create an issue.
      operationId: create-an-issueany-user-with-pull-access-to-a-repository-can-create-an-issue
      x-api-path-slug: reposownerrepoissues-post
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
      - Issues
  /repos/{owner}/{repo}/issues/comments:
    get:
      summary: Get Repos Owner Repo Issues Comments
      description: List comments in a repository.
      operationId: list-comments-in-a-repository
      x-api-path-slug: reposownerrepoissuescomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
        description: Ignored without sort parameter
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: since
        description: 'The time should be passed in as UTC in the ISO 8601 format:
          YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: sort
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Issues
      - Comments
  /repos/{owner}/{repo}/issues/comments/{commentId}:
    delete:
      summary: Delete Repos Owner Repo Issues Comments Comment
      description: Delete a comment.
      operationId: delete-a-comment
      x-api-path-slug: reposownerrepoissuescommentscommentid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: ID of comment
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
      - Issues
      - Comments
      - Comment
    get:
      summary: Get Repos Owner Repo Issues Comments Comment
      description: Get a single comment.
      operationId: get-a-single-comment
      x-api-path-slug: reposownerrepoissuescommentscommentid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: ID of comment
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
      - Issues
      - Comments
      - Comment
    patch:
      summary: Patch Repos Owner Repo Issues Comments Comment
      description: Edit a comment.
      operationId: edit-a-comment
      x-api-path-slug: reposownerrepoissuescommentscommentid-patch
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
        name: commentId
        description: ID of comment
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
      - Issues
      - Comments
      - Comment
  /repos/{owner}/{repo}/issues/events:
    get:
      summary: Get Repos Owner Repo Issues Events
      description: List issue events for a repository.
      operationId: list-issue-events-for-a-repository
      x-api-path-slug: reposownerrepoissuesevents-get
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
      - Issues
      - Events
  /repos/{owner}/{repo}/issues/events/{eventId}:
    get:
      summary: Get Repos Owner Repo Issues Events Event
      description: Get a single event.
      operationId: get-a-single-event
      x-api-path-slug: reposownerrepoissueseventseventid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: eventId
        description: Id of the event
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
      - Issues
      - Events
      - Event
  /repos/{owner}/{repo}/issues/{number}:
    get:
      summary: Get Repos Owner Repo Issues Number
      description: Get a single issue
      operationId: get-a-single-issue
      x-api-path-slug: reposownerrepoissuesnumber-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of issue
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
      - Issues
      - Number
    patch:
      summary: Patch Repos Owner Repo Issues Number
      description: |-
        Edit an issue.
        Issue owners and users with push access can edit an issue.
      operationId: edit-an-issueissue-owners-and-users-with-push-access-can-edit-an-issue
      x-api-path-slug: reposownerrepoissuesnumber-patch
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
        name: number
        description: Number of issue
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
      - Issues
      - Number
  /repos/{owner}/{repo}/issues/{number}/comments:
    get:
      summary: Get Repos Owner Repo Issues Number Comments
      description: List comments on an issue.
      operationId: list-comments-on-an-issue
      x-api-path-slug: reposownerrepoissuesnumbercomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Comments
    post:
      summary: Add Repos Owner Repo Issues Number Comments
      description: Create a comment.
      operationId: create-a-comment
      x-api-path-slug: reposownerrepoissuesnumbercomments-post
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
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Comments
  /repos/{owner}/{repo}/issues/{number}/events:
    get:
      summary: Get Repos Owner Repo Issues Number Events
      description: List events for an issue.
      operationId: list-events-for-an-issue
      x-api-path-slug: reposownerrepoissuesnumberevents-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Events
  /repos/{owner}/{repo}/issues/{number}/labels:
    delete:
      summary: Delete Repos Owner Repo Issues Number Labels
      description: Remove all labels from an issue.
      operationId: remove-all-labels-from-an-issue
      x-api-path-slug: reposownerrepoissuesnumberlabels-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Labels
    get:
      summary: Get Repos Owner Repo Issues Number Labels
      description: List labels on an issue.
      operationId: list-labels-on-an-issue
      x-api-path-slug: reposownerrepoissuesnumberlabels-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Labels
    post:
      summary: Add Repos Owner Repo Issues Number Labels
      description: Add labels to an issue.
      operationId: add-labels-to-an-issue
      x-api-path-slug: reposownerrepoissuesnumberlabels-post
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
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Labels
    put:
      summary: Put Repos Owner Repo Issues Number Labels
      description: |-
        Replace all labels for an issue.
        Sending an empty array ([]) will remove all Labels from the Issue.
      operationId: replace-all-labels-for-an-issuesending-an-empty-array--will-remove-all-labels-from-the-issue
      x-api-path-slug: reposownerrepoissuesnumberlabels-put
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
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Labels
  /repos/{owner}/{repo}/issues/{number}/labels/{name}:
    delete:
      summary: Delete Repos Owner Repo Issues Number Labels Name
      description: Remove a label from an issue.
      operationId: remove-a-label-from-an-issue
      x-api-path-slug: reposownerrepoissuesnumberlabelsname-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: number
        description: Number of issue
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
      - Issues
      - Number
      - Labels
      - Name
  /repos/{owner}/{repo}/keys:
    get:
      summary: Get Repos Owner Repo Keys
      description: Get list of keys.
      operationId: get-list-of-keys
      x-api-path-slug: reposownerrepokeys-get
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
      - Keys
    post:
      summary: Add Repos Owner Repo Keys
      description: Create a key.
      operationId: create-a-key
      x-api-path-slug: reposownerrepokeys-post
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
      - Keys
  /repos/{owner}/{repo}/keys/{keyId}:
    delete:
      summary: Delete Repos Owner Repo Keys Key
      description: Delete a key.
      operationId: delete-a-key
      x-api-path-slug: reposownerrepokeyskeyid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: keyId
        description: Id of key
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
      - Keys
      - Key
    get:
      summary: Get Repos Owner Repo Keys Key
      description: Get a key
      operationId: get-a-key
      x-api-path-slug: reposownerrepokeyskeyid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: keyId
        description: Id of key
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
      - Keys
      - Key
  /repos/{owner}/{repo}/labels:
    get:
      summary: Get Repos Owner Repo Labels
      description: List all labels for this repository.
      operationId: list-all-labels-for-this-repository
      x-api-path-slug: reposownerrepolabels-get
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
      - Labels
    post:
      summary: Add Repos Owner Repo Labels
      description: Create a label.
      operationId: create-a-label
      x-api-path-slug: reposownerrepolabels-post
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
      - Labels
  /repos/{owner}/{repo}/labels/{name}:
    delete:
      summary: Delete Repos Owner Repo Labels Name
      description: Delete a label.
      operationId: delete-a-label
      x-api-path-slug: reposownerrepolabelsname-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
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
      - Labels
      - Name
    get:
      summary: Get Repos Owner Repo Labels Name
      description: Get a single label.
      operationId: get-a-single-label
      x-api-path-slug: reposownerrepolabelsname-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
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
      - Labels
      - Name
    patch:
      summary: Patch Repos Owner Repo Labels Name
      description: Update a label.
      operationId: update-a-label
      x-api-path-slug: reposownerrepolabelsname-patch
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
        name: name
        description: Name of the label
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
      - Labels
      - Name
  /repos/{owner}/{repo}/languages:
    get:
      summary: Get Repos Owner Repo Languages
      description: |-
        List languages.
        List languages for the specified repository. The value on the right of a
        language is the number of bytes of code written in that language.
      operationId: list-languageslist-languages-for-the-specified-repository-the-value-on-the-right-of-alanguage-is-the
      x-api-path-slug: reposownerrepolanguages-get
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
      - Languages
  /repos/{owner}/{repo}/merges:
    post:
      summary: Add Repos Owner Repo Merges
      description: Perform a merge.
      operationId: perform-a-merge
      x-api-path-slug: reposownerrepomerges-post
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
      - Merges
  /repos/{owner}/{repo}/milestones:
    get:
      summary: Get Repos Owner Repo Milestones
      description: List milestones for a repository.
      operationId: list-milestones-for-a-repository
      x-api-path-slug: reposownerrepomilestones-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
        description: Ignored without sort parameter
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: sort
      - in: query
        name: state
        description: String to filter by state
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Milestones
    post:
      summary: Add Repos Owner Repo Milestones
      description: Create a milestone.
      operationId: create-a-milestone
      x-api-path-slug: reposownerrepomilestones-post
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
      - Milestones
  /repos/{owner}/{repo}/milestones/{number}:
    delete:
      summary: Delete Repos Owner Repo Milestones Number
      description: Delete a milestone.
      operationId: delete-a-milestone
      x-api-path-slug: reposownerrepomilestonesnumber-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of milestone
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
      - Milestones
      - Number
    get:
      summary: Get Repos Owner Repo Milestones Number
      description: Get a single milestone.
      operationId: get-a-single-milestone
      x-api-path-slug: reposownerrepomilestonesnumber-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of milestone
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
      - Milestones
      - Number
    patch:
      summary: Patch Repos Owner Repo Milestones Number
      description: Update a milestone.
      operationId: update-a-milestone
      x-api-path-slug: reposownerrepomilestonesnumber-patch
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
        name: number
        description: Number of milestone
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
      - Milestones
      - Number
  /repos/{owner}/{repo}/milestones/{number}/labels:
    get:
      summary: Get Repos Owner Repo Milestones Number Labels
      description: Get labels for every issue in a milestone.
      operationId: get-labels-for-every-issue-in-a-milestone
      x-api-path-slug: reposownerrepomilestonesnumberlabels-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of milestone
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
      - Milestones
      - Number
      - Labels
  /repos/{owner}/{repo}/notifications:
    get:
      summary: Get Repos Owner Repo Notifications
      description: |-
        List your notifications in a repository
        List all notifications for the current user.
      operationId: list-your-notifications-in-a-repositorylist-all-notifications-for-the-current-user
      x-api-path-slug: reposownerreponotifications-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: all
        description: True to show notifications marked as read
      - in: path
        name: owner
        description: Name of repository owner
      - in: query
        name: participating
        description: True to show only notifications in which the user is directly
          participatingor mentioned
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: since
        description: 'The time should be passed in as UTC in the ISO 8601 format:
          YYYY-MM-DDTHH:MM:SSZ'
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Notifications
    put:
      summary: Put Repos Owner Repo Notifications
      description: |-
        Mark notifications as read in a repository.
        Marking all notifications in a repository as "read" removes them from the
        default view on GitHub.com.
      operationId: mark-notifications-as-read-in-a-repositorymarking-all-notifications-in-a-repository-as-read-removes-
      x-api-path-slug: reposownerreponotifications-put
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
      - Notifications
  /repos/{owner}/{repo}/pulls:
    get:
      summary: Get Repos Owner Repo Pulls
      description: List pull requests.
      operationId: list-pull-requests
      x-api-path-slug: reposownerrepopulls-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: base
        description: Filter pulls by base branch name
      - in: query
        name: head
        description: Filter pulls by head user and branch name in the format of user:ref-name
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: state
        description: String to filter by state
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
    post:
      summary: Add Repos Owner Repo Pulls
      description: Create a pull request.
      operationId: create-a-pull-request
      x-api-path-slug: reposownerrepopulls-post
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
      - Pulls
  /repos/{owner}/{repo}/pulls/comments:
    get:
      summary: Get Repos Owner Repo Pulls Comments
      description: |-
        List comments in a repository.
        By default, Review Comments are ordered by ascending ID.
      operationId: list-comments-in-a-repositoryby-default-review-comments-are-ordered-by-ascending-id
      x-api-path-slug: reposownerrepopullscomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
        description: Ignored without sort parameter
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: since
        description: 'The time should be passed in as UTC in the ISO 8601 format:
          YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: sort
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Comments
  /repos/{owner}/{repo}/pulls/comments/{commentId}:
    delete:
      summary: Delete Repos Owner Repo Pulls Comments Comment
      description: Delete a comment.
      operationId: delete-a-comment
      x-api-path-slug: reposownerrepopullscommentscommentid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: Id of comment
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
      - Pulls
      - Comments
      - Comment
    get:
      summary: Get Repos Owner Repo Pulls Comments Comment
      description: Get a single comment.
      operationId: get-a-single-comment
      x-api-path-slug: reposownerrepopullscommentscommentid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: Id of comment
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
      - Pulls
      - Comments
      - Comment
    patch:
      summary: Patch Repos Owner Repo Pulls Comments Comment
      description: Edit a comment.
      operationId: edit-a-comment
      x-api-path-slug: reposownerrepopullscommentscommentid-patch
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
        name: commentId
        description: Id of comment
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
      - Pulls
      - Comments
      - Comment
  /repos/{owner}/{repo}/pulls/{number}:
    get:
      summary: Get Repos Owner Repo Pulls Number
      description: Get a single pull request.
      operationId: get-a-single-pull-request
      x-api-path-slug: reposownerrepopullsnumber-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
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
      - Pulls
      - Number
    patch:
      summary: Patch Repos Owner Repo Pulls Number
      description: Update a pull request.
      operationId: update-a-pull-request
      x-api-path-slug: reposownerrepopullsnumber-patch
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
        name: number
        description: Id of pull
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
      - Pulls
      - Number
  /repos/{owner}/{repo}/pulls/{number}/comments:
    get:
      summary: Get Repos Owner Repo Pulls Number Comments
      description: List comments on a pull request.
      operationId: list-comments-on-a-pull-request
      x-api-path-slug: reposownerrepopullsnumbercomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
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
      - Pulls
      - Number
      - Comments
    post:
      summary: Add Repos Owner Repo Pulls Number Comments
      description: |-
        Create a comment.
          #TODO Alternative input ( http://developer.github.com/v3/pulls/comments/ )
          description: |
            Alternative Input.
            Instead of passing commit_id, path, and position you can reply to an
            existing Pull Request Comment like this:

                body
                   Required string
                in_reply_to
                   Required number - Comment id to reply to.
      operationId: create-a-comment--todo-alternative-input--httpdevelopergithubcomv3pullscomments---description-----al
      x-api-path-slug: reposownerrepopullsnumbercomments-post
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
        name: number
        description: Id of pull
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
      - Pulls
      - Number
      - Comments
  /repos/{owner}/{repo}/pulls/{number}/commits:
    get:
      summary: Get Repos Owner Repo Pulls Number Commits
      description: List commits on a pull request.
      operationId: list-commits-on-a-pull-request
      x-api-path-slug: reposownerrepopullsnumbercommits-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
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
      - Pulls
      - Number
      - Commits
  /repos/{owner}/{repo}/pulls/{number}/files:
    get:
      summary: Get Repos Owner Repo Pulls Number Files
      description: List pull requests files.
      operationId: list-pull-requests-files
      x-api-path-slug: reposownerrepopullsnumberfiles-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
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
      - Pulls
      - Number
      - Files
  /repos/{owner}/{repo}/pulls/{number}/merge:
    get:
      summary: Get Repos Owner Repo Pulls Number Merge
      description: Get if a pull request has been merged.
      operationId: get-if-a-pull-request-has-been-merged
      x-api-path-slug: reposownerrepopullsnumbermerge-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
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
      - Pulls
      - Number
      - Merge
    put:
      summary: Put Repos Owner Repo Pulls Number Merge
      description: Merge a pull request (Merge Button's)
      operationId: merge-a-pull-request-merge-buttons
      x-api-path-slug: reposownerrepopullsnumbermerge-put
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
        name: number
        description: Id of pull
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
      - Pulls
      - Number
      - Merge
  /repos/{owner}/{repo}/readme:
    get:
      summary: Get Repos Owner Repo Readme
      description: |-
        Get the README.
        This method returns the preferred README for a repository.
      operationId: get-the-readmethis-method-returns-the-preferred-readme-for-a-repository
      x-api-path-slug: reposownerreporeadme-get
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
      - in: query
        name: ref
        description: The String name of the Commit/Branch/Tag
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
      - Readme
  /repos/{owner}/{repo}/releases:
    get:
      summary: Get Repos Owner Repo Releases
      description: Users with push access to the repository will receive all releases
        (i.e., published releases and draft releases). Users with pull access will
        receive published releases only
      operationId: users-with-push-access-to-the-repository-will-receive-all-releases-ie-published-releases-and-draft-r
      x-api-path-slug: reposownerreporeleases-get
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
      - Releases
    post:
      summary: Add Repos Owner Repo Releases
      description: |-
        Create a release
        Users with push access to the repository can create a release.
      operationId: create-a-releaseusers-with-push-access-to-the-repository-can-create-a-release
      x-api-path-slug: reposownerreporeleases-post
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
      - Releases
  /repos/{owner}/{repo}/releases/assets/{id}:
    delete:
      summary: Delete Repos Owner Repo Releases Assets
      description: Delete a release asset
      operationId: delete-a-release-asset
      x-api-path-slug: reposownerreporeleasesassetsid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
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
      - Releases
      - Assets
    get:
      summary: Get Repos Owner Repo Releases Assets
      description: Get a single release asset
      operationId: get-a-single-release-asset
      x-api-path-slug: reposownerreporeleasesassetsid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
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
      - Releases
      - Assets
    patch:
      summary: Patch Repos Owner Repo Releases Assets
      description: |-
        Edit a release asset
        Users with push access to the repository can edit a release asset.
      operationId: edit-a-release-assetusers-with-push-access-to-the-repository-can-edit-a-release-asset
      x-api-path-slug: reposownerreporeleasesassetsid-patch
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
        name: id
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
      - Releases
      - Assets
  /repos/{owner}/{repo}/releases/{id}:
    delete:
      summary: Delete Repos Owner Repo Releases
      description: Users with push access to the repository can delete a release.
      operationId: users-with-push-access-to-the-repository-can-delete-a-release
      x-api-path-slug: reposownerreporeleasesid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
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
      - Releases
    get:
      summary: Get Repos Owner Repo Releases
      description: Get a single release
      operationId: get-a-single-release
      x-api-path-slug: reposownerreporeleasesid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
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
      - Releases
    patch:
      summary: Patch Repos Owner Repo Releases
      description: Users with push access to the repository can edit a release
      operationId: users-with-push-access-to-the-repository-can-edit-a-release
      x-api-path-slug: reposownerreporeleasesid-patch
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
        name: id
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
      - Releases
  /repos/{owner}/{repo}/releases/{id}/assets:
    get:
      summary: Get Repos Owner Repo Releases  Assets
      description: List assets for a release
      operationId: list-assets-for-a-release
      x-api-path-slug: reposownerreporeleasesidassets-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: id
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
      - Releases
      - ""
      - Assets
  /repos/{owner}/{repo}/stargazers:
    get:
      summary: Get Repos Owner Repo Stargazers
      description: List Stargazers.
      operationId: list-stargazers
      x-api-path-slug: reposownerrepostargazers-get
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
      - Stargazers
  /repos/{owner}/{repo}/stats/code_frequency:
    get:
      summary: Get Repos Owner Repo Stats Code Frequency
      description: |-
        Get the number of additions and deletions per week.
        Returns a weekly aggregate of the number of additions and deletions pushed
        to a repository.
      operationId: get-the-number-of-additions-and-deletions-per-weekreturns-a-weekly-aggregate-of-the-number-of-additi
      x-api-path-slug: reposownerrepostatscode-frequency-get
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
      - Stats
      - Code
      - Frequency
      - Aggregation
  /repos/{owner}/{repo}/stats/commit_activity:
    get:
      summary: Get Repos Owner Repo Stats Commit Activity
      description: |-
        Get the last year of commit activity data.
        Returns the last year of commit activity grouped by week. The days array
        is a group of commits per day, starting on Sunday.
      operationId: get-the-last-year-of-commit-activity-datareturns-the-last-year-of-commit-activity-grouped-by-week-th
      x-api-path-slug: reposownerrepostatscommit-activity-get
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
      - Stats
      - Commit
      - Activity
  /repos/{owner}/{repo}/stats/contributors:
    get:
      summary: Get Repos Owner Repo Stats Contributors
      description: Get contributors list with additions, deletions, and commit counts.
      operationId: get-contributors-list-with-additions-deletions-and-commit-counts
      x-api-path-slug: reposownerrepostatscontributors-get
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
      - Stats
      - Contributors
  /repos/{owner}/{repo}/stats/participation:
    get:
      summary: Get Repos Owner Repo Stats Participation
      description: Get the weekly commit count for the repo owner and everyone else.
      operationId: get-the-weekly-commit-count-for-the-repo-owner-and-everyone-else
      x-api-path-slug: reposownerrepostatsparticipation-get
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
      - Stats
      - Participation
  /repos/{owner}/{repo}/stats/punch_card:
    get:
      summary: Get Repos Owner Repo Stats Punch Card
      description: |-
        Get the number of commits per hour in each day.
        Each array contains the day number, hour number, and number of commits
        0-6 Sunday - Saturday
        0-23 Hour of day
        Number of commits

        For example, [2, 14, 25] indicates that there were 25 total commits, during
        the 2.00pm hour on Tuesdays. All times are based on the time zone of
        individual commits.
      operationId: get-the-number-of-commits-per-hour-in-each-dayeach-array-contains-the-day-number-hour-number-and-num
      x-api-path-slug: reposownerrepostatspunch-card-get
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
      - Stats
      - Punch
      - Card
  /repos/{owner}/{repo}/statuses/{ref}:
    get:
      summary: Get Repos Owner Repo Statuses Ref
      description: List Statuses for a specific Ref.
      operationId: list-statuses-for-a-specific-ref
      x-api-path-slug: reposownerrepostatusesref-get
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
        name: ref
        description: Ref to list the statuses from
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
      - Statuses
      - Ref
    post:
      summary: Add Repos Owner Repo Statuses Ref
      description: Create a Status.
      operationId: create-a-status
      x-api-path-slug: reposownerrepostatusesref-post
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
        name: ref
        description: Ref to list the statuses from
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
      - Statuses
      - Ref
  /repos/{owner}/{repo}/subscribers:
    get:
      summary: Get Repos Owner Repo Subscribers
      description: List watchers.
      operationId: list-watchers
      x-api-path-slug: reposownerreposubscribers-get
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
      - Subscribers
  /repos/{owner}/{repo}/subscription:
    delete:
      summary: Delete Repos Owner Repo Subscription
      description: Delete a Repository Subscription.
      operationId: delete-a-repository-subscription
      x-api-path-slug: reposownerreposubscription-delete
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
      - Subscription
    get:
      summary: Get Repos Owner Repo Subscription
      description: Get a Repository Subscription.
      operationId: get-a-repository-subscription
      x-api-path-slug: reposownerreposubscription-get
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
      - Subscription
    put:
      summary: Put Repos Owner Repo Subscription
      description: Set a Repository Subscription
      operationId: set-a-repository-subscription
      x-api-path-slug: reposownerreposubscription-put
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
      - Subscription
  /repos/{owner}/{repo}/tags:
    get:
      summary: Get Repos Owner Repo Tags
      description: Get list of tags.
      operationId: get-list-of-tags
      x-api-path-slug: reposownerrepotags-get
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
      - Tags
  /repos/{owner}/{repo}/teams:
    get:
      summary: Get Repos Owner Repo Teams
      description: Get list of teams
      operationId: get-list-of-teams
      x-api-path-slug: reposownerrepoteams-get
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
      - Teams
  /repos/{owner}/{repo}/watchers:
    get:
      summary: Get Repos Owner Repo Watchers
      description: List Stargazers. New implementation.
      operationId: list-stargazers-new-implementation
      x-api-path-slug: reposownerrepowatchers-get
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
      - Watchers
  /repos/{owner}/{repo}/{archive_format}/{path}:
    get:
      summary: Get Repos Owner Repo Archive Format Path
      description: |-
        Get archive link.
        This method will return a 302 to a URL to download a tarball or zipball
        archive for a repository. Please make sure your HTTP framework is
        configured to follow redirects or you will need to use the Location header
        to make a second GET request.
        Note: For private repositories, these links are temporary and expire quickly.
      operationId: get-archive-linkthis-method-will-return-a-302-to-a-url-to-download-a-tarball-or-zipballarchive-for-a
      x-api-path-slug: reposownerrepoarchive-formatpath-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: archive_format
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: path
        description: Valid Git reference, defaults to master
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
      - Archives
      - Format
      - Path
  /teams/{teamId}/repos:
    get:
      summary: Get Teams Team Repos
      description: List team repos
      operationId: list-team-repos
      x-api-path-slug: teamsteamidrepos-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Repos
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