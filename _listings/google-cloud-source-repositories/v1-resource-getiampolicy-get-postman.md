{
  "info": {
    "name": "Cloud Source Repositories API Get Access Control Policy",
    "_postman_id": "01c52f44-cdba-442b-86d6-63f036dea334",
    "description": "Gets the access control policy for a resource.\nReturns an empty policy if the resource exists and does not have a policy\nset.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repository policy",
      "item": [
        {
          "id": "f08c90ab-8483-4ef1-8ae6-3ca8b10b5ffb",
          "name": "sourcerepo.projects.repos.getIamPolicy",
          "request": {
            "url": {
              "protocol": "http",
              "host": "sourcerepo.googleapis.com",
              "path": [
                "v1/:resource:getIamPolicy"
              ],
              "variable": [
                {
                  "id": "resource",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the access control policy for a resource"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a669d287-87ba-4a66-b155-ef7ab4631de6"
            }
          ]
        }
      ]
    }
  ]
}