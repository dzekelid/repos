{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Components",
    "_postman_id": "b4c9f4f3-63da-4898-8595-a332363d80cf",
    "description": "Returns the components that have been defined in the issue tracker.\n\nThis resource is only available on repositories that have the issue\ntracker enabled.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "93316f38-e29c-45a6-9b67-ebcdd18b398d",
          "name": "getRepositoriesUsernameRepoSlugComponents",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/components"
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
            "description": "Returns the components that have been defined in the issue tracker"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "40b7828c-add9-45aa-857b-c1cbbaccb5ea"
            }
          ]
        }
      ]
    }
  ]
}