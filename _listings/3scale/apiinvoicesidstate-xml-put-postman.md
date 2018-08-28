{
  "info": {
    "name": "3Scale Billing API Invoice",
    "_postman_id": "b74073b9-4079-4b77-870a-3aeba47351ba",
    "description": "Invoice.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Invoice",
      "item": [
        {
          "id": "df4ed68b-017f-41dd-9f3e-6b7333825573",
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
              "id": "84f559ff-4c65-4db9-ad1b-cf6003345339"
            }
          ]
        },
        {
          "id": "3bd7a07f-2506-48ab-b201-2a664d17f868",
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
              "id": "21a5d820-18ce-403f-a6c3-616b6a6e27d6"
            }
          ]
        },
        {
          "id": "bf55aba3-091a-47c6-ac4c-d66a3540dacf",
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
              "id": "d4f6bc28-00d1-4b1b-bc7e-8f96636a010a"
            }
          ]
        },
        {
          "id": "26916aef-bfc3-417d-847c-f437bb26e7fa",
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
              "id": "22d14441-4c52-4a0b-aba4-9b7cbf5f2bfd"
            }
          ]
        },
        {
          "id": "9d3f1009-e75c-4291-a85f-f279cb3650c2",
          "name": "finance",
          "request": {
            "url": {
              "protocol": "http",
              "host": "su1.3scale.net",
              "path": [
                "api/invoices/:id/state.xml"
              ],
              "query": [
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
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
              "id": "37c93428-fcd5-417d-8854-68fef5395ab3"
            }
          ]
        }
      ]
    }
  ]
}