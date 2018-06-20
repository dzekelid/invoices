---
swagger: "2.0"
x-collection-name: PayPal
x-complete: 0
info:
  title: Paypal Cancel Invoice
  description: Use the CancelInvoice API operation to cancel an invoice.
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
        1:
          description: Photoset not found - The photoset id passed was not the id
            of avalid photoset owned by the calling user
        2:
          description: Photo not found - The photo id passed was not the id of a valid
            photo owned by the calling user
        95:
          description: SSL is required - SSL is required to access the Flickr API
        96:
          description: Invalid signature - The passed signature was invalid
        97:
          description: Missing signature - The call required signing but no signature
            was sent
        98:
          description: Login failed / Invalid auth token - The login details or auth
            token passed were invalid
        99:
          description: User not logged in / Insufficient permissions - The method
            requires user authentication but the user was not logged in, or the authenticated
            method call did not have the required permissions
        100:
          description: Invalid API Key - The API key passed was not valid or has expired
        105:
          description: Service currently unavailable - The requested service is temporarily
            unavailable
        106:
          description: Write operation failed - The requested operation failed due
            to a temporary issue
        111:
          description: Format "xxx" not found - The requested response format was
            not found
        112:
          description: Method "xxx" not found - The requested method was not found
        114:
          description: Invalid SOAP envelope - The SOAP envelope send in the request
            could not be parsed
        115:
          description: Invalid XML-RPC Method Call - The XML-RPC request document
            could not be parsed
        116:
          description: Bad URL found - One or more arguments contained a URL that
            has been used for abuse on Flickr
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