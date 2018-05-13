{
  "info": {
    "name": "Bitbucket Add Repositories Username Repo Slug Downloads",
    "_postman_id": "514f6293-80fe-4480-8326-0ee820fb908e",
    "description": "Upload new download artifacts.\n\nTo upload files, perform a `multipart/form-data` POST containing one\nor more `files` fields:\n\n    $ echo Hello World > hello.txt\n    $ curl -s -u evzijst -X POST https://api.bitbucket.org/2.0/repositories/evzijst/git-tests/downloads -F files=@hello.txt\n\nWhen a file is uploaded with the same name as an existing artifact,\nthen the existing file will be replaced.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "fa7d8289-9f3d-457b-889e-a926c4642dbb",
          "name": "postRepositoriesUsernameRepoSlugDownloads",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/downloads"
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
            "description": "Upload new download artifacts"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "55d19595-dc21-4b09-ae25-1debd1abe85c"
            }
          ]
        }
      ]
    }
  ]
}