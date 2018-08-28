{
  "info": {
    "name": "Bitbucket Update Repositories Username Repo Slug Issues Issue  Vote",
    "_postman_id": "0e06abe1-fee4-4e6a-9e93-d538aeb772b8",
    "description": "Vote for this issue.\n\nTo cast your vote, do an empty PUT. The 204 status code indicates that\nthe operation was successful.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "e4bf0149-6a49-451a-82ec-10db6d83479f",
          "name": "putRepositoriesUsernameRepoSlugIssuesIssueVote",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Vote for this issue"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "972a6625-3722-449c-966c-e28f3bf5bf85"
            }
          ]
        }
      ]
    }
  ]
}