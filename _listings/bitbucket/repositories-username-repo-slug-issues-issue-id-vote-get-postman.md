{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue  Vote",
    "_postman_id": "9c0ab72b-a0ae-4f6e-9728-76d51b14ca93",
    "description": "Check whether the authenticated user has voted for this issue.\nA 204 status code indicates that the user has voted, while a 404\nimplies they haven't.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "4a9db5d1-7d9d-4ec3-9704-d3e440cbd936",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssueVote",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/vote"
              ],
              "variable": [
                {
                  "id": "issue_id",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Check whether the authenticated user has voted for this issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0718df6e-60ee-4f06-a37c-cd4b8e40e125"
            }
          ]
        }
      ]
    }
  ]
}