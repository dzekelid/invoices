{
  "info": {
    "name": "Stripe Get Invoices",
    "_postman_id": "19948d64-a28d-4b5c-a361-9a027fd1b596",
    "description": "You can list all invoices, or list the invoices for a specific customer. The invoices are returned sorted by creation date, with the most recently created invoices appearing first.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "invoices",
      "item": [
        {
          "id": "636fbcdd-7456-493a-ac2c-22971b89fba8",
          "name": "getInvoices",
          "request": {
            "url": "http://api.stripe.com/v1/invoices?billing=%7B%7D&customer=%7B%7D&date=%7B%7D&due_date=%7B%7D&ending_before=%7B%7D&expand=%7B%7D&limit=%7B%7D&starting_after=%7B%7D&subscription=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "You can list all invoices, or list the invoices for a specific customer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4e7dfae5-14e3-4d15-8a36-7affc182bd15"
            }
          ]
        }
      ]
    }
  ]
}