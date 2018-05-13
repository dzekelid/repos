{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Versions Version",
    "_postman_id": "38c202c4-0f95-43c5-bfde-8998f92040d8",
    "description": "Get repositories username repo slug versions version",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "db210186-d7a0-4d58-88ec-6af22c00d4b8",
          "name": "getRepositoriesUsernameRepoSlugVersionsVersion",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/versions/:version_id"
              ],
              "variable": [
                {
                  "id": "version_id",
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
            "description": "Get repositories username repo slug versions version"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0e28438b-4e2f-44f5-bfc0-6ebdcc495c20"
            }
          ]
        }
      ]
    }
  ]
}