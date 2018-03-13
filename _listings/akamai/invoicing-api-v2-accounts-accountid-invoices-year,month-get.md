---
swagger: "2.0"
info:
  title: Akamai Merged API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /invoicing-api/v2/accounts/{accountId}/invoices{?year,month}:
    get:
      summary: List Account&#8217;s Invoices
      description: List Account&#8217;s Invoices
      operationId: invoicingapiv2accountsaccountidinvoicesyearmonth
      parameters:
      - in: String
        name: accountId
        description: Identifies the account under which data is aggregated
        type: string
      - in: Integer
        name: month
        description: The month for which data is aggregated
        type: string
      - in: Integer
        name: year
        description: The year for which data is aggregated
        type: string
      responses:
        200:
          description: OK
      tags:
      - invoicing
      - accounts
      - account
      - invoices
      - year
      - month
definitions: []
x-collection-name: Akamai
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