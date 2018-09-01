---
swagger: "2.0"
x-collection-name: SmartBear Software
x-complete: 0
info:
  title: TestServer REST API Returns test run results stored on the TestServer.
  description: Use this operation to get results of the latest test runs stored on
    the TestServer.<br/> The number of stored results is [configurable](http://readyapi.smartbear.com/testserver/reference/server_properties).
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