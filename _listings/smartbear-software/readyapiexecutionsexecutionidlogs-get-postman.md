{
  "info": {
    "name": "TestServer REST API Returns the transaction logs for the specified recipe execution.",
    "_postman_id": "b1116cad-fedb-4180-a180-c08d4d25c9dd",
    "description": "Use this operation to get transaction logs (individual request and recponse of executed test steps) of the recipe execution specified by <i>executionID</i>.  You can find it in the response of your execution request ([see how](http://readyapi.smartbear.com/testserver/tutorials/your_first_recipe/results)), or you can send a GET <code>/readyapi/executions/{executionID}/logs</code> request to the TestServer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "executions",
      "item": [
        {
          "id": "0e68fede-406f-4382-b64d-8aadec01313a",
          "name": "getMessageExchanges",
          "request": {
            "url": {
              "protocol": "http",
              "host": "testserver.readyapi.io",
              "path": [
                "v1",
                "readyapi/executions/:executionID/logs"
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
            "description": "Use this operation to get transaction logs (individual request and recponse of executed test steps) of the recipe execution specified by <i>executionID</i>"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f528817-42ee-4ca4-b327-ccc6c5ee5763"
            }
          ]
        }
      ]
    }
  ]
}