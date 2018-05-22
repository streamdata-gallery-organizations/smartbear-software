{
  "info": {
    "name": "TestServer REST API Cancels the specified recipe execution",
    "_postman_id": "081e10ea-1bfc-4878-a8d9-fa7e950b0fdc",
    "description": "Use this operation to stop the run specified by <i>executionID</i>. You can find in the response to your execution request ([see how](http://readyapi.smartbear.com/testserver/tutorials/your_first_recipe/results)), or you can send a GET <code>/readyapi/executions</code> request to the TestServer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "executions",
      "item": [
        {
          "id": "b7c87abb-83be-4aae-b95d-69780e4fad9e",
          "name": "cancelExecution",
          "request": {
            "url": {
              "protocol": "http",
              "host": "testserver.readyapi.io",
              "path": [
                "v1",
                "readyapi/executions/:executionID"
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Use this operation to stop the run specified by <i>executionID</i>"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d70c3b52-56c2-4ea2-920b-13a41f5fde81"
            }
          ]
        }
      ]
    }
  ]
}