[Webhooks Setup - WhatsApp Business Management API](https://developers.facebook.com/docs/whatsapp/business-management-api/guides/set-up-webhooks)

Subscribe Webhooks to get notifications for changes to your WhatsApp Business Account settings and quality signals.

Webhooks set up will not affect the phone number on your WhatsApp Business App. Only after you [migrate your number over to the WhatsApp Business Platform](https://developers.facebook.com/docs/whatsapp/overview/phone-number#migrate) can you no longer use that number on your WhatsApp Business App.

## Create an Endpoint

Before you can start receiving notifications you will need to create an endpoint on your server to receive notifications.

Your endpoint must be able to process two types of HTTPS requests: Verification Requests and Event Notifications. Since both requests use HTTPs, your server must have a valid TLS or SSL certificate correctly configured and installed. Self-signed certificates are not supported.

[Learn more about Verifying Requests and Event Notifications ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#create-endpoint) 

## Subcribe to Webhooks

To subscribe to Webhooks, you will need to get a Meta App ID and permissions. To do this go to the Meta App Dashboard. There you will:

1. [Create a Meta App in the Meta App Dashboard ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/development/create-an-app) 
2. [Add the Webhooks Product to your Meta app in the App Dashboard ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#configure-webhooks-product) 
    
    At any time, each Meta App can have only one endpoint configured. If you need to send your webhook updates to multiple endpoints, you need multiple Meta Apps.
    

When you are ready to scale your business messaging, you may need to:

1. [Add the `whatsapp_business_management` permission ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/development/create-an-app/app-dashboard#app-review) in your App Dashboard
2. [Successfully complete Meta App Review ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/app-review) – This step will take time but you can continue to test during the entire review process.

[](https://developers.facebook.com/docs/whatsapp/business-management-api/guides/set-up-webhooks#)

## Available Subscription Fields

|Field Name|Description|
|---|---|
|`account_alerts`|Notifies you of decisions related to Official Business Account status or a denial of messaging limit increases. Note that these are independent of [developer notifications](https://developers.facebook.com/docs/development/create-an-app/developer-settings#notification-settings).|
|`account_review_update`|A notification is sent to you when a WhatsApp Business Account has been reviewed.|
|`account_update`|A notification is sent to you when a change to your WhatsApp Business Account has occurred. This change can include phone number update, a [policy violation](https://developers.facebook.com/docs/whatsapp/overview/policy-enforcement), a WhatsApp Business Account has been banned and more.|
|`business_capability_update`|Notifies you of changes to a business's capabilities. This can include changes to the maximum number of business phone numbers your WhatsApp Business Account can have, or a change to the [messaging limit](https://developers.facebook.com/docs/whatsapp/messaging-limits) for all of your WhatsApp Business Account's business phone numbers.|
|`message_template_quality_update`|A notification is sent to you when a message template's quality rating changes.|
|`message_template_status_update`|A notification is sent to you when the message template has been approved or rejected, or if it has been disabled.|
|`messages`|A notification is sent to you when your business has received a message from a customer, when you send a message to a customer, when a message is delivered to a customer, and when your message is read by a customer.|
|`phone_number_name_update`|A notification is sent to you when the name associated with a phone number has been approved or rejected.|
|`phone_number_quality_update`|A notification is sent to you when the [business phone number quality status](https://www.facebook.com/business/help/896873687365001) changes. See [Monitor Quality Signals](https://developers.facebook.com/docs/whatsapp/guides/how-to-monitor-quality-signals) for additional information.|
|`security`|A notification is sent to you when:<br><br>- you request to disable two-step verification code<br>- the two-step verification code is disabled<br>- the two-step verification code is updated|
|`template_category_update`|A notification is sent to you when a template's category changes, indicating the template's previous and new category.|

Visit the [WhatsApp Business Account Webhooks Reference ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/graph-api/webhooks/reference/whatsapp-business-account/) for more information about each payload field and the [WhatsApp Cloud API Webhooks Reference ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/whatsapp/cloud-api/webhooks/components) for more information on the different types of `messages` notifications you can receive.

### Notification Payload

All notifications have the following generic format:

```json
[{
    "object": "whatsapp_business_account",
    "entry": [{
       "id": "_{whatsapp-business-account-id}_",
        "time": _{unix-timestamp}_,
        "changes": [{
            "field": "_{subscribed-field}_",
            "value": {
                # Information that was update
            }
          }]
      }]
  }]
```

The top level array contains two main objects:

|Parameter|Description|
|---|---|
|[`object`](https://developers.facebook.com/docs/whatsapp/business-management-api/webhooks/components)|This is the object that was subscribed to.|
|[`entry`](https://developers.facebook.com/docs/whatsapp/business-management-api/webhooks/components#entry-object)|This object contains the details of the change that triggered the webhooks call.|

See [Components](https://developers.facebook.com/docs/whatsapp/business-management-api/webhooks/components) for all available webhooks objects.

[](https://developers.facebook.com/docs/whatsapp/business-management-api/guides/set-up-webhooks#)

## Sample App Endpoints

- [Sample App Endpoints using Glitch ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/sample-app-endpoints) 
    
- [Sample App Endpoints using Heroku ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/graph-api/webhooks/sample-apps)