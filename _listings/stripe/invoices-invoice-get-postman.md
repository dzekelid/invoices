{
  "info": {
    "name": "Stripe Get Invoices Invoice",
    "_postman_id": "c949055f-6006-4f3f-8db7-8bbf0df3e08a",
    "description": "Retrieves the invoice with the given ID.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "invoices",
      "item": [
        {
          "id": "26e7a56b-1133-4cd6-ae4c-6436c5c192bf",
          "name": "getInvoicesInvoice",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stripe.com",
              "path": [
                "v1",
                "invoices/:invoice"
              ],
              "query": [
                {
                  "key": "expand",
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
            "description": "Retrieves the invoice with the given ID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30014e69-0b66-45e1-9cf4-20030ad1c7aa"
            }
          ]
        }
      ]
    }
  ]
}