{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Comments",
    "_postman_id": "39db1c68-e05c-4036-b6df-cf4d50b05205",
    "description": "Returns a paginated list of the pull request's comments.\n\nThis includes both global, inline comments and replies.\n\nThe default sorting is oldest to newest and can be overridden with\nthe `sort` query parameter.\n\nThis endpoint also supports filtering and sorting of the results. See\n[filtering and sorting](../../../../../../meta/filtering) for more\ndetails.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "7dbb52ad-f7a3-48f7-977b-982f35dc69be",
          "name": "getRepositoriesUsernameRepoSlugPullrequestsPullRequestComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests/:pull_request_id/comments"
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
            "description": "Returns a paginated list of the pull request's comments"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e067615f-2ad8-4451-94ef-401e04912d66"
            }
          ]
        }
      ]
    }
  ]
}