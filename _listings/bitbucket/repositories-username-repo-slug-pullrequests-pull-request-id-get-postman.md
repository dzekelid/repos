{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request",
    "_postman_id": "13d41c0b-67fd-4453-8b18-f1b85a6cab94",
    "description": "Get repositories username repo slug pullrequests pull request",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "eaa05fd1-191b-4a79-93ff-b21a56179c8e",
          "name": "getRepositoriesUsernameRepoSlugPullrequestsPullRequest",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id"
              ],
              "variable": [
                {
                  "id": "pull_request_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "repo_slug",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "username",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug pullrequests pull request"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "582579ab-2ab8-40a6-8007-55ddde365ced"
            }
          ]
        }
      ]
    }
  ]
}