{
  "info": {
    "name": "Dezrez Get agent fees invoices earned",
    "_postman_id": "30029ea1-f371-45f7-a931-4d574d792938",
    "description": "Get agent fees invoices earned.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "S",
      "item": [
        {
          "id": "80b05cb3-f16f-41c6-9cb5-e73a1debc09a",
          "name": "AccountingSystem_GetAgentCash",
          "request": {
            "url": "http://api.dezrez.com/api/accountingsystem/agentcash",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets overview of the agent cash account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b324f0db-c8ff-4894-bd29-118eef1e610f"
            }
          ]
        }
      ]
    },
    {
      "name": "Agent",
      "item": [
        {
          "id": "e4eef96d-29af-418d-accd-7e177c160eb2",
          "name": "Invoice_GetAgentFeesEarned",
          "request": {
            "url": "http://api.dezrez.com/api/invoice/fees",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get agent fees invoices earned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef178dd0-5fd1-4d63-bd58-a7fe7a724f26"
            }
          ]
        }
      ]
    }
  ]
}