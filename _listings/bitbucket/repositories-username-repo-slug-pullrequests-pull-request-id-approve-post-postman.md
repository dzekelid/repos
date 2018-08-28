{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Pullrequests Pull Request  Approve",
    "_postman_id": "2d0e1d19-df3d-433c-9fa1-32957d34d257",
    "description": "Post repositories username repo slug pullrequests pull request  approve",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "a55b0653-f8c5-4b94-8ec7-7c287eb0d869",
          "name": "postRepositoriesUsernameRepoSlugPullrequestsPullRequestApprove",
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Post repositories username repo slug pullrequests pull request  approve"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0bef04aa-c790-4bdd-8d10-8bc73b56c4f3"
            }
          ]
        }
      ]
    }
  ]
}