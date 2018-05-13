{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug",
    "_postman_id": "bd413c5f-08ca-432b-b109-355cc3ea93eb",
    "description": "Returns the object describing this repository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "b9da2fe1-600b-47c3-b2af-fda7a3692150",
          "name": "getRepositoriesUsernameRepoSlug",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug"
              ],
              "variable": [
                {
                  "id": "repo_slug",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "username",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the object describing this repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c50c961-71b6-4f5e-8451-d9523a2ee2e0"
            }
          ]
        }
      ]
    }
  ]
}