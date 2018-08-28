{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Refs Tags",
    "_postman_id": "be82ae43-3d24-463b-aeca-57231b4703f6",
    "description": "Get repositories username repo slug refs tags",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "e08a338c-809b-4b2a-a6f3-4dfd58393c75",
          "name": "getRepositoriesUsernameRepoSlugRefsTags",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/refs/tags"
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
            "description": "Get repositories username repo slug refs tags"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "623ddf17-0a46-4aa8-a0eb-a918397d13cd"
            }
          ]
        }
      ]
    }
  ]
}