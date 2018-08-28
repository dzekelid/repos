{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Milestones",
    "_postman_id": "1412cfcc-f6d5-4d71-925e-390e44cb98d8",
    "description": "Returns the milestones that have been defined in the issue tracker.\n\nThis resource is only available on repositories that have the issue\ntracker enabled.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "ab199d36-89f8-4e60-a789-9fe949dbed67",
          "name": "getRepositoriesUsernameRepoSlugMilestones",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/milestones"
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
            "description": "Returns the milestones that have been defined in the issue tracker"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be32f058-7faa-406e-a635-b7df2fc213a1"
            }
          ]
        }
      ]
    }
  ]
}