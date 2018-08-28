{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Issues Issue",
    "_postman_id": "be982548-e3c7-45df-b96c-415b786b13aa",
    "description": "Deletes the specified issue. This requires write access to the\nrepository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "b92f0333-72bb-46ef-a49f-30251d2c3d2f",
          "name": "deleteRepositoriesUsernameRepoSlugIssuesIssue",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id"
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef7a008b-62e9-4f5d-b261-8234f170ff51"
            }
          ]
        }
      ]
    }
  ]
}