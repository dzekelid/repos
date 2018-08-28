{
  "info": {
    "name": "Bitbucket Update Repositories Username Repo Slug Issues Issue  Watch",
    "_postman_id": "6ae5900d-0660-4699-ae33-9f570dfa3c8a",
    "description": "Start watching this issue.\n\nTo start watching this issue, do an empty PUT. The 204 status code\nindicates that the operation was successful.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "d623f09e-3720-41ef-b702-862e599e4e4c",
          "name": "putRepositoriesUsernameRepoSlugIssuesIssueWatch",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Start watching this issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aef5a861-4178-4b72-9dda-24f717cc93a9"
            }
          ]
        }
      ]
    }
  ]
}