{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Default Reviewers Target Username",
    "_postman_id": "07369287-de5c-4513-b82d-0550543879ee",
    "description": "Returns the specified reviewer.\n\nThis can be used to test whether a user is among the repository's\ndefault reviewers list. A 404 indicates that that specified user is not\na default reviewer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "3ee20676-c914-4be3-929b-23090deac06d",
          "name": "getRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/default-reviewers/:target_username"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "repo_slug",
                  "value": "repo_slug",
                  "type": "string"
                },
                {
                  "id": "target_username",
                  "value": "target_username",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the specified reviewer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "47a2a9d9-27ef-49e8-9782-95b068ee5f92"
            }
          ]
        }
      ]
    }
  ]
}