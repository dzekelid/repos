{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Pullrequests Pull Request  Decline",
    "_postman_id": "d0da192c-922b-4413-ab75-732483c9abf9",
    "description": "Post repositories username repo slug pullrequests pull request  decline",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "ab9912a8-7713-40a1-8f97-b5558dff605d",
          "name": "postRepositoriesUsernameRepoSlugPullrequestsPullRequestDecline",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/decline"
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
            "description": "Post repositories username repo slug pullrequests pull request  decline"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c39c3956-2a32-495a-bcec-a8f59829c997"
            }
          ]
        }
      ]
    }
  ]
}