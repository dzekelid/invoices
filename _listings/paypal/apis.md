---
name: PayPal
x-slug: paypal
description: PayPal is the faster, safer way to send money, make an online payment,
  receive money or set up a merchant account.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
x-kinRank: "10"
x-alexaRank: "71"
tags: Invoices
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/apis.md
specificationVersion: "0.14"
apis:
- name: Paypal Search Invoices
  x-api-slug: paypal
  description: Use the SearchInvoice API operation to search an invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/SearchInvoices
  tags: Payments,Invoices,Search
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicesearchinvoices-post-openapi.md
- name: Paypal Mark Invoice As Paid
  x-api-slug: paypal
  description: Use the MarkInvoiceAsPaid API operation to mark an invoice as paid.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/MarkInvoiceAsPaid
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicemarkinvoiceaspaid-post-openapi.md
- name: Paypal Cancel Invoice
  x-api-slug: paypal
  description: Use the CancelInvoice API operation to cancel an invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/Cancel Invoice
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicecancel-invoice-post-openapi.md
- name: Paypal Get Invoice Details
  x-api-slug: paypal
  description: Use the GetInvoiceDetails API operation to get detailed information
    about an invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/GetInvoiceDetails
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicegetinvoicedetails-post-openapi.md
- name: Paypal Update Invoice
  x-api-slug: paypal
  description: Use the UpdateInvoice API operation to update an invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/UpdateInvoice
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoiceupdateinvoice-post-openapi.md
- name: Paypal Create And Send Invoice
  x-api-slug: paypal
  description: Use the CreateAndSendInvoice API operation to create and send an invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/CreateAndSendInvoice
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicecreateandsendinvoice-post-openapi.md
- name: Paypal Send Invoice
  x-api-slug: paypal
  description: Use the SendInvoice API operation to send an invoice to a payer, and
    notify the payer of the pending invoice.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/SendInvoice
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicesendinvoice-post-openapi.md
- name: Paypal Create Invoice
  x-api-slug: paypal
  description: Use the CreateInvoice API operation to create a new invoice. The call
    includes merchant, payer, and API caller information, in addition to invoice detail.
    The response to the call contains an invoice ID and URL.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com////Invoice/CreateInvoice
  tags: Payments,Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/invoicecreateinvoice-post-openapi.md
- name: Paypal
  x-api-slug: paypal
  description: PayPal is the faster, safer way to send money, make an online payment,
    receive money or set up a merchant account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/237-paypal.jpg
  humanURL: https://paypal.com
  baseURL: https://svcs.sandbox.paypal.com//
  tags: Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/paypal/openapi.md
x-common:
- type: x-base-url
  url: https://api.paypal.com
- type: x-crunchbase
  url: https://crunchbase.com/organization/paypal
- type: x-crunchbase
  url: http://www.crunchbase.com/company/paypal
- type: x-developer
  url: https://developer.paypal.com/
- type: x-faq
  url: https://developer.paypal.com/docs/faq/
- type: x-getting-started
  url: https://developer.paypal.com/docs/
- type: x-github
  url: https://github.com/paypal
- type: x-playground
  url: https://devtools-paypal.com/hateoas/index.html
- type: x-privacy
  url: https://www.paypal.com/us/cgi-bin/webscr?cmd=p/gen/ua/policy_privacy-outside
- type: x-release-notes
  url: https://developer.paypal.com/docs/release-notes/
- type: x-terms-of-service
  url: https://cms.paypal.com/us/cgi-bin/?cmd=_render-content&content_ID=ua/Legal_Hub_full
- type: x-twitter
  url: https://twitter.com/paypal
- type: x-website
  url: https://paypal.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---