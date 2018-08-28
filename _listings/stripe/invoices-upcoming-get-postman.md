{
  "info": {
    "name": "Stripe Get Invoices Upcoming",
    "_postman_id": "495d296a-bc63-4b50-ba3a-b8343f64a64d",
    "description": "At any time, you can preview the upcoming invoice for a customer. This will show you all the charges that are pending, including subscription renewal charges, invoice item charges, etc. It will also show you any discount that is applicable to the customer.Note that when you are viewing an upcoming invoice, you are simply viewing a preview – the invoice has not yet been created. As such, the upcoming invoice will not show up in invoice listing calls, and you cannot use the API to pay or edit the invoice. If you want to change the amount that your customer will be billed, you can add, remove, or update pending invoice items, or update the customer’s discount.You can preview the effects of updating a subscription, including a preview of what proration will take place. To ensure that the actual proration is calculated exactly the same as the previewed proration, you should pass a proration_date parameter when doing the actual subscription update. The value passed in should be the same as the subscription_proration_date returned on the upcoming invoice resource. The recommended way to get only the prorations being previewed is to consider only proration line items where period[start] is equal to the subscription_proration_date on the upcoming invoice resource.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "invoices",
      "item": [
        {
          "id": "24204eee-ede0-4c5d-8f44-6fbb52acbdb0",
          "name": "getInvoicesUpcoming",
          "request": {
            "url": "http://api.stripe.com/v1/invoices/upcoming?coupon=%7B%7D&customer=%7B%7D&expand=%7B%7D&invoice_items=%7B%7D&subscription=%7B%7D&subscription_items=%7B%7D&subscription_prorate=%7B%7D&subscription_proration_date=%7B%7D&subscription_tax_percent=%7B%7D&subscription_trial_end=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "At any time, you can preview the upcoming invoice for a customer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "98d595c3-fd42-4863-963f-852ec317bad3"
            }
          ]
        }
      ]
    }
  ]
}