{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Refs Branches Name",
    "_postman_id": "36b2771b-7243-47d6-998a-5e879f943a23",
    "description": "Get repositories username repo slug refs branches name",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "24589f18-d8db-4171-89be-69e2d693f0b1",
          "name": "getRepositoriesUsernameRepoSlugRefsBranchesName",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/refs/branches/:name"
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
                  "id": "name",
                  "value": "name",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug refs branches name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0fb458ef-90b5-4cae-8d14-bdc93674afa8"
            }
          ]
        }
      ]
    }
  ]
}