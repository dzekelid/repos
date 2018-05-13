{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues",
    "_postman_id": "1e789e3f-2f3a-4992-a987-66a14ba60806",
    "description": "Get repositories username repo slug issues",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "7cdbfea2-f660-44cc-941a-7ee48bfece13",
          "name": "getRepositoriesUsernameRepoSlugIssues",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug issues"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ecd1308a-8c92-438c-974b-6c1f3b97ed34"
            }
          ]
        }
      ]
    }
  ]
}