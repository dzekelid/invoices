---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Abandon an invoice
  description: Abandon an invoice with specified identifier string
  termsOfService: https://www.rebilly.com/terms/
  contact:
    name: Rebilly API Support
    url: https://www.rebilly.com/contact/
    email: integrations@rebilly.com
  version: "2.1"
host: api.rebilly.com
basePath: /v2.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /invoices:
    get:
      summary: Retrieve a list of invoices
      description: Retrieve a list of invoices
      operationId: invoices.get
      x-api-path-slug: invoices-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - List
      - Of
      - Invoices
    post:
      summary: Create an invoice
      description: Create an invoice
      operationId: invoices.post
      x-api-path-slug: invoices-post
      parameters:
      - in: body
        name: body
        description: Invoice resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /invoices/{id}/lead-source:
    get:
      summary: Retrieve an invoice's Lead Source
      description: Retrieve a Lead Source of given invoice
      operationId: invoices.id.lead_source.get
      x-api-path-slug: invoicesidleadsource-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Invoices
      - Lead
      - Source
    delete:
      summary: Delete a Lead Source for an invoice
      description: Delete a Lead Source that belongs to a certain invoice
      operationId: invoices.id.lead_source.delete
      x-api-path-slug: invoicesidleadsource-delete
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcean
      - Invoice
    put:
      summary: Create a Lead Source for an invoice
      description: Create a Lead Source for an invoice
      operationId: invoices.id.lead_source.put
      x-api-path-slug: invoicesidleadsource-put
      parameters:
      - in: body
        name: body
        description: Lead Source resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Lead
      - Sourcean
      - Invoice
  /invoices/{id}:
    get:
      summary: Retrieve an invoice
      description: Retrieve an invoice with specified identifier string
      operationId: invoices.id.get
      x-api-path-slug: invoicesid-get
      parameters:
      - in: header
        name: Accept
        description: The response media type
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Invoice
    put:
      summary: Create or update an invoice with predefined ID
      description: Create or update an invoice with predefined identifier string
      operationId: invoices.id.put
      x-api-path-slug: invoicesid-put
      parameters:
      - in: body
        name: body
        description: Invoice resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Invoice
      - Predefined
      - ID
  /invoices/{id}/abandon:
    post:
      summary: Abandon an invoice
      description: Abandon an invoice with specified identifier string
      operationId: invoices.id.abandon.post
      x-api-path-slug: invoicesidabandon-post
      responses:
        200:
          description: OK
      tags:
      - Abandon
      - Invoice
  /invoices/{id}/issue:
    post:
      summary: Issue an invoice
      description: Issue an invoice with specified identifier string
      operationId: invoices.id.issue.post
      x-api-path-slug: invoicesidissue-post
      parameters:
      - in: body
        name: body
        description: InvoiceIssue resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Invoice
  /invoices/{id}/items:
    get:
      summary: Retrieve invoice items
      description: Retrieve an invoice items with specified invoice identifier string
      operationId: invoices.id.items.get
      x-api-path-slug: invoicesiditems-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Invoice
      - Items
    post:
      summary: Create an invoice item
      description: Create an invoice item
      operationId: invoices.id.items.post
      x-api-path-slug: invoicesiditems-post
      parameters:
      - in: body
        name: body
        description: InvoiceItem resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - Item
  /invoices/{id}/matched-rules:
    get:
      summary: Get matched rules for the invoice
      description: Get matched rules for the invoice
      operationId: invoices.id.matched_rules.get
      x-api-path-slug: invoicesidmatchedrules-get
      responses:
        200:
          description: OK
      tags:
      - Matched
      - Rulesthe
      - Invoice
  /invoices/{id}/void:
    post:
      summary: Void an invoice
      description: Void an invoice with specified identifier string
      operationId: invoices.id.void.post
      x-api-path-slug: invoicesidvoid-post
      responses:
        200:
          description: OK
      tags:
      - Void
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