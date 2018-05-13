{
  "info": {
    "name": "Bitbucket Get Repositories Username",
    "_postman_id": "f58bd034-9168-45b9-ab80-e7f4ed22b7e3",
    "description": "Returns a paginated list of all repositories owned by the specified\naccount or UUID.\n\nThe result can be narrowed down based on the authenticated user's role.\n\nE.g. with `?role=contributor`, only those repositories that the\nauthenticated user has write access to are returned (this includes any\nrepo the user is an admin on, as that implies write access).\n\nThis endpoint also supports filtering and sorting of the results. See\n[filtering and sorting](../../meta/filtering) for more details.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "8f6d55af-624a-4acf-9850-16424b656ab6",
          "name": "getRepositoriesUsername",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username"
              ],
              "query": [
                {
                  "key": "role",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
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
            "description": "Returns a paginated list of all repositories owned by the specified\naccount or UUID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "10880a1a-c2cd-4b6c-a20f-3ad077cddfb8"
            }
          ]
        }
      ]
    }
  ]
}