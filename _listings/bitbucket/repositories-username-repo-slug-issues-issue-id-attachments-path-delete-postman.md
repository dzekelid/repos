{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Issues Issue  Attachments Path",
    "_postman_id": "5848f154-3972-49df-afe5-862baa9ef2c8",
    "description": "Delete repositories username repo slug issues issue  attachments path",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "1301b71f-1fa7-4351-86b2-23f06f626f5a",
          "name": "deleteRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete repositories username repo slug issues issue  attachments path"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0afda4d-b0cd-455c-9e17-b731d9b0e462"
            }
          ]
        }
      ]
    }
  ]
}