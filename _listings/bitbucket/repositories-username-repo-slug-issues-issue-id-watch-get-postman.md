{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue  Watch",
    "_postman_id": "d2a41029-d634-4087-bb92-120a0bf2391e",
    "description": "Indicated whether or not the authenticated user is watching this\nissue.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "ba86cde5-f99f-406a-ab2e-fa4abbf72fe1",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssueWatch",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Indicated whether or not the authenticated user is watching this\nissue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb42b55e-2352-4bf7-aa49-a4a48ec728e9"
            }
          ]
        }
      ]
    }
  ]
}