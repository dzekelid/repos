{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Versions",
    "_postman_id": "1f67d25e-aca4-4b1b-8225-eefb8321b477",
    "description": "Returns the versions that have been defined in the issue tracker.\n\nThis resource is only available on repositories that have the issue\ntracker enabled.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "37bd8ab8-cdc7-445a-bf3b-02c4ff9b9792",
          "name": "getRepositoriesUsernameRepoSlugVersions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/versions"
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
            "description": "Returns the versions that have been defined in the issue tracker"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "00fa24d0-aed3-49d9-a60c-637e86bcf70b"
            }
          ]
        }
      ]
    }
  ]
}