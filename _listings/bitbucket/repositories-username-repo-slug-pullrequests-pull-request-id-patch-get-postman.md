{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Patch",
    "_postman_id": "e2fc1daa-3307-4541-aa1b-b851e726c046",
    "description": "Get repositories username repo slug pullrequests pull request  patch",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "08de861a-f42f-44b6-9bbc-6a7d0bac38e0",
          "name": "getRepositoriesUsernameRepoSlugPullrequestsPullRequestPatch",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/patch"
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug pullrequests pull request  patch"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18e38bac-2832-4326-b7a5-90ef01e93abf"
            }
          ]
        }
      ]
    }
  ]
}