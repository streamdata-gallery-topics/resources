---
swagger: "2.0"
x-collection-name: Azure Resource Manager
x-complete: 0
info:
  title: Azure Resource Manager API Resources Check Existence
  description: Checks whether a resource exists.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/resourceGroups/{sourceResourceGroupName}/moveResources:
    post:
      summary: Moves resources from one resource group to another resource group.
      description: The resources to move must be in the same source resource group.
        The target resource group may be in a different subscription. When moving
        resources, both the source group and the target group are locked for the duration
        of the operation. Write and delete operations are blocked on the groups until
        the move completes.
      operationId: Resources_MoveResources
      x-api-path-slug: subscriptionssubscriptionidresourcegroupssourceresourcegroupnamemoveresources-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters for moving resources
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: sourceResourceGroupName
        description: The name of the resource group containing the rsources to move
      responses:
        200:
          description: OK
      tags:
      - Resources
  /subscriptions/{subscriptionId}/resources:
    get:
      summary: Resources List
      description: Get all the resources in a subscription.
      operationId: Resources_List
      x-api-path-slug: subscriptionssubscriptionidresources-get
      parameters:
      - in: query
        name: $expand
        description: The $expand query parameter
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: query
        name: $top
        description: The number of results to return
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Resources
  ? /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{parentResourcePath}/{resourceType}/{resourceName}
  : head:
      summary: Resources Check Existence
      description: Checks whether a resource exists.
      operationId: Resources_CheckExistence
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersresourceprovidernamespaceparentresourcepathresourcetyperesourcename-head
      parameters:
      - in: query
        name: api-version
        description: The API version to use for the operation
      - in: query
        name: No Name
      - in: path
        name: parentResourcePath
        description: The parent resource identity
      - in: path
        name: resourceGroupName
        description: The name of the resource group containing the resource to check
      - in: path
        name: resourceName
        description: The name of the resource to check whether it exists
      - in: path
        name: resourceProviderNamespace
        description: The resource provider of the resource to check
      - in: path
        name: resourceType
        description: The resource type
      responses:
        200:
          description: OK
      tags:
      - Resources
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