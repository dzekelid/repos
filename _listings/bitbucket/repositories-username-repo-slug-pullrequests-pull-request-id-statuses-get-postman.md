{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Statuses",
    "_postman_id": "e9a6efba-c647-446f-9dcd-00c7252dbbeb",
    "description": "Get repositories username repo slug pullrequests pull request  statuses",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "2bd7348a-38a3-491d-a755-4e310b585cce",
          "name": "getRepositoriesUsernameRepoSlugPullrequestsPullRequestStatuses",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/statuses"
              ],
              "variable": [
                {
                  "id": "pull_request_id",
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
            "description": "Get repositories username repo slug pullrequests pull request  statuses"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e4717486-a51e-4fa2-8730-3fa79b47ea09"
            }
          ]
        }
      ]
    }
  ]
}