{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Components Component",
    "_postman_id": "15b63892-a883-4209-9383-4697c9cc21ed",
    "description": "Get repositories username repo slug components component",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "89272583-3a7f-4f9b-991d-4004cfb238ae",
          "name": "getRepositoriesUsernameRepoSlugComponentsComponent",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/components/:component_id"
              ],
              "variable": [
                {
                  "id": "component_id",
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
            "description": "Get repositories username repo slug components component"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0e2602f4-37c8-4167-9e80-95648c868234"
            }
          ]
        }
      ]
    }
  ]
}