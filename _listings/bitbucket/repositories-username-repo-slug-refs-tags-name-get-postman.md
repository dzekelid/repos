{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Refs Tags Name",
    "_postman_id": "246d27c9-1f7e-4328-a1e8-ad4cb0d2851f",
    "description": "Get repositories username repo slug refs tags name",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "96efbb2b-e9a7-498f-a153-e023f65b4812",
          "name": "getRepositoriesUsernameRepoSlugRefsTagsName",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/refs/tags/:name"
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
            "description": "Get repositories username repo slug refs tags name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b97108d2-442e-4a4e-b5de-bffff8ea82b5"
            }
          ]
        }
      ]
    }
  ]
}