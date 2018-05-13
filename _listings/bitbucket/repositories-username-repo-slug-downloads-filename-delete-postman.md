{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Downloads Filename",
    "_postman_id": "f35e68c0-b0d2-4c53-ba64-9ccd9b99870c",
    "description": "Deletes the specified download artifact from the repository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "de892a0c-875c-40dd-8aac-6b6be25a3e5e",
          "name": "deleteRepositoriesUsernameRepoSlugDownloadsFilename",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/downloads/:filename"
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
                  "id": "filename",
                  "value": "filename",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified download artifact from the repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b398261-f537-4129-bdcd-c5cdbfcf37af"
            }
          ]
        }
      ]
    }
  ]
}