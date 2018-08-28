{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Hooks",
    "_postman_id": "2e7894bb-be7a-4f34-bbec-c94180e0bade",
    "description": "Returns a paginated list of webhooks installed on this repository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "71aacaad-5da4-4437-8cf5-2215983d7495",
          "name": "getRepositoriesUsernameRepoSlugHooks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/hooks"
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
            "description": "Returns a paginated list of webhooks installed on this repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dfd707e9-bc4f-4211-afc6-f9e9429b8c74"
            }
          ]
        }
      ]
    }
  ]
}