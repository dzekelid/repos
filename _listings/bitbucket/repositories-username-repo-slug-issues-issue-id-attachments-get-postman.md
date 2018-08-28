{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue  Attachments",
    "_postman_id": "5a309d58-9009-4587-88a7-87cb18bb3b28",
    "description": "Returns all attachments for this issue.\n\nThis returns the files' meta data. This does not return the files'\nactual contents.\n\nThe files are always ordered by their upload date.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "983920ab-d3fd-4941-99d0-27bfda643984",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssueAttachments",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all attachments for this issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56f8d132-0c32-4aca-a6cc-b835620b8770"
            }
          ]
        }
      ]
    }
  ]
}