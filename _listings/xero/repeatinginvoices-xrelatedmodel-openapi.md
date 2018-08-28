---
swagger: "2.0"
x-collection-name: Xero
x-complete: 0
info:
  title: Clarity Accounting X-related-model Repeatinginvoices
  description: X-related-model repeatinginvoices.
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
    x-related-model:
      summary: X-related-model Invoices
      description: X-related-model invoices.
      operationId: x-related-modelInvoices
      x-api-path-slug: invoices-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - Invoices
  /Invoices/{InvoiceID}:
    get:
      summary: Get Invoices Invoice
      description: Get invoices invoice.
      operationId: getInvoicesInvoice
      x-api-path-slug: invoicesinvoiceid-get
      parameters:
      - in: path
        name: InvoiceID
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
    post:
      summary: Post Invoices Invoice
      description: Post invoices invoice.
      operationId: postInvoicesInvoice
      x-api-path-slug: invoicesinvoiceid-post
      parameters:
      - in: path
        name: InvoiceID
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
      - InvoiceID
    x-related-model:
      summary: X-related-model Invoices Invoice
      description: X-related-model invoices invoice.
      operationId: x-related-modelInvoicesInvoice
      x-api-path-slug: invoicesinvoiceid-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
  /Invoices/{InvoiceID}/Attachments:
    get:
      summary: Get Invoices Invoice Attachments
      description: Get invoices invoice attachments.
      operationId: getInvoicesInvoiceAttachments
      x-api-path-slug: invoicesinvoiceidattachments-get
      parameters:
      - in: path
        name: InvoiceID
        description: The Xero generated unique identifier for an Invoice
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
      - Attachments
  /Invoices/{InvoiceID}/Attachments/{FileName}:
    get:
      summary: Get Invoices Invoice Attachments Filename
      description: Get invoices invoice attachments filename.
      operationId: getInvoicesInvoiceAttachmentsFilename
      x-api-path-slug: invoicesinvoiceidattachmentsfilename-get
      parameters:
      - in: path
        name: FileName
        description: The filename of the attachment to be downloaded
      - in: path
        name: InvoiceID
        description: The Xero generated unique identifier for an Invoice
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
      - Attachments
      - FileName
    post:
      summary: Post Invoices Invoice Attachments Filename
      description: Post invoices invoice attachments filename.
      operationId: postInvoicesInvoiceAttachmentsFilename
      x-api-path-slug: invoicesinvoiceidattachmentsfilename-post
      parameters:
      - in: body
        name: Content
        description: The raw content of the file to be uploaded
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: FileName
        description: The filename of the attachment being uploaded
      - in: path
        name: InvoiceID
        description: The Xero generated unique identifier for an Invoice
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
      - Attachments
      - FileName
  /Invoices/{InvoiceID}/OnlineInvoice:
    get:
      summary: Get Invoices Invoice Onlineinvoice
      description: Get invoices invoice onlineinvoice.
      operationId: getInvoicesInvoiceOnlineinvoice
      x-api-path-slug: invoicesinvoiceidonlineinvoice-get
      parameters:
      - in: path
        name: InvoiceID
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
      - OnlineInvoice
    x-related-model:
      summary: X-related-model Invoices Invoice Onlineinvoice
      description: X-related-model invoices invoice onlineinvoice.
      operationId: x-related-modelInvoicesInvoiceOnlineinvoice
      x-api-path-slug: invoicesinvoiceidonlineinvoice-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - Invoices
      - InvoiceID
      - OnlineInvoice
  /RepeatingInvoices/{RepeatingInvoiceID}:
    get:
      summary: Get Repeatinginvoices Repeatinginvoice
      description: Get repeatinginvoices repeatinginvoice.
      operationId: getRepeatinginvoicesRepeatinginvoice
      x-api-path-slug: repeatinginvoicesrepeatinginvoiceid-get
      parameters:
      - in: path
        name: RepeatingInvoiceID
      responses:
        200:
          description: OK
      tags:
      - RepeatingInvoices
      - RepeatingInvoiceID
    x-related-model:
      summary: X-related-model Repeatinginvoices Repeatinginvoice
      description: X-related-model repeatinginvoices repeatinginvoice.
      operationId: x-related-modelRepeatinginvoicesRepeatinginvoice
      x-api-path-slug: repeatinginvoicesrepeatinginvoiceid-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - RepeatingInvoices
      - RepeatingInvoiceID
  /RepeatingInvoices/{RepeatingInvoiceID}/Attachments:
    get:
      summary: Get Repeatinginvoices Repeatinginvoice Attachments
      description: Get repeatinginvoices repeatinginvoice attachments.
      operationId: getRepeatinginvoicesRepeatinginvoiceAttachments
      x-api-path-slug: repeatinginvoicesrepeatinginvoiceidattachments-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: RepeatingInvoiceID
        description: The Xero generated unique identifier for a RepeatingInvoice
      responses:
        200:
          description: OK
      tags:
      - RepeatingInvoices
      - RepeatingInvoiceID
      - Attachments
  /RepeatingInvoices/{RepeatingInvoiceID}/Attachments/{FileName}:
    get:
      summary: Get Repeatinginvoices Repeatinginvoice Attachments Filename
      description: Get repeatinginvoices repeatinginvoice attachments filename.
      operationId: getRepeatinginvoicesRepeatinginvoiceAttachmentsFilename
      x-api-path-slug: repeatinginvoicesrepeatinginvoiceidattachmentsfilename-get
      parameters:
      - in: path
        name: FileName
        description: The filename of the attachment to be downloaded
      - in: query
        name: No Name
      - in: path
        name: RepeatingInvoiceID
        description: The Xero generated unique identifier for a RepeatingInvoice
      responses:
        200:
          description: OK
      tags:
      - RepeatingInvoices
      - RepeatingInvoiceID
      - Attachments
      - FileName
  /RepeatingInvoices:
    get:
      summary: Get Repeatinginvoices
      description: Get repeatinginvoices.
      operationId: getRepeatinginvoices
      x-api-path-slug: repeatinginvoices-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - RepeatingInvoices
    x-related-model:
      summary: X-related-model Repeatinginvoices
      description: X-related-model repeatinginvoices.
      operationId: x-related-modelRepeatinginvoices
      x-api-path-slug: repeatinginvoices-xrelatedmodel
      responses:
        200:
          description: OK
      tags:
      - RepeatingInvoices
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