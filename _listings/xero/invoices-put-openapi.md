---
swagger: "2.0"
x-collection-name: Xero
x-complete: 0
info:
  title: Clarity Accounting Put Invoices
  description: Put invoices.
  contact:
    name: Xero Developer Team
    url: https://developer.xero.com
  version: "2.0"
host: api.xero.com
basePath: /api.xro/2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Invoices:
    get:
      summary: Get Invoices
      description: Get invoices.
      operationId: getInvoices
      x-api-path-slug: invoices-get
      parameters:
      - in: query
        name: ContactIDs
        description: Filter by a comma-separated list of ContactIDs
      - in: query
        name: IDs
        description: Filter by a comma-separated list of InvoiceIDs
      - in: query
        name: InvoiceNumbers
        description: Filter by a comma-separated list of InvoiceNumbers
      - in: query
        name: No Name
      - in: query
        name: Statuses
        description: Filter by a comma-separated list of Statuses
      responses:
        200:
          description: OK
      tags:
      - Invoices
    post:
      summary: Post Invoices
      description: Post invoices.
      operationId: postInvoices
      x-api-path-slug: invoices-post
      parameters:
      - in: body
        name: Invoices
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoices
    put:
      summary: Put Invoices
      description: Put invoices.
      operationId: putInvoices
      x-api-path-slug: invoices-put
      parameters:
      - in: body
        name: Invoices
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoices
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