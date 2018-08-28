---
name: Azure Billing API
x-slug: azure-billing-api
description: Use Azure Billing APIs to pull usage and resource data into your preferred
  data analysis tools. The Azure Resource Usage and RateCard APIs can help you accurately
  predict and manage your costs. The APIs are implemented as a Resource Provider and
  part of the family of APIs exposed by the Azure Resource Manager.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Invoices
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/apis.md
specificationVersion: "0.14"
apis:
- name: ConsumptionManagementClient - Invoices List
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get
  description: Lists the available invoices for a subscription in reverse chronological
    order beginning with the most recent invoice. In preview, invoices are available
    via this API only for invoice periods which end December 1, 2016 or later.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get-openapi.md
- name: ConsumptionManagementClient - Invoices Get
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get
  description: Gets a named invoice resource. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get-openapi.md
- name: ConsumptionManagementClient - Invoices Get Latest
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get
  description: Gets the most recent invoice. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get-openapi.md
- name: ConsumptionManagementClient - Invoices List
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get
  description: Lists the available invoices for a subscription in reverse chronological
    order beginning with the most recent invoice. In preview, invoices are available
    via this API only for invoice periods which end December 1, 2016 or later.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get-openapi.md
- name: ConsumptionManagementClient - Invoices Get
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get
  description: Gets a named invoice resource. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get-openapi.md
- name: ConsumptionManagementClient - Invoices Get Latest
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get
  description: Gets the most recent invoice. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get-openapi.md
- name: ConsumptionManagementClient - Invoices Get Latest
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get
  description: Gets the most recent invoice. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoiceslatest-get-openapi.md
- name: ConsumptionManagementClient - Invoices Get
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get
  description: Gets a named invoice resource. When getting a single invoice, the downloadUrl
    property is expanded automatically.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoicesinvoicename-get-openapi.md
- name: ConsumptionManagementClient - Invoices List
  x-api-slug: subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get
  description: Lists the available invoices for a subscription in reverse chronological
    order beginning with the most recent invoice. In preview, invoices are available
    via this API only for invoice periods which end December 1, 2016 or later.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-billing-api.png
  humanURL: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
  baseURL: ://management.azure.com//
  tags: Billing, Management, Microsoft, Stack Network, API Service Provider, API Provider,
    Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/invoices/master/_listings/azure-billing-api/subscriptionssubscriptionidprovidersmicrosoft-billinginvoices-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://azure.batch.api.gallery.streamdata.io
- type: x-api-stack
  url: http://azure.billing.api.stack.network
- type: x-website
  url: https://docs.microsoft.com/en-us/azure/billing/billing-usage-rate-card-overview
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---