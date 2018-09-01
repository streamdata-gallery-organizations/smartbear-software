{
  "info": {
    "name": "TestServer REST API Returns test run results stored on the TestServer.",
    "_postman_id": "a920064b-8863-4e7d-81d9-b5dd288603fd",
    "description": "Use this operation to get results of the latest test runs stored on the TestServer.<br/> The number of stored results is [configurable](http://readyapi.smartbear.com/testserver/reference/server_properties).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "executions",
      "item": [
        {
          "id": "7e49c00e-6340-4561-89fe-6e3b30837006",
          "name": "getExecutions",
          "request": {
            "url": "http://testserver.readyapi.io:8080/v1/readyapi/executions",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use this operation to get results of the latest test runs stored on the TestServer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5314c3f8-6bfe-4d57-afee-9fe258eccd90"
            }
          ]
        }
      ]
    }
  ]
}