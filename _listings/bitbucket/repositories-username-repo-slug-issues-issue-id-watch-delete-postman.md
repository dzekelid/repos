{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Issues Issue  Watch",
    "_postman_id": "62e1c8e8-e87b-4cb8-91c0-85e46d44ffcb",
    "description": "Delete repositories username repo slug issues issue  watch",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "3bf6dd98-be7a-4151-99d3-ee10ffcb7345",
          "name": "deleteRepositoriesUsernameRepoSlugIssuesIssueWatch",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/watch"
              ],
              "variable": [
                {
                  "id": "issue_id",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete repositories username repo slug issues issue  watch"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fad526ca-4663-44ee-866e-806f06886413"
            }
          ]
        }
      ]
    }
  ]
}