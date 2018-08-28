{
  "info": {
    "name": "3Scale Billing API Invoice List",
    "_postman_id": "44e2a5a6-ee87-4cc5-a91a-c7f24e356ff5",
    "description": "Invoice list.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Invoice",
      "item": [
        {
          "id": "535cebe7-4dab-4781-ad99-f06bfa4af8fd",
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
              "id": "121217be-e311-41ee-b154-36aefe912090"
            }
          ]
        },
        {
          "id": "9b34003f-acd5-43bc-8cde-54eeab2ccc28",
          "name": "finance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "su1.3scale.net",
              "path": [
                "api/accounts/:account_id/invoices/:id.xml"
              ],
              "query": [
                {
                  "key": "provider_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "account_id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Invoice by account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "37e63d2a-c6ca-40ac-8aa0-d70904dc3b04"
            }
          ]
        },
        {
          "id": "080997fa-fa19-475c-98d6-09a235bd3991",
          "name": "finance",
          "request": {
            "url": "http://su1.3scale.net/api/invoices.xml?month=%7B%7D&page=%7B%7D&per_page=%7B%7D&provider_key=%7B%7D&state=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Invoice list."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "932957ca-6229-448b-9dcf-3151c5d5beb5"
            }
          ]
        }
      ]
    }
  ]
}