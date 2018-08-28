{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Downloads",
    "_postman_id": "e7f8aaa3-e283-44ff-a0e9-f949ac72f7b0",
    "description": "Returns a list of download links associated with the repository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "39b0be8c-b8cc-48ff-8b89-573c04ab7ea8",
          "name": "getRepositoriesUsernameRepoSlugDownloads",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/downloads"
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
            "description": "Returns a list of download links associated with the repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "88f2a733-9da6-4409-a20b-040cd027966d"
            }
          ]
        }
      ]
    }
  ]
}