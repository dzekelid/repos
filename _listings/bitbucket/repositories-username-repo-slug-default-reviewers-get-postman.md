{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Default Reviewers",
    "_postman_id": "35fc60b8-70ce-42d7-8c0b-954b3b09580c",
    "description": "Returns the repository's default reviewers.\n\nThese are the users that are automatically added as reviewers on every\nnew pull request that is created.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "294259e2-6916-4519-af57-0445def80420",
          "name": "getRepositoriesUsernameRepoSlugDefaultReviewers",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/default-reviewers"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the repository's default reviewers"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b07e5b14-9ab3-41e4-bed9-f9df666e2e2d"
            }
          ]
        }
      ]
    }
  ]
}