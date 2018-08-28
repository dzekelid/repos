{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue  Attachments Path",
    "_postman_id": "9fd3e970-674d-4470-962b-f33b8279e17d",
    "description": "Returns the contents of the specified file attachment.\n\nNote that this endpoint does not return a JSON response, but instead\nreturns a redirect pointing to the actual file that in turn will return\nthe raw contents.\n\nThe redirect URL contains a one-time token that has a limited lifetime.\nAs a result, the link should not be persisted, stored, or shared.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "90b2c581-9ede-47dd-ba95-7fafcf394b9b",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/attachments/:path"
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
                },
                {
                  "id": "path",
                  "value": "path",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the contents of the specified file attachment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "176a5df5-88ec-4556-b4d7-b4904f1f8bba"
            }
          ]
        }
      ]
    }
  ]
}