{
  "info": {
    "name": "Bitbucket Delete Repositories Username Repo Slug Default Reviewers Target Username",
    "_postman_id": "82b022c7-371b-4acf-9729-a4dca6fa380e",
    "description": "Delete repositories username repo slug default reviewers target username",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "0e2cc511-87b9-4351-b590-6c6d9cb0dbb3",
          "name": "deleteRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/default-reviewers/:target_username"
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
                  "id": "target_username",
                  "value": "target_username",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete repositories username repo slug default reviewers target username"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d35c766a-03a2-4d05-a526-798df6fc99dd"
            }
          ]
        }
      ]
    }
  ]
}