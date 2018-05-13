{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Hooks",
    "_postman_id": "d4924aef-c3d9-424a-9f1c-64a86eba5955",
    "description": "Creates a new webhook on the specified repository.\n\nExample:\n\n```\n$ curl -X POST -u credentials -H 'Content-Type: application/json'           https://api.bitbucket.org/2.0/repositories/username/slug/hooks           -d '\n    {\n      \"description\": \"Webhook Description\",\n      \"url\": \"https://example.com/\",\n      \"active\": true,\n      \"events\": [\n        \"repo:push\",\n        \"issue:created\",\n        \"issue:updated\"\n      ]\n    }'\n```\n\nNote that this call requires the webhook scope, as well as any scope\nthat applies to the events that the webhook subscribes to. In the\nexample above that means: `webhook`, `repository` and `issue`.\n\nAlso note that the `url` must properly resolve and cannot be an\ninternal, non-routed address.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "716194e0-bb25-4d44-bf16-35a9dcf374a7",
          "name": "postRepositoriesUsernameRepoSlugHooks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/hooks"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new webhook on the specified repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f2c04184-3454-4cfa-97ab-4f3885a3b093"
            }
          ]
        }
      ]
    }
  ]
}