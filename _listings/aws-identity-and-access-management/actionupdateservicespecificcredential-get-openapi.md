---
swagger: "2.0"
x-collection-name: AWS Identity and Access Management
x-complete: 0
info:
  title: AWS Identity and Access Management API Update Service Specific Credential
  version: 1.0.0
  description: |-
    Sets the status of a service-specific credential to Active or
            Inactive.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=UpdateAccessKey:
    get:
      summary: Update Access Key
      description: Changes the status of the specified access key from Active to Inactive,
        or vice versa.
      operationId: updateAccessKey
      x-api-path-slug: actionupdateaccesskey-get
      parameters:
      - in: query
        name: AccessKeyId
        description: The access key ID of the secret access key you want to update
        type: string
      - in: query
        name: Status
        description: The status you want to assign to the secret access key
        type: string
      - in: query
        name: UserName
        description: The name of the user whose key you want to update
        type: string
      responses:
        200:
          description: OK
      tags:
      - Access Keys
  /?Action=UpdateServiceSpecificCredential:
    get:
      summary: Update Service Specific Credential
      description: |-
        Sets the status of a service-specific credential to Active or
                Inactive.
      operationId: updateServiceSpecificCredential
      x-api-path-slug: actionupdateservicespecificcredential-get
      parameters:
      - in: query
        name: ServiceSpecificCredentialId
        description: The unique identifier of the service-specific credential
        type: string
      - in: query
        name: Status
        description: The status to be assigned to the service-specific credential
        type: string
      - in: query
        name: UserName
        description: The name of the IAM user associated with the service-specific
          credential
        type: string
      responses:
        200:
          description: OK
      tags:
      - Service Specific Credentials
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