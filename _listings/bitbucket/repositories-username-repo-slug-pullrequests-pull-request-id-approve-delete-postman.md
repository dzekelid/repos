{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Pullrequests Pull Request  Approve",
    "_postman_id": "0e4d0889-3ef3-4829-a81c-fee33533dea4",
    "description": "Delete repositories username repo slug pullrequests pull request  approve",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "78e0ed81-e520-4983-97a3-7b9e819cc24b",
          "name": "deleteRepositoriesUsernameRepoSlugPullrequestsPullRequestApprove",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/approve"
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
                  "id": "pull_request_id",
                  "value": "pull_request_id",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete repositories username repo slug pullrequests pull request  approve"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "949cae20-c770-4785-a387-1490476309ac"
            }
          ]
        }
      ]
    }
  ]
}