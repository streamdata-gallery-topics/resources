---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Access Control Creates/Updates a given resource for a given zone.
    The resourceIdentifier must be URL encoded in application/x-www-form-urlencoded
    format with UTF-8.
  description: Creates/updates a given resource for a given zone. the resourceidentifier
    must be url encoded in application/x-www-form-urlencoded format with utf-8..
  version: 1.0.0
host: predix-acs.run.aws-usw02-pr.ice.predix.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/resource:
    post:
      summary: Creates a list of resources for the given zone. Existing resources
        will be updated with the provided values.
      description: Creates a list of resources for the given zone. existing resources
        will be updated with the provided values..
      operationId: appendResourcesUsingPOST
      x-api-path-slug: v1resource-post
      parameters:
      - in: body
        name: resources
        description: resources
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Creates
      - List
      - Of
      - Resourcesthe
      - Given
      - Zone
      - ""
      - Existing
      - Resources
      - Will
      - Be
      - Updated
      - Provided
      - Values
    get:
      summary: Retrieves the list of all resources for the given zone.
      description: Retrieves the list of all resources for the given zone..
      operationId: getResourcesUsingGET
      x-api-path-slug: v1resource-get
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - List
      - Of
      - ""
      - Resourcesthe
      - Given
      - Zone
  /v1/connector/resource:
    get:
      summary: Retrieves connector configuration for external resource attributes
        for the given zone.
      description: Retrieves connector configuration for external resource attributes
        for the given zone..
      operationId: getResourceConnectorUsingGET_1
      x-api-path-slug: v1connectorresource-get
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Connector
      - Configurationexternal
      - Resource
      - Attributesthe
      - Given
      - Zone
    put:
      summary: Creates or updates connector configuration for external resource attributes
        for the given zone.
      description: Creates or updates connector configuration for external resource
        attributes for the given zone..
      operationId: putResourceConnectorUsingPUT_1
      x-api-path-slug: v1connectorresource-put
      parameters:
      - in: body
        name: connector
        description: New or updated connector configuration for external resource
          attributes
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Creates
      - Updates
      - Connector
      - Configurationexternal
      - Resource
      - Attributesthe
      - Given
      - Zone
    delete:
      summary: Deletes connector configuration for external resource attributes for
        the given zone.
      description: Deletes connector configuration for external resource attributes
        for the given zone..
      operationId: deleteResourceConnectorUsingDELETE
      x-api-path-slug: v1connectorresource-delete
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Connector
      - Configurationexternal
      - Resource
      - Attributesthe
      - Given
      - Zone
  /v1/resource/{resourceIdentifier}:
    put:
      summary: Creates/Updates a given resource for a given zone. The resourceIdentifier
        must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Creates/updates a given resource for a given zone. the resourceidentifier
        must be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: putResourceV1UsingPUT_1
      x-api-path-slug: v1resourceresourceidentifier-put
      parameters:
      - in: body
        name: resource
        description: resource
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceIdentifier
        description: resourceIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - Creates
      - S
      - Given
      - Resourcea
      - Given
      - Zone
      - ""
      - ResourceIdentifier
      - Must
      - Be
      - URL
      - Encoded
      - In
      - Application
      - X-www-form-urlencoded
      - Format
      - UTF-8
    delete:
      summary: Deletes the resource for a given zone. The resourceIdentifier must
        be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Deletes the resource for a given zone. the resourceidentifier must
        be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: deleteResourceV1UsingDELETE
      x-api-path-slug: v1resourceresourceidentifier-delete
      parameters:
      - in: path
        name: resourceIdentifier
        description: resourceIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Resourcea
      - Given
      - Zone
      - ""
      - ResourceIdentifier
      - Must
      - Be
      - URL
      - Encoded
      - In
      - Application
      - X-www-form-urlencoded
      - Format
      - UTF-8
    get:
      summary: Retrieves the resource for the given zone. The resourceIdentifier must
        be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Retrieves the resource for the given zone. the resourceidentifier
        must be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: getResourceV1UsingGET
      x-api-path-slug: v1resourceresourceidentifier-get
      parameters:
      - in: query
        name: includeInheritedAttributes
        description: includeInheritedAttributes
      - in: path
        name: resourceIdentifier
        description: resourceIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Resourcethe
      - Given
      - Zone
      - ""
      - ResourceIdentifier
      - Must
      - Be
      - URL
      - Encoded
      - In
      - Application
      - X-www-form-urlencoded
      - Format
      - UTF-8
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