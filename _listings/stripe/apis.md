---
name: Stripe
x-slug: stripe
description: Online payment processing for internet businesses. Stripe is a suite
  of payment APIs that powers commerce for online businesses of all sizes, including
  fraud prevention, and subscription management. Use Stripes payment platform to accept
  and process p...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
x-kinRank: "10"
x-alexaRank: "1914"
tags: Invoices
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/apis.md
specificationVersion: "0.14"
apis:
- name: Stripe - Get Invoices
  x-api-slug: invoices-get
  description: You can list all invoices, or list the invoices for a specific customer.
    The invoices are returned sorted by creation date, with the most recently created
    invoices appearing first.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-get-openapi.md
- name: Stripe - Add Invoices
  x-api-slug: invoices-post
  description: If you need to invoice your customer outside the regular billing cycle,
    you can create an invoice that pulls in all pending invoice items, including prorations.
    The customer???s billing cycle and regular subscription won???t be affected.Once
    you create the invoice, Stripe will attempt to collect payment according to your
    subscriptions settings, though you can choose to pay it right away.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-post-openapi.md
- name: Stripe - Get Invoices Upcoming
  x-api-slug: invoicesupcoming-get
  description: At any time, you can preview the upcoming invoice for a customer. This
    will show you all the charges that are pending, including subscription renewal
    charges, invoice item charges, etc. It will also show you any discount that is
    applicable to the customer.Note that when you are viewing an upcoming invoice,
    you are simply viewing a preview ??? the invoice has not yet been created. As
    such, the upcoming invoice will not show up in invoice listing calls, and you
    cannot use the API to pay or edit the invoice. If you want to change the amount
    that your customer will be billed, you can add, remove, or update pending invoice
    items, or update the customer???s discount.You can preview the effects of updating
    a subscription, including a preview of what proration will take place. To ensure
    that the actual proration is calculated exactly the same as the previewed proration,
    you should pass a proration_date parameter when doing the actual subscription
    update. The value passed in should be the same as the subscription_proration_date
    returned on the upcoming invoice resource. The recommended way to get only the
    prorations being previewed is to consider only proration line items where period[start]
    is equal to the subscription_proration_date on the upcoming invoice resource.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesupcoming-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesupcoming-get-openapi.md
- name: Stripe - Get Invoices Invoice
  x-api-slug: invoicesinvoice-get
  description: Retrieves the invoice with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-openapi.md
- name: Stripe - Add Invoices Invoice
  x-api-slug: invoicesinvoice-post
  description: Until an invoice is paid, it is marked as open (closed=false). If you???d
    like to stop Stripe from attempting to collect payment on an invoice or would
    simply like to close the invoice out as no longer owed by the customer, you can
    update the closed parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-post-openapi.md
- name: Stripe - Get Invoices Invoice Lines
  x-api-slug: invoicesinvoicelines-get
  description: When retrieving an invoice, you???ll get a lines property containing
    the total count of line items and the first handful of those items. There is also
    a URL where you can retrieve the full (paginated) list of line items.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-openapi.md
- name: Stripe - Add Invoices Invoice Pay
  x-api-slug: invoicesinvoicepay-post
  description: Stripe automatically creates and then attempts to collect payment on
    invoices for customers on subscriptions according to your subscriptions settings.
    However, if you???d like to attempt payment on an invoice out of the normal collection
    schedule or for some other reason, you can do so.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicepay-post-openapi.md
- name: Stripe - Get Invoices Invoice
  x-api-slug: invoicesinvoice-get
  description: Retrieves the invoice with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-openapi.md
- name: Stripe - Add Invoices Invoice
  x-api-slug: invoicesinvoice-post
  description: Until an invoice is paid, it is marked as open (closed=false). If you???d
    like to stop Stripe from attempting to collect payment on an invoice or would
    simply like to close the invoice out as no longer owed by the customer, you can
    update the closed parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-post-openapi.md
- name: Stripe - Get Invoices Invoice Lines
  x-api-slug: invoicesinvoicelines-get
  description: When retrieving an invoice, you???ll get a lines property containing
    the total count of line items and the first handful of those items. There is also
    a URL where you can retrieve the full (paginated) list of line items.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-openapi.md
- name: Stripe - Add Invoices Invoice Pay
  x-api-slug: invoicesinvoicepay-post
  description: Stripe automatically creates and then attempts to collect payment on
    invoices for customers on subscriptions according to your subscriptions settings.
    However, if you???d like to attempt payment on an invoice out of the normal collection
    schedule or for some other reason, you can do so.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicepay-post-openapi.md
- name: Stripe - Delete Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-delete
  description: Removes an invoice item from the upcoming invoice. Removing an invoice
    item is only possible before the invoice it???s attached to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-delete-openapi.md
- name: Stripe - Get Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-get
  description: Retrieves the invoice item with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-get-openapi.md
- name: Stripe - Add Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-post
  description: Updates the amount or description of an invoice item on an upcoming
    invoice. Updating an invoice item is only possible before the invoice it???s attached
    to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-post-openapi.md
- name: Stripe - Get Invoiceitems
  x-api-slug: invoiceitems-get
  description: Returns a list of your invoice items. Invoice items are returned sorted
    by creation date, with the most recently created invoice items appearing first.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitems-get-openapi.md
- name: Stripe - Add Invoiceitems
  x-api-slug: invoiceitems-post
  description: Adds an arbitrary charge or credit to the customer???s upcoming invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitems-post-openapi.md
- name: Stripe - Delete Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-delete
  description: Removes an invoice item from the upcoming invoice. Removing an invoice
    item is only possible before the invoice it???s attached to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-delete-openapi.md
- name: Stripe - Get Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-get
  description: Retrieves the invoice item with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-get-openapi.md
- name: Stripe - Add Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-post
  description: Updates the amount or description of an invoice item on an upcoming
    invoice. Updating an invoice item is only possible before the invoice it???s attached
    to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-post-openapi.md
- name: Stripe - Get Invoices Invoice
  x-api-slug: invoicesinvoice-get
  description: Retrieves the invoice with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-openapi.md
- name: Stripe - Add Invoices Invoice
  x-api-slug: invoicesinvoice-post
  description: Until an invoice is paid, it is marked as open (closed=false). If you???d
    like to stop Stripe from attempting to collect payment on an invoice or would
    simply like to close the invoice out as no longer owed by the customer, you can
    update the closed parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-post-openapi.md
- name: Stripe - Get Invoices Invoice Lines
  x-api-slug: invoicesinvoicelines-get
  description: When retrieving an invoice, you???ll get a lines property containing
    the total count of line items and the first handful of those items. There is also
    a URL where you can retrieve the full (paginated) list of line items.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-openapi.md
- name: Stripe - Add Invoices Invoice Pay
  x-api-slug: invoicesinvoicepay-post
  description: Stripe automatically creates and then attempts to collect payment on
    invoices for customers on subscriptions according to your subscriptions settings.
    However, if you???d like to attempt payment on an invoice out of the normal collection
    schedule or for some other reason, you can do so.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicepay-post-openapi.md
- name: Stripe - Delete Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-delete
  description: Removes an invoice item from the upcoming invoice. Removing an invoice
    item is only possible before the invoice it???s attached to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-delete-openapi.md
- name: Stripe - Get Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-get
  description: Retrieves the invoice item with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-get-openapi.md
- name: Stripe - Add Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-post
  description: Updates the amount or description of an invoice item on an upcoming
    invoice. Updating an invoice item is only possible before the invoice it???s attached
    to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-post-openapi.md
- name: Stripe - Get Invoiceitems
  x-api-slug: invoiceitems-get
  description: Returns a list of your invoice items. Invoice items are returned sorted
    by creation date, with the most recently created invoice items appearing first.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitems-get-openapi.md
- name: Stripe - Add Invoiceitems
  x-api-slug: invoiceitems-post
  description: Adds an arbitrary charge or credit to the customer???s upcoming invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitems-post-openapi.md
- name: Stripe - Delete Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-delete
  description: Removes an invoice item from the upcoming invoice. Removing an invoice
    item is only possible before the invoice it???s attached to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-delete-openapi.md
- name: Stripe - Get Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-get
  description: Retrieves the invoice item with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-get-openapi.md
- name: Stripe - Add Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-post
  description: Updates the amount or description of an invoice item on an upcoming
    invoice. Updating an invoice item is only possible before the invoice it???s attached
    to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-post-openapi.md
- name: Stripe - Add Invoices Invoice Pay
  x-api-slug: invoicesinvoicepay-post
  description: Stripe automatically creates and then attempts to collect payment on
    invoices for customers on subscriptions according to your subscriptions settings.
    However, if you???d like to attempt payment on an invoice out of the normal collection
    schedule or for some other reason, you can do so.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicepay-post-openapi.md
- name: Stripe - Get Invoices Invoice Lines
  x-api-slug: invoicesinvoicelines-get
  description: When retrieving an invoice, you???ll get a lines property containing
    the total count of line items and the first handful of those items. There is also
    a URL where you can retrieve the full (paginated) list of line items.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoicelines-get-openapi.md
- name: Stripe - Add Invoices Invoice
  x-api-slug: invoicesinvoice-post
  description: Until an invoice is paid, it is marked as open (closed=false). If you???d
    like to stop Stripe from attempting to collect payment on an invoice or would
    simply like to close the invoice out as no longer owed by the customer, you can
    update the closed parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-post-openapi.md
- name: Stripe - Get Invoices Invoice
  x-api-slug: invoicesinvoice-get
  description: Retrieves the invoice with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoicesinvoice-get-openapi.md
- name: Stripe - Add Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-post
  description: Updates the amount or description of an invoice item on an upcoming
    invoice. Updating an invoice item is only possible before the invoice it???s attached
    to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-post-openapi.md
- name: Stripe - Get Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-get
  description: Retrieves the invoice item with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-get-openapi.md
- name: Stripe - Delete Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-delete
  description: Removes an invoice item from the upcoming invoice. Removing an invoice
    item is only possible before the invoice it???s attached to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-delete-openapi.md
- name: Stripe - Add Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-post
  description: Updates the amount or description of an invoice item on an upcoming
    invoice. Updating an invoice item is only possible before the invoice it???s attached
    to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-post-openapi.md
- name: Stripe - Get Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-get
  description: Retrieves the invoice item with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-get-openapi.md
- name: Stripe - Delete Invoiceitems Invoiceitem
  x-api-slug: invoiceitemsinvoiceitem-delete
  description: Removes an invoice item from the upcoming invoice. Removing an invoice
    item is only possible before the invoice it???s attached to is closed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitemsinvoiceitem-delete-openapi.md
- name: Stripe - Add Invoiceitems
  x-api-slug: invoiceitems-post
  description: Adds an arbitrary charge or credit to the customer???s upcoming invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitems-post-openapi.md
- name: Stripe - Get Invoiceitems
  x-api-slug: invoiceitems-get
  description: Returns a list of your invoice items. Invoice items are returned sorted
    by creation date, with the most recently created invoice items appearing first.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/254-stripe.jpg
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Billing, Finance, Payments, Payments, Stripe Stack, Imports, Change Log Example,
    Stack Network, Stack, SaaS, Invoices, Payments, Relative Data, Service API, Relative
    StreamRank, Streams
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoiceitems-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://stride.api.gallery.streamdata.io
- type: x-api-stack
  url: http://stripe.stack.network
- type: x-base
  url: https://api.stripe.com/
- type: x-blog
  url: https://stripe.com/blog
- type: x-blog-rss
  url: https://stripe.com/blog/feed.rss
- type: x-change-log
  url: https://stripe.com/docs/upgrades
- type: x-crunchbase
  url: http://www.crunchbase.com/company/stripe
- type: x-crunchbase
  url: https://crunchbase.com/organization/stripe
- type: x-email
  url: info@stripe.com
- type: x-email
  url: privacy@stripe.com
- type: x-email
  url: atlas@stripe.com
- type: x-email
  url: notices@stripe.com
- type: x-email
  url: jane.diaz@stripe.com
- type: x-email
  url: nonprofit@stripe.com
- type: x-email
  url: support@stripe.com
- type: x-email
  url: dpo@stripe.com
- type: x-github
  url: https://github.com/stripe
- type: x-linkedin
  url: https://www.linkedin.com/company/stripe/
- type: x-pricing
  url: https://stripe.com/us/pricing
- type: x-twitter
  url: https://twitter.com/stripe
- type: x-website
  url: https://stripe.com/
- type: x-website
  url: http://stripe.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---