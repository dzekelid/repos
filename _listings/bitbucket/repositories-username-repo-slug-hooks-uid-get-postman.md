{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Hooks U",
    "_postman_id": "9c83ccec-7d3c-4b68-b8b5-e81004ff50c7",
    "description": "Returns the webhook with the specified id installed on the specified\nrepository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "fc3d2de4-3c84-4751-ad8d-e50dddeedaee",
          "name": "getRepositoriesUsernameRepoSlugHooksU",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/hooks/:uid"
              ],
              "variable": [
                {
                  "id": "uid",
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
            "description": "Returns the webhook with the specified id installed on the specified\nrepository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4f009c1f-9920-4a87-850d-5b4388fdcfe1"
            }
          ]
        }
      ]
    }
  ]
}