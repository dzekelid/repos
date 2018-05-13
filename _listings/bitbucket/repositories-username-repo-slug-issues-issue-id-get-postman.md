{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue",
    "_postman_id": "ea3620b0-2cdb-42f3-bc81-b561447c6ca8",
    "description": "Get repositories username repo slug issues issue",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "ff5740e0-d717-4401-b9aa-2e4f6b802455",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssue",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug issues issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0feaf1d-434a-4fd4-84fb-caab2c53c429"
            }
          ]
        }
      ]
    }
  ]
}