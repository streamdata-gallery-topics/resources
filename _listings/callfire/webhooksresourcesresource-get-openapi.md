---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 0
info:
  title: Callfire Find specific webhook resource
  description: Returns information about supported events for a given webhook resource
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /webhooks/resources:
    get:
      summary: Find webhook resources
      description: 'Searches for webhook resources. Available resources include ''CccCampaign'':
        [''started'', ''stopped'', ''finished''], ''CallBroadcast'': [''started'',
        ''stopped'', ''finished''], ''TextBroadcast'': [''started'', ''stopped'',
        ''finished''], ''OutboundCall'': [''finished''], ''InboundCall'': [''finished''],
        ''OutboundText'': [''finished''], ''InboundText'': [''finished''], ''ContactList'':
        [''validationFinished'', ''validationFailed'']'
      operationId: findWebhookResources
      x-api-path-slug: webhooksresources-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      responses:
        200:
          description: OK
      tags:
      - Webhooks
      - Resources
  /webhooks/resources/{resource}:
    get:
      summary: Find specific webhook resource
      description: Returns information about supported events for a given webhook
        resource
      operationId: getWebhookResource
      x-api-path-slug: webhooksresourcesresource-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: resource
        description: A name of a webhook resource
      responses:
        200:
          description: OK
      tags:
      - Webhooks
      - Resources
      - Resource
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