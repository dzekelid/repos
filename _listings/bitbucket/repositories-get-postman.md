{
  "info": {
    "name": "Bitbucket Get Repositories",
    "_postman_id": "534e1269-3be1-458a-95b1-fc1d4a4b1db0",
    "description": "Returns a paginated list of all public repositories.\n\nThis endpoint also supports filtering and sorting of the results. See\n[filtering and sorting](../meta/filtering) for more details.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "9dcfcf3e-2139-4588-b654-453ff07838aa",
          "name": "getRepositories",
          "request": {
            "url": "http://api.bitbucket.org/2.0/repositories?after=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a paginated list of all public repositories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d3b59ca5-ef3d-482a-a5a8-78608fa80845"
            }
          ]
        }
      ]
    }
  ]
}