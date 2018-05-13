{
  "info": {
    "name": "Cloud Source Repositories API Delete Repo",
    "_postman_id": "6e79c4f7-f903-4db1-92e7-284b48c8c157",
    "description": "Deletes a repo.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repository",
      "item": [
        {
          "id": "fab8f65e-318b-44ec-9bf2-88c3e53c926d",
          "name": "sourcerepo.projects.repos.delete",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a repo"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "116ecabc-a9e0-4c2e-98ee-a5bf070dbbcf"
            }
          ]
        }
      ]
    }
  ]
}