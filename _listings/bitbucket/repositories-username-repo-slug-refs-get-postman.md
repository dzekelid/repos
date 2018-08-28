{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Refs",
    "_postman_id": "1e72b49a-f46e-4447-9f7b-10a463ab574c",
    "description": "Get repositories username repo slug refs",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "6b0fcf9f-e7fc-42a5-bb44-060342957e4c",
          "name": "getRepositoriesUsernameRepoSlugRefs",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/refs"
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
            "description": "Get repositories username repo slug refs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6847c62f-d1cf-4a5b-b5c5-6d606b9f1c77"
            }
          ]
        }
      ]
    }
  ]
}