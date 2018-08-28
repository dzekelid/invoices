---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Get summary of an account based on invoice amounts allocated
  version: 1.0.0
  description: Get summary of an account based on invoice amounts allocated.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/invoice/find:
    post:
      summary: Get filtered list of invoices
      description: Get filtered list of invoices.
      operationId: Invoice_GetInvoicesByfilterBypageSizeBypageNumber
      x-api-path-slug: apiinvoicefind-post
      parameters:
      - in: body
        name: filter
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Filtered
      - List
      - Of
      - Invoices
  /api/invoice/totals:
    post:
      summary: Get filtered list of invoices
      description: Get filtered list of invoices.
      operationId: Invoice_InvoiceTotalsByfilter
      x-api-path-slug: apiinvoicetotals-post
      parameters:
      - in: body
        name: filter
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Filtered
      - List
      - Of
      - Invoices
  /api/invoice/fees:
    get:
      summary: Get agent fees invoices earned
      description: Get agent fees invoices earned.
      operationId: Invoice_GetAgentFeesEarned
      x-api-path-slug: apiinvoicefees-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Agent
      - Fees
      - Invoices
      - Earned
  /api/account/{id}/invoiceoverview:
    post:
      summary: Get summary of an account based on invoice amounts allocated
      description: Get summary of an account based on invoice amounts allocated.
      operationId: Account_GetInvoiceOverviewByidBydataContract
      x-api-path-slug: apiaccountidinvoiceoverview-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Summary
      - Of
      - Account
      - Based
      - "On"
      - Invoice
      - Amounts
      - Ocated
  /api/invoice/{id}:
    get:
      summary: Get invoice by Id
      description: Get invoice by id.
      operationId: Invoice_GetByid
      x-api-path-slug: apiinvoiceid-get
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - By
      - Id
  /api/invoice/sales/create:
    post:
      summary: Create a new invoice
      description: Create a new invoice.
      operationId: Invoice_CreateSalesInvoiceBydataContract
      x-api-path-slug: apiinvoicesalescreate-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - New
      - Invoice
  /api/invoice/{id}/linkfees:
    post:
      summary: Add a fee to an existing invoice
      description: Add a fee to an existing invoice.
      operationId: Invoice_AddLinkedFeesByidByfees
      x-api-path-slug: apiinvoiceidlinkfees-post
      parameters:
      - in: body
        name: fees
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Fee
      - To
      - Existing
      - Invoice
  /api/invoice/{id}/removefee:
    put:
      summary: Remove fee from existing invoice
      description: Remove fee from existing invoice.
      operationId: Invoice_RemoveLinkedFeeByidByattachedFeeId
      x-api-path-slug: apiinvoiceidremovefee-put
      parameters:
      - in: query
        name: attachedFeeId
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Fee
      - From
      - Existing
      - Invoice
  /api/invoice/makeallocation:
    post:
      summary: Make an allocation against an existing invoice
      description: Make an allocation against an existing invoice.
      operationId: Invoice_MakeAllocationByallocationDataContract
      x-api-path-slug: apiinvoicemakeallocation-post
      parameters:
      - in: body
        name: allocationDataContract
        description: Details of Allocation
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Make
      - Ocation
      - Against
      - Existing
      - Invoice
  /api/invoice/raisecreditnote:
    post:
      summary: Raise a credit note against invoice items on an invoice
      description: Raise a credit note against invoice items on an invoice.
      operationId: Invoice_RaiseCreditNoteBycreditNoteDataContract
      x-api-path-slug: apiinvoiceraisecreditnote-post
      parameters:
      - in: body
        name: creditNoteDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Raise
      - Credit
      - Note
      - Against
      - Invoice
      - Items
      - "On"
      - Invoice
  /api/invoice/{id}/updatedetails:
    put:
      summary: Update properties on invoice
      description: Update properties on invoice.
      operationId: Invoice_UpdateInvoiceDetailsByidByupdateInvoiceDataContract
      x-api-path-slug: apiinvoiceidupdatedetails-put
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: updateInvoiceDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Properties
      - "On"
      - Invoice
  /api/invoice/raiseadjustment:
    post:
      summary: Raise an adjustment against an invoice
      description: Raise an adjustment against an invoice.
      operationId: Invoice_RaiseAdjustmentByadjustmentDataContract
      x-api-path-slug: apiinvoiceraiseadjustment-post
      parameters:
      - in: body
        name: adjustmentDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Raise
      - Adjustment
      - Against
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