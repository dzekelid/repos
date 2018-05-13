{
  "info": {
    "name": "Bitbucket Update Repositories Username Repo Slug Default Reviewers Target Username",
    "_postman_id": "c3e099a7-33cb-44bc-b4a9-5285e0e55a6f",
    "description": "Adds the specified user to the repository's list of default\nreviewers.\n\nThis method is idempotent. Adding a user a second time has no effect.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "0871cf03-67ed-4015-b922-65efa1a51662",
          "name": "putRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Adds the specified user to the repository's list of default\nreviewers"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbe50aa0-8493-4115-b916-f741a2cb6f6c"
            }
          ]
        }
      ]
    }
  ]
}