{
  "info": {
    "name": "Cloud Source Repositories API Get Repo",
    "_postman_id": "24fdb93f-38e8-4a50-88d0-cf0b164512d9",
    "description": "Returns information about a repo.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repository",
      "item": [
        {
          "id": "437c558d-3d12-4ea2-8506-c7b1408cc9bb",
          "name": "sourcerepo.projects.repos.get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "sourcerepo.googleapis.com",
              "path": [
                "v1/:name"
              ],
              "variable": [
                {
                  "id": "name",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns information about a repo"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "afce90f9-8a0c-4d2c-8a78-724c92c12429"
            }
          ]
        }
      ]
    }
  ]
}