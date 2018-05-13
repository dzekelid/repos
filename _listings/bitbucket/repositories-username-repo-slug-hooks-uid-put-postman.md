{
  "info": {
    "name": "Bitbucket Update Repositories Username Repo Slug Hooks U",
    "_postman_id": "2eb3a509-db17-4c73-a5b0-0daa54e05879",
    "description": "Updates the specified webhook subscription.\n\nThe following properties can be mutated:\n\n* `description`\n* `url`\n* `active`\n* `events`",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "12570aee-5f9a-4c18-b37b-f682ae2f916a",
          "name": "putRepositoriesUsernameRepoSlugHooksU",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Updates the specified webhook subscription"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22699a96-4030-46d0-88b3-16834e4954ec"
            }
          ]
        }
      ]
    }
  ]
}