{
  "info": {
    "name": "TestServer REST API Returns the status of the specified recipe execution.",
    "_postman_id": "21da6793-f659-47e4-8dbe-c7da7e41f157",
    "description": "Use this operation to get information on the recipe execution specified by <i>executionID</i>.  You can find in the response to your execution request ([see how](http://readyapi.smartbear.com/testserver/tutorials/your_first_recipe/results)), or you can send a GET <code>/readyapi/executions</code> request to the TestServer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "executions",
      "item": [
        {
          "id": "aefc9de3-d02a-4d16-a578-9df46258e2c3",
          "name": "getExecutionStatus",
          "request": {
            "url": {
              "protocol": "http",
              "host": "testserver.readyapi.io",
              "path": [
                "v1",
                "readyapi/executions/:executionID/status"
              ],
              "port": "8080",
              "variable": [
                {
                  "id": "executionID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Use this operation to get information on the recipe execution specified by <i>executionID</i>"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a046a256-d6c7-4ba3-b3be-94bec7f96f99"
            }
          ]
        }
      ]
    }
  ]
}