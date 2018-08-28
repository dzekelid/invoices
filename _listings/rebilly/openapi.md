swagger: "2.0"
x-collection-name: Rebilly
x-complete: 1
info:
  title: Rebilly
  description: -introductionthe-rebilly-api-is-built-on-http---our-api-is-restful---it-has-predictableresource-urls---it-returns-http-response-codes-to-indicate-errors---it-alsoaccepts-and-returns-json-in-the-http-body---you-can-use-your-favoritehttprest-library-for-your-programming-language-to-use-rebillys-api-oryou-can-use-one-of-our-sdks-currently-available-in-phphttpsgithub-comrebillyrebillyphpand-chttpsgithub-comrebillyrebillydotnetclient--authenticationwhen-you-sign-up-for-an-account-you-are-given-your-first-api-key-you-can-generate-additional-api-keys-and-delete-api-keys-as-you-mayneed-to-rotate-your-keys-in-the-future--you-authenticate-to-therebilly-api-by-providing-your-secret-key-in-the-request-header-rebilly-offers-three-forms-of-authentication--private-key-json-web-tokens-andpublic-key--private-key-authenticates-each-request-by-searching-for-the-presenceof-an-http-header-rebapikey--jwt-authenticates-each-request-by-the-http-header-authorization--public-key-authenticates-by-the-http-header-rebauth-read-more-on-this-below-rebilly-also-offers-json-web-tokens-jwt-authentication-where-you-can-controlthe-specific-granular-permissions-and-expiration-for-that-jwt---we-call-our-resourcefor-generating-jwt-sessionstagsessions-rebilly-also-has-a-clientside-authentication-scheme-that-uses-anapiuser-and-hmacsha1-signature-only-for-the-tokens-resource-sothat-you-may-safely-create-tokens-from-the-clientside-without-compromisingyour-secret-keys-never-share-your-secret-keys--keep-them-guarded-and-secure-the-clientside-authentication-scheme-uses-one-http-header-named-rebauth--redocinject-securitydefinitions--php-sdkfor-all-php-sdk-examples-provided-in-this-spec-you-will-need-to-configure-client-you-may-do-it-like-thisphpclient--new-rebillyclient----apikey--yourapikeyhere----baseurl--httpsapi-rebilly-com
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