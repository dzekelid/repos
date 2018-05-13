{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Watchers",
    "_postman_id": "21c59415-4150-47c8-a4bb-459ed748dcbc",
    "description": "Returns a paginated list of all the watchers on the specified\nrepository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "d389a39c-623f-4f71-8c26-7edbb56f71cf",
          "name": "getRepositoriesUsernameRepoSlugWatchers",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/watchers"
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
            "description": "Returns a paginated list of all the watchers on the specified\nrepository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "50eb6472-8e92-4dc6-8c87-991bd4aeccb8"
            }
          ]
        }
      ]
    }
  ]
}