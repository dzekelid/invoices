---
name: Stripe
description: 'Stripe is a simple, developer-friendly way to accept payments online.
  They believe that enabling transactions on the web is a problem rooted in code,
  not finance, and they want to help put more websites in business. '
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/stripe-black.png
x-kinRank: "10"
x-alexaRank: ""
tags:
- Stripe Stack
- Stack Network
- Stack
- Payments
- Payments
- Payment API
- Invoicing
- Imports
- Finance
- Change Log Example
- Change Log
- Billing
- API LIfeycle
created: "2018-03-25"
modified: "2018-03-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/apis.yaml
specificationVersion: "0.14"
apis:
- name: Stripe
  description: Stripe is a simple, developer-friendly way to accept payments online
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/stripe-black.png
  humanURL: ""
  baseURL: https://api.stripe.com/v1/
  tags: Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-invoice-pay-post.md
- name: Stripe Get Invoices Upcoming
  description: "At any time, you can preview the upcoming invoice for a customer.
    This will show you all the charges that are pending, including subscription renewal
    charges, invoice item charges, etc. It will also show you any discount that is
    applicable to the customer.Note that when you are viewing an upcoming invoice,
    you are simply viewing a preview \u2013 the invoice has not yet been created.
    As such, the upcoming invoice will not show up in invoice listing calls, and you
    cannot use the API to pay or edit the invoice. If you want to change the amount
    that your customer will be billed, you can add, remove, or update pending invoice
    items, or update the customer\u2019s discount.You can preview the effects of updating
    a subscription, including a preview of what proration will take place. To ensure
    that the actual proration is calculated exactly the same as the previewed proration,
    you should pass a proration_date parameter when doing the actual subscription
    update. The value passed in should be the same as the subscription_proration_date
    returned on the upcoming invoice resource. The recommended way to get only the
    prorations being previewed is to consider only proration line items where period[start]
    is equal to the subscription_proration_date on the upcoming invoice resource."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/stripe-black.png
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-upcoming-get.md
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-upcoming-get-postman.md
x-common:
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
- type: x-github
  url: https://github.com/stripe
- type: x-pricing
  url: https://stripe.com/us/pricing
- type: x-twitter
  url: https://twitter.com/stripe
- type: x-website
  url: https://stripe.com/
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
- type: x-github
  url: https://github.com/stripe
- type: x-pricing
  url: https://stripe.com/us/pricing
- type: x-twitter
  url: https://twitter.com/stripe
- type: x-website
  url: https://stripe.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---