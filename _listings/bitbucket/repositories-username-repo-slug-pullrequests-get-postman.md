{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Pullrequests",
    "_postman_id": "760d2afc-56a0-40db-9649-7f2572a57cf3",
    "description": "Returns a paginated list of all pull requests on the specified\nrepository. By default only open pull requests are returned. This can\nbe controlled using the `state` query parameter. To retrieve pull\nrequests that are in one of multiple states, repeat the `state`\nparameter for each individual state.\n\nThis endpoint also supports filtering and sorting of the results. See\n[filtering and sorting](../../../../meta/filtering) for more details.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "1df43e26-4189-4101-906e-85037838fc14",
          "name": "getRepositoriesUsernameRepoSlugPullrequests",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/pullrequests"
              ],
              "query": [
                {
                  "key": "state",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "Returns a paginated list of all pull requests on the specified\nrepository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bde05860-853d-40a0-93f6-f9caa5152093"
            }
          ]
        }
      ]
    }
  ]
}