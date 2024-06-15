[Getting Started - Meta Webhooks](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#configure-webhooks-product)
## Configuring the Webhooks Product

Once your endpoint or sample app is ready, use your app's [App Dashboard](https://developers.facebook.com/apps/) to add and configure the Webhooks product. You can also do this programmatically by using the [`/{app-id}/subscriptions` endpoint](https://developers.facebook.com/docs/graph-api/reference/application/subscriptions) for all Webhooks except [Instagram](https://developers.facebook.com/docs/instagram-api/guides/webhooks).

In this example we'll use the dashboard to configure a Webhook that subscribes to any changes to the photos of any of your app's Users.

1. In the App Dashboard, go to **Products** > **Webhooks**, select **User** from the drop-down menu, then click **Subscribe to this object**.
    
    ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/28578042_231932047352922_7562214390548660224_n.png?_nc_cat=106&ccb=1-7&_nc_sid=e280be&_nc_ohc=xOwkZxiIoYAQ7kNvgF0V7Js&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYCRjC_75bTFxyDrbZQiddfhrzEDIl11psYzZnhGaLNsQA&oe=66833AFA)
    
    Choosing the User object.
    
2. Enter your endpoint's URL in the **Callback URL** field and enter a string in the **Verify Token** field. We will include this string in all [Verification Requests](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#verification-requests). If you are using one of our sample apps, this should be the same string you used for your app's `TOKEN` config variable.
    
    If you want event notification payloads to include the names of the fields that have changed as well as their new values, set the **Include Values** toggle to **Yes**.
    
    ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/26906757_2023310897989945_1753801942011740160_n.png?_nc_cat=101&ccb=1-7&_nc_sid=e280be&_nc_ohc=mf5rCTtD5PQQ7kNvgHew1gu&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYDVZ3JvqJ2nU4Eshuaw5N-bKcoE2UeYoNA9ffXFZaX9qQ&oe=6683451C)
    
    Entering an endpoint URL and a verification token string.
    
3. Once you click **Verify and Save**, we'll send your endpoint a Verification Request which you must [validate](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#validate-requests). If your endpoint successfully validates the request, you should see this:
    
    ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/28578201_353858248459965_4983102755687104512_n.png?_nc_cat=105&ccb=1-7&_nc_sid=e280be&_nc_ohc=lUtxVv8Afj8Q7kNvgES6sLi&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBS7Yfxd9J1kjVvnAEv7b8ez0BW4lKUrv9ZJquaITHAvA&oe=66833FD1)
    
    Successful validation.
    
4. The last step is to subscribe to individual fields. Subscribe to the `photos` field and send a test Event Notification.
    
    ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/28578275_637235979960743_9002663837995892736_n.png?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=Z92d8wqr34AQ7kNvgE578NH&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBIuJzh8QT-U5aB4_oZPzBRUy84DQzsH6qR1tFFqqUGMw&oe=66832FD4)
    
    Subscribing to the Photos field on the User object.
    
    If your endpoint is set up correctly, it should [validate the payload](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#validate-payloads) and execute whatever code you have set it up to do upon successful validation. If you are using our [sample app](https://developers.facebook.com/docs/graph-api/webhooks/sample-apps), load the app's URL in your web browser. It should display the payload's contents:
    
    ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/28967070_176977706438684_6537686724187783168_n.png?_nc_cat=109&ccb=1-7&_nc_sid=e280be&_nc_ohc=Vb22JIrn_OAQ7kNvgEFQ2ci&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYDvq5REJjytu1aLTyDTa4uB84f8-tJJ0eCJRyjF_6wd3w&oe=66835470)
    
    Sample App displaying test notifcation payload.
    

[](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#)

## Next Steps

Now that you know how to set up Webhooks, you may want to refer our additional documents that describe the extra steps involved when setting up Webhooks for specific products:

- [Webhooks for Ad Accounts](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-ad-accounts)
- [Webhooks for Certificate Transparency](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-certificate-transparency)
- [Webhooks for Instagram](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-instagram)
- [Webhooks for Leads](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-leadgen)
- [Webhooks for Messenger](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-messenger)
- [Webhooks for Pages](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-pages)
- [Webhooks for Payments](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-payments)
- [Webhooks for WhatsApp](https://developers.facebook.com/docs/graph-api/webhooks/getting-started/webhooks-for-whatsapp)