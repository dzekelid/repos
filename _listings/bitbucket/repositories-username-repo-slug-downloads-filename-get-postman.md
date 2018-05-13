{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Downloads Filename",
    "_postman_id": "f9a97e87-8d3c-4e68-8aea-d165988554c6",
    "description": "Return a redirect to the contents of a download artifact.\n\nThis endpoint returns the actual file contents and not the artifact's\nmetadata.\n\n    $ curl -s -L https://api.bitbucket.org/2.0/repositories/evzijst/git-tests/downloads/hello.txt\n    Hello World",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "8dc5cbf5-edca-40bb-af65-060cd2c9e8a8",
          "name": "getRepositoriesUsernameRepoSlugDownloadsFilename",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/downloads/:filename"
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
                  "id": "filename",
                  "value": "filename",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a redirect to the contents of a download artifact"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "884fefba-5d5d-482c-a29a-1a6d1b1c1aae"
            }
          ]
        }
      ]
    }
  ]
}