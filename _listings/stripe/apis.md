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
- name: Stripe Add Invoices
  description: "If you need to invoice your customer outside the regular billing cycle,
    you can create an invoice that pulls in all pending invoice items, including prorations.
    The customer\u2019s billing cycle and regular subscription won\u2019t be affected.Once
    you create the invoice, Stripe will attempt to collect payment according to your
    subscriptions settings, though you can choose to pay it right away."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/stripe-black.png
  humanURL: https://stripe.com/
  baseURL: https://api.stripe.com/v1/
  tags: Invoices
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/stripe/invoices-post.md
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