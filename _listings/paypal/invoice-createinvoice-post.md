---
swagger: "2.0"
info:
  title: Paypal Create Invoice
  description: Use the CreateInvoice API operation to create a new invoice. The call
    includes merchant, payer, and API caller information, in addition to invoice detail.
    The response to the call contains an invoice ID and URL.
  version: 1.0.0
host: svcs.sandbox.paypal.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Invoice/CreateInvoice:
    post:
      summary: Create Invoice
      description: Use the CreateInvoice API operation to create a new invoice
      operationId: Invoice.CreateInvoice.post
      responses:
        200:
          description: OK
      tags:
      - payments
      - invoices
definitions: []
x-collection-name: PayPal
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