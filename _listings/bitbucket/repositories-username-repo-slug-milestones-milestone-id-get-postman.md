{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Milestones Milestone",
    "_postman_id": "15ab4084-8e6e-4b22-8db9-bae1cff0441f",
    "description": "Get repositories username repo slug milestones milestone",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "7f41abbc-3162-4832-a292-6c6519e7afaf",
          "name": "getRepositoriesUsernameRepoSlugMilestonesMilestone",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/milestones/:milestone_id"
              ],
              "variable": [
                {
                  "id": "milestone_id",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug milestones milestone"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e90fbde3-9424-4bd3-a96c-00a0a345953f"
            }
          ]
        }
      ]
    }
  ]
}