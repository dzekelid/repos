{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Forks",
    "_postman_id": "cf023119-ddad-4bee-ac45-862ef13ff0ed",
    "description": "Returns a paginated list of all the forks of the specified\nrepository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "c063d35c-10e2-4bf8-b49b-855b8c9b44cd",
          "name": "getRepositoriesUsernameRepoSlugForks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/forks"
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
            "description": "Returns a paginated list of all the forks of the specified\nrepository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aa0787f2-611b-45d7-940c-f034a1562981"
            }
          ]
        }
      ]
    }
  ]
}