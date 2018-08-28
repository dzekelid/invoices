{
  "info": {
    "name": "3Scale Billing API Invoice",
    "_postman_id": "b377b98a-c607-408d-a166-6fa83c4b5c17",
    "description": "Invoice.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Invoice",
      "item": [
        {
          "id": "93daab00-bd4d-4ce7-b8b3-8e826f48a577",
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
              "id": "bc844f12-5a40-41b3-9cc6-f9e80572cd63"
            }
          ]
        },
        {
          "id": "71d4864f-f142-40af-b70f-e9a6fa5c28ed",
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
              "id": "aed8d288-55a4-4750-9cd8-709ec91dde18"
            }
          ]
        },
        {
          "id": "4a27c389-67df-405e-9208-fad1c4123b4c",
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
              "id": "7ca862d6-559d-4e64-a7a6-82b8640a2713"
            }
          ]
        },
        {
          "id": "6c16ec9f-4494-4ac0-be3a-a2521714f4af",
          "name": "finance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "su1.3scale.net",
              "path": [
                "api/invoices/:id.xml"
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
            "description": "Invoice."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9e214302-f69d-421b-8c0c-da1153a01b90"
            }
          ]
        }
      ]
    }
  ]
}