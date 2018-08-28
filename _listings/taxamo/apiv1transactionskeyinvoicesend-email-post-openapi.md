---
swagger: "2.0"
x-collection-name: Taxamo
x-complete: 0
info:
  title: Taxamo Email Invoice
  description: Email invoice.
  version: "1"
host: api.taxamo.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/transactions/{key}/invoice/send_email:
    post:
      summary: Email Invoice
      description: Email invoice.
      operationId: emailInvoice
      x-api-path-slug: apiv1transactionskeyinvoicesend-email-post
      parameters:
      - in: body
        name: input
        description: Input
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: key
        description: Transaction key
      responses:
        200:
          description: OK
      tags:
      - Email
      - Invoice
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