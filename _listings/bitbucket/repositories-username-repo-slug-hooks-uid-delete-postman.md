{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Hooks U",
    "_postman_id": "9fcfa88e-359e-4181-9e49-d49aa1fc2d4a",
    "description": "Deletes the specified webhook subscription from the given\nrepository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "654f1d26-ec44-4bdc-ab2d-f98fb65ca6d2",
          "name": "deleteRepositoriesUsernameRepoSlugHooksU",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified webhook subscription from the given\nrepository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dc2b2522-6353-48fd-9984-92c488c4af56"
            }
          ]
        }
      ]
    }
  ]
}