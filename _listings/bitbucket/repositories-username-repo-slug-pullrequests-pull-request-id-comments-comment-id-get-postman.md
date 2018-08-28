{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Comments Comment",
    "_postman_id": "284dcac7-ac8c-4887-9567-0173f9be1f46",
    "description": "Get repositories username repo slug pullrequests pull request  comments comment",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "cd40357a-bee1-47ab-83da-979309ced126",
          "name": "getRepositoriesUsernameRepoSlugPullrequestsPullRequestCommentsComment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/comments/:comment_id"
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
                },
                {
                  "id": "comment_id",
                  "value": "comment_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug pullrequests pull request  comments comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a410b0bd-2866-4fdc-b7b9-657ef91176c9"
            }
          ]
        }
      ]
    }
  ]
}