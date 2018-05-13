{
  "info": {
    "name": "Cloud Source Repositories API Get Repos",
    "_postman_id": "5d647e77-7aa6-4da7-8312-fbdb9c472dc5",
    "description": "Returns all repos belonging to a project.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repository",
      "item": [
        {
          "id": "e9f047b5-275a-4329-a66d-2a398c992332",
          "name": "sourcerepo.projects.repos.list",
          "request": {
            "url": {
              "protocol": "http",
              "host": "sourcerepo.googleapis.com",
              "path": [
                "v1/:name/repos"
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
            "description": "Returns all repos belonging to a project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f798c00e-39af-45e0-8c56-079588067d55"
            }
          ]
        }
      ]
    }
  ]
}