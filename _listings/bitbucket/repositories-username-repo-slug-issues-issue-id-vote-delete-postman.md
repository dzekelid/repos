{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Issues Issue  Vote",
    "_postman_id": "68f41642-ef07-4816-8dda-436bc1cb7490",
    "description": "Delete repositories username repo slug issues issue  vote",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "23a519f4-a25a-455a-8e53-49788459bf2f",
          "name": "deleteRepositoriesUsernameRepoSlugIssuesIssueVote",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/vote"
              ],
              "variable": [
                {
                  "id": "issue_id",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete repositories username repo slug issues issue  vote"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3120a155-a599-454a-8cfe-6a54abd0ef6d"
            }
          ]
        }
      ]
    }
  ]
}