{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Issues Issue  Comments Comment",
    "_postman_id": "559fa62d-1a1f-44e7-83e0-5ddf938fc8bf",
    "description": "Get repositories username repo slug issues issue  comments comment",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "0fc3a440-52f9-4c9e-8b66-288e77d7c9f6",
          "name": "getRepositoriesUsernameRepoSlugIssuesIssueCommentsComment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/issues/:issue_id/comments/:comment_id"
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
                  "id": "issue_id",
                  "value": "issue_id",
                  "type": "string"
                },
                {
                  "id": "comment_id",
                  "value": "comment_id",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get repositories username repo slug issues issue  comments comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4671ceb9-53ce-4b78-b10f-8d0869495881"
            }
          ]
        }
      ]
    }
  ]
}