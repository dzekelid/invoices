{
  "info": {
    "name": "Stripe Get Invoices Invoice Lines",
    "_postman_id": "c9a52194-11e3-4af9-ae7c-ed7e847c54ea",
    "description": "When retrieving an invoice, you’ll get a lines property containing the total count of line items and the first handful of those items. There is also a URL where you can retrieve the full (paginated) list of line items.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "invoices",
      "item": [
        {
          "id": "357f504a-deea-4d6e-9945-ac9671dd2d4f",
          "name": "getInvoicesInvoiceLines",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stripe.com",
              "path": [
                "v1",
                "invoices/:invoice/lines"
              ],
              "query": [
                {
                  "key": "coupon",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "customer",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "ending_before",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "starting_after",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subscription",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subscription_items",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subscription_prorate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subscription_proration_date",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subscription_tax_percent",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "subscription_trial_end",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "invoice",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "When retrieving an invoice, you’ll get a lines property containing the total count of line items and the first handful of those items"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90638014-438a-48c0-9f1b-447161c4afbc"
            }
          ]
        }
      ]
    }
  ]
}