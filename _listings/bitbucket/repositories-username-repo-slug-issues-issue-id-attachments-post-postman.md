{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Issues Issue  Attachments",
    "_postman_id": "d9835887-e0a1-41ea-a268-8c7a7c88e9ab",
    "description": "Upload new issue attachments.\n\nTo upload files, perform a `multipart/form-data` POST containing one\nor more file fields.\n\nWhen a file is uploaded with the same name as an existing attachment,\nthen the existing file will be replaced.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "9c9eb6ea-7bb5-44f7-bacf-9a212ca9c27a",
          "name": "postRepositoriesUsernameRepoSlugIssuesIssueAttachments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/attachments"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Upload new issue attachments"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7da4a93b-3dd1-436c-b46a-82b6ea2cb206"
            }
          ]
        }
      ]
    }
  ]
}