---
swagger: "2.0"
x-collection-name: PayPal
x-complete: 0
info:
  title: Paypal Send Invoice
  description: Use the SendInvoice API operation to send an invoice to a payer, and
    notify the payer of the pending invoice.
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
  /Invoice/SearchInvoices:
    post:
      summary: Search Invoices
      description: Use the SearchInvoice API operation to search an invoice.
      operationId: Invoice.SearchInvoices.post
      x-api-path-slug: invoicesearchinvoices-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Invoices
      - Search
  /Invoice/MarkInvoiceAsPaid:
    post:
      summary: Mark Invoice As Paid
      description: Use the MarkInvoiceAsPaid API operation to mark an invoice as paid.
      operationId: Invoice.MarkInvoiceAsPaid.post
      x-api-path-slug: invoicemarkinvoiceaspaid-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Invoices
  /Invoice/Cancel Invoice:
    post:
      summary: Cancel Invoice
      description: Use the CancelInvoice API operation to cancel an invoice.
      operationId: Invoice.CancelInvoice.post
      x-api-path-slug: invoicecancel-invoice-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Invoices
  /Invoice/GetInvoiceDetails:
    post:
      summary: Get Invoice Details
      description: Use the GetInvoiceDetails API operation to get detailed information
        about an invoice.
      operationId: Invoice.GetInvoiceDetails.post
      x-api-path-slug: invoicegetinvoicedetails-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Invoices
  /Invoice/UpdateInvoice:
    post:
      summary: Update Invoice
      description: Use the UpdateInvoice API operation to update an invoice.
      operationId: Invoice.UpdateInvoice.post
      x-api-path-slug: invoiceupdateinvoice-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Invoices
  /Invoice/CreateAndSendInvoice:
    post:
      summary: Create And Send Invoice
      description: Use the CreateAndSendInvoice API operation to create and send an
        invoice.
      operationId: Invoice.CreateAndSendInvoice.post
      x-api-path-slug: invoicecreateandsendinvoice-post
      responses:
        200:
          description: OK
      tags:
      - Payments
      - Invoices
  /Invoice/SendInvoice:
    post:
      summary: Send Invoice
      description: Use the SendInvoice API operation to send an invoice to a payer,
        and notify the payer of the pending invoice.
      operationId: Invoice.SendInvoice.post
      x-api-path-slug: invoicesendinvoice-post
      responses:
        200:
          description: OK
      tags:
      - Payments
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