---
swagger: "2.0"
x-collection-name: SmartBear Software
x-complete: 0
info:
  title: TestServer REST API Cancels the specified recipe execution
  description: Use this operation to stop the run specified by <i>executionID</i>.
    You can find in the response to your execution request ([see how](http://readyapi.smartbear.com/testserver/tutorials/your_first_recipe/results)),
    or you can send a GET <code>/readyapi/executions</code> request to the TestServer.
  contact:
    name: SmartBear Software
    url: http://smartbear.com/testserver
  version: 1.2.1
host: testserver.readyapi.io:8080
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /readyapi/executions:
    get:
      summary: Returns test run results stored on the TestServer.
      description: Use this operation to get results of the latest test runs stored
        on the TestServer.<br/> The number of stored results is [configurable](http://readyapi.smartbear.com/testserver/reference/server_properties).
      operationId: getExecutions
      x-api-path-slug: readyapiexecutions-get
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Executions
    post:
      summary: Runs a test recipe.
      description: Use this operation to send a test recipe to the TestServer. The
        recipe contents is passed in the request body (should be valid JSON contents).
      operationId: postRecipe
      x-api-path-slug: readyapiexecutions-post
      parameters:
      - in: query
        name: async
        description: Specifies when the TestServer replies:`true` - Immediately
      - in: body
        name: body
        description: JSON-based test recipe contents
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: callback
        description: The URL, to which the results will be posted
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Executions
  /readyapi/executions/xml:
    post:
      summary: Executes a Ready! API project.
      description: Use this operation to send a Ready! API test project to the TestServer.
        You command the TestServer to execute the entire project, or an individual
        test suite or test case in it. The recipe request should have a Ready! API
        project file (.xml) attached to it.
      operationId: postProjectExecution
      x-api-path-slug: readyapiexecutionsxml-post
      parameters:
      - in: query
        name: async
        description: Specifies when TestServer replies:`true` - Immediately
      - in: body
        name: body
        description: Ready! API XML project
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: callback
        description: The URL, to which the results will be posted
      - in: query
        name: clientCertFileName
        description: The name of the separately provided client certificate file
      - in: query
        name: clientCertPassword
        description: The password for the separately provided client certificate file
      - in: query
        name: environment
        description: The target environment for tests execution
      - in: query
        name: testCaseName
        description: The name of the test case to run
      - in: query
        name: testSuiteName
        description: The name of the test suite to run
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Executions
  /readyapi/executions/composite:
    post:
      summary: Executes a zipped Ready! API composite project.
      description: Use this operation to send a zipped Ready! API composite project
        to the TestServer. You command the TestServer to execute the entire project,
        or an individual test suite or test case in it. The recipe request should
        have a Ready! API project file (.xml) attached to it.
      operationId: postCompositeProjectExecution
      x-api-path-slug: readyapiexecutionscomposite-post
      parameters:
      - in: query
        name: async
        description: Specifies when TestServer replies:`true` - Immediately
      - in: body
        name: body
        description: Ready! API XML project
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: callback
        description: The URL, to which the results will be posted
      - in: query
        name: clientCertFileName
        description: The name of the separately provided client certificate file
      - in: query
        name: clientCertPassword
        description: The password for the separately provided client certificate file
      - in: query
        name: environment
        description: The target environment for tests execution
      - in: query
        name: testCaseName
        description: The name of the test case to run
      - in: query
        name: testSuiteName
        description: The name of the test suite to run
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Executions
  /readyapi/executions/{executionID}:
    delete:
      summary: Cancels the specified recipe execution
      description: Use this operation to stop the run specified by <i>executionID</i>.
        You can find in the response to your execution request ([see how](http://readyapi.smartbear.com/testserver/tutorials/your_first_recipe/results)),
        or you can send a GET <code>/readyapi/executions</code> request to the TestServer.
      operationId: cancelExecution
      x-api-path-slug: readyapiexecutionsexecutionid-delete
      parameters:
      - in: path
        name: executionID
        description: The id of the test run to stop
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Executions
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---