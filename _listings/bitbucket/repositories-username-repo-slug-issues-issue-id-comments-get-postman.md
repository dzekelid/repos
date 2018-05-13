{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue  Comments",
    "_postman_id": "d2679ee8-c921-4383-beca-9ea31a864d76",
    "description": "Returns all comments that were made on the specified issue.\n\nThe default sorting is oldest to newest and can be overridden with\nthe `sort` query parameter.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "11344646-1389-4080-be9d-e4639edba6a5",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssueComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/comments"
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
                  "id": "issue_id",
                  "value": "issue_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all comments that were made on the specified issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "21ee500a-ab11-40d7-a3b1-e7ea4fe548cb"
            }
          ]
        }
      ]
    }
  ]
}