{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug",
    "_postman_id": "f5c98a3f-8956-47fc-af7d-48db6129c645",
    "description": "Deletes the repository. This is an irreversible operation.\n\nThis does not affect its forks.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "e974ef84-0f4e-43f0-8940-095629271232",
          "name": "deleteRepositoriesUsernameRepoSlug",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug"
              ],
              "variable": [
                {
                  "id": "repo_slug",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "username",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d94f316f-c871-4a12-8afc-1ea00f48e450"
            }
          ]
        }
      ]
    }
  ]
}