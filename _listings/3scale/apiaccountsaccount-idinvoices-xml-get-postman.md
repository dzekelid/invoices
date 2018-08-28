{
  "info": {
    "name": "3Scale Billing API Invoice List by Account",
    "_postman_id": "ac689c5b-a628-4009-875c-7899f449c6c8",
    "description": "Invoice list by account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Invoice",
      "item": [
        {
          "id": "21350ec0-b8b4-4815-9462-d45598e7967b",
          "name": "finance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "su1.3scale.net",
              "path": [
                "api/accounts/:account_id/invoices.xml"
              ],
              "query": [
                {
                  "key": "month",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "per_page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "provider_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "state",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "account_id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Invoice list by account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "638101a0-5f18-4125-8462-ec420243a7ce"
            }
          ]
        }
      ]
    }
  ]
}