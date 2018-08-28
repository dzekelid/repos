{
  "info": {
    "name": "Bitbucket Get Users Username Repositories",
    "_postman_id": "1f0412de-f0e3-42b7-84d8-679484eb1c74",
    "description": "All repositories owned by a user/team. This includes private\nrepositories, but filtered down to the ones that the calling user has\naccess to.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "f1590975-65a6-42bf-8a37-683afbe865c6",
          "name": "getUsersUsernameRepositories",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "users/:username/repositories"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All repositories owned by a user/team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d3e5ec99-48bf-4227-b8e3-f437a2fa973d"
            }
          ]
        }
      ]
    }
  ]
}