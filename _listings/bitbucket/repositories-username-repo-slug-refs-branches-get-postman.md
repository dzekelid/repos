{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Refs Branches",
    "_postman_id": "6cbb234c-05f6-41e0-8557-b567c3c3a5f5",
    "description": "Get repositories username repo slug refs branches",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "f55b156d-90b9-4c72-a16a-01fbd9365241",
          "name": "getRepositoriesUsernameRepoSlugRefsBranches",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/refs/branches"
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
            "description": "Get repositories username repo slug refs branches"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c71451a9-8c2f-4df0-bbb5-a4eb8f8a835b"
            }
          ]
        }
      ]
    }
  ]
}