---
swagger: "2.0"
x-collection-name: Stripe
x-complete: 0
info:
  title: Stripe Add Invoices Invoice Pay
  description: Stripe automatically creates and then attempts to collect payment on
    invoices for customers on subscriptions according to your subscriptions settings.
    However, if you???d like to attempt payment on an invoice out of the normal collection
    schedule or for some other reason, you can do so.
  termsOfService: https://stripe.com/us/terms/
  contact:
    name: Stripe Dev Platform Team
    url: https://stripe.com
    email: dev-platform@stripe.com
  version: v1
host: api.stripe.com
basePath: v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /invoices:
    get:
      summary: Get Invoices
      description: You can list all invoices, or list the invoices for a specific
        customer. The invoices are returned sorted by creation date, with the most
        recently created invoices appearing first.
      operationId: getInvoices
      x-api-path-slug: invoices-get
      parameters:
      - in: query
        name: billing
        description: The billing mode of the invoice to retrieve
      - in: query
        name: customer
        description: Only return invoices for the customer specified by this customer
          ID
      - in: query
        name: date
      - in: query
        name: due_date
      - in: query
        name: ending_before
        description: A cursor for use in pagination
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: query
        name: limit
        description: A limit on the number of objects to be returned
      - in: query
        name: starting_after
        description: A cursor for use in pagination
      - in: query
        name: subscription
        description: Only return invoices for the subscription specified by this subscription
          ID
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
      tags:
      - Invoices
    post:
      summary: Add Invoices
      description: If you need to invoice your customer outside the regular billing
        cycle, you can create an invoice that pulls in all pending invoice items,
        including prorations. The customer???s billing cycle and regular subscription
        won???t be affected.Once you create the invoice, Stripe will attempt to collect
        payment according to your subscriptions settings, though you can choose to
        pay it right away.
      operationId: postInvoices
      x-api-path-slug: invoices-post
      parameters:
      - in: body
        name: payload
        description: Body parameters for the request
        schema:
          $ref: '#/definitions/holder'
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
      tags:
      - Invoices
  /invoices/upcoming:
    get:
      summary: Get Invoices Upcoming
      description: At any time, you can preview the upcoming invoice for a customer.
        This will show you all the charges that are pending, including subscription
        renewal charges, invoice item charges, etc. It will also show you any discount
        that is applicable to the customer.Note that when you are viewing an upcoming
        invoice, you are simply viewing a preview ??? the invoice has not yet been
        created. As such, the upcoming invoice will not show up in invoice listing
        calls, and you cannot use the API to pay or edit the invoice. If you want
        to change the amount that your customer will be billed, you can add, remove,
        or update pending invoice items, or update the customer???s discount.You can
        preview the effects of updating a subscription, including a preview of what
        proration will take place. To ensure that the actual proration is calculated
        exactly the same as the previewed proration, you should pass a proration_date
        parameter when doing the actual subscription update. The value passed in should
        be the same as the subscription_proration_date returned on the upcoming invoice
        resource. The recommended way to get only the prorations being previewed is
        to consider only proration line items where period[start] is equal to the
        subscription_proration_date on the upcoming invoice resource.
      operationId: getInvoicesUpcoming
      x-api-path-slug: invoicesupcoming-get
      parameters:
      - in: query
        name: coupon
        description: The code of the coupon to apply
      - in: query
        name: customer
        description: The identifier of the customer whose upcoming invoice youd like
          to retrieve
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: query
        name: invoice_items
        description: List of invoice items to add or update in the upcoming invoice
          preview
      - in: query
        name: subscription
        description: The identifier of the subscription for which youd like to retrieve
          the upcoming invoice
      - in: query
        name: subscription_items
        description: List of subscription items, each with an attached plan
      - in: query
        name: subscription_prorate
        description: If previewing an update to a subscription, this decides whether
          the preview will show the result of applying prorations or not
      - in: query
        name: subscription_proration_date
        description: If previewing an update to a subscription, and doing proration,
          `subscription_proration_date` forces the proration to be calculated as though
          the update was done at the specified time
      - in: query
        name: subscription_tax_percent
        description: If provided, the invoice returned will preview updating or creating
          a subscription with that tax percent
      - in: query
        name: subscription_trial_end
        description: If provided, the invoice returned will preview updating or creating
          a subscription with that trial end
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
      tags:
      - Invoices
      - Upcoming
  /invoices/{invoice}:
    get:
      summary: Get Invoices Invoice
      description: Retrieves the invoice with the given ID.
      operationId: getInvoicesInvoice
      x-api-path-slug: invoicesinvoice-get
      parameters:
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: path
        name: invoice
        description: The identifier of the desired invoice
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
      tags:
      - Invoices
      - Invoice
    post:
      summary: Add Invoices Invoice
      description: Until an invoice is paid, it is marked as open (closed=false).
        If you???d like to stop Stripe from attempting to collect payment on an invoice
        or would simply like to close the invoice out as no longer owed by the customer,
        you can update the closed parameter.
      operationId: postInvoicesInvoice
      x-api-path-slug: invoicesinvoice-post
      parameters:
      - in: path
        name: invoice
      - in: body
        name: payload
        description: Body parameters for the request
        schema:
          $ref: '#/definitions/holder'
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
      tags:
      - Invoices
      - Invoice
  /invoices/{invoice}/lines:
    get:
      summary: Get Invoices Invoice Lines
      description: When retrieving an invoice, you???ll get a lines property containing
        the total count of line items and the first handful of those items. There
        is also a URL where you can retrieve the full (paginated) list of line items.
      operationId: getInvoicesInvoiceLines
      x-api-path-slug: invoicesinvoicelines-get
      parameters:
      - in: query
        name: coupon
        description: For upcoming invoices, preview applying this coupon to the invoice
      - in: query
        name: customer
        description: In the case of upcoming invoices, the customer of the upcoming
          invoice is required
      - in: query
        name: ending_before
        description: A cursor for use in pagination
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: path
        name: invoice
        description: The ID of the invoice containing the lines to be retrieved
      - in: query
        name: limit
        description: The maximum number of line items to return
      - in: query
        name: starting_after
        description: A cursor for use in pagination
      - in: query
        name: subscription
        description: In the case of upcoming invoices, the subscription of the upcoming
          invoice is optional
      - in: query
        name: subscription_items
        description: For upcoming invoices, preview updating the subscription with
          this list of items
      - in: query
        name: subscription_prorate
        description: For upcoming invoices, this decides whether the preview will
          show the result of applying prorations or not
      - in: query
        name: subscription_proration_date
        description: For previewing upcoming invoices with proration, `subscription_proration_date`
          forces the proration to be calculated as though the update was done at the
          specified time
      - in: query
        name: subscription_tax_percent
      - in: query
        name: subscription_trial_end
        description: For upcoming invoices, preview updating or creating a subscription
          with that trial end
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
      tags:
      - Invoices
      - Invoice
      - Lines
  /invoices/{invoice}/pay:
    post:
      summary: Add Invoices Invoice Pay
      description: Stripe automatically creates and then attempts to collect payment
        on invoices for customers on subscriptions according to your subscriptions
        settings. However, if you???d like to attempt payment on an invoice out of
        the normal collection schedule or for some other reason, you can do so.
      operationId: postInvoicesInvoicePay
      x-api-path-slug: invoicesinvoicepay-post
      parameters:
      - in: path
        name: invoice
        description: ID of invoice to pay
      - in: body
        name: payload
        description: Body parameters for the request
        schema:
          $ref: '#/definitions/holder'
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
      tags:
      - Invoices
      - Invoice
      - Pay
  /invoiceitems/{invoiceitem}:
    delete:
      summary: Delete Invoiceitems Invoiceitem
      description: Removes an invoice item from the upcoming invoice. Removing an
        invoice item is only possible before the invoice it???s attached to is closed.
      operationId: deleteInvoiceitemsInvoiceitem
      x-api-path-slug: invoiceitemsinvoiceitem-delete
      parameters:
      - in: path
        name: invoiceitem
        description: The identifier of the invoice item to be deleted
      - in: body
        name: payload
        description: Body parameters for the request
        schema:
          $ref: '#/definitions/holder'
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
      tags:
      - Invoiceitems
      - Invoiceitem
    get:
      summary: Get Invoiceitems Invoiceitem
      description: Retrieves the invoice item with the given ID.
      operationId: getInvoiceitemsInvoiceitem
      x-api-path-slug: invoiceitemsinvoiceitem-get
      parameters:
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: path
        name: invoiceitem
        description: The ID of the desired invoice item
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
      tags:
      - Invoiceitems
      - Invoiceitem
    post:
      summary: Add Invoiceitems Invoiceitem
      description: Updates the amount or description of an invoice item on an upcoming
        invoice. Updating an invoice item is only possible before the invoice it???s
        attached to is closed.
      operationId: postInvoiceitemsInvoiceitem
      x-api-path-slug: invoiceitemsinvoiceitem-post
      parameters:
      - in: path
        name: invoiceitem
      - in: body
        name: payload
        description: Body parameters for the request
        schema:
          $ref: '#/definitions/holder'
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
      tags:
      - Invoiceitems
      - Invoiceitem
  /invoiceitems:
    get:
      summary: Get Invoiceitems
      description: Returns a list of your invoice items. Invoice items are returned
        sorted by creation date, with the most recently created invoice items appearing
        first.
      operationId: getInvoiceitems
      x-api-path-slug: invoiceitems-get
      parameters:
      - in: query
        name: created
      - in: query
        name: customer
        description: The identifier of the customer whose invoice items to return
      - in: query
        name: ending_before
        description: A cursor for use in pagination
      - in: query
        name: expand
        description: Specifies which fields in the response should be expanded
      - in: query
        name: limit
        description: A limit on the number of objects to be returned
      - in: query
        name: starting_after
        description: A cursor for use in pagination
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
      tags:
      - Invoiceitems
    post:
      summary: Add Invoiceitems
      description: Adds an arbitrary charge or credit to the customer???s upcoming
        invoice.
      operationId: postInvoiceitems
      x-api-path-slug: invoiceitems-post
      parameters:
      - in: body
        name: payload
        description: Body parameters for the request
        schema:
          $ref: '#/definitions/holder'
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
      tags:
      - Invoiceitems
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