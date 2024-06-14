url:: [Get Started - WhatsApp Business Management API](https://developers.facebook.com/docs/whatsapp/business-management-api/get-started)
course:: [Set up the WhatsApp Business Platform : Learn new skills to build your brand or business](https://www.facebookblueprint.com/student/collection/409587/path/360218)


## Started
Requirement
- [[001 Create Meta Business Portfolio]]
- [[002 Business App]]

## Webhooks Setup
[[Webhooks Setup - WhatsApp Business Management API]]
#### Subscribe
[Getting Started - Meta Webhooks](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#configure-webhooks-product)
- Use sample apps
  [Sample App Endpoints using Glitch ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/sample-app-endpoints) 
  [Sample App Endpoints using Heroku ![](https://scontent.fmlg11-1.fna.fbcdn.net/v/t39.2365-6/276034258_1045248339390233_3876773921429146148_n.png?stp=dst-webp&_nc_cat=110&ccb=1-7&_nc_sid=e280be&_nc_ohc=81-3ZJVfydoQ7kNvgEYhkTg&_nc_ht=scontent.fmlg11-1.fna&oh=00_AYBdmBQag3KBrsEiLQ1HpHhRGtbWiWSsL0J6RMfwTCXXqQ&oe=66835575)](https://developers.facebook.com/docs/graph-api/webhooks/sample-apps)
- App Dashboard, go to **Products** > **Webhooks**, select **User** from the drop-down menu, then click **Subscribe to this object**.
- Enter your endpoint's URL in the **Callback URL** field and enter a string in the **Verify Token** field. We will include this string in all [Verification Requests](https://developers.facebook.com/docs/graph-api/webhooks/getting-started#verification-requests). If you are using one of our sample apps, this should be the same string you used for your app's `TOKEN` config variable.
  If you want event notification payloads to include the names of the fields that have changed as well as their new values, set the **Include Values** toggle to **Yes**.
  - In the `.env` file, update the value of the `WEBHOOK_VERIFY_TOKEN` to a random string of your choosing. Then, you can optionally, copy the value of your temporary/permanent access token from **WhatsApp > API Setup** in your App Dashboard and paste that value for `GRAPH_API_TOKEN`.
- Click **Share** at the top right to get the **Live site** URL. Add `/webhook` at the end of the URL to get your complete callback URL. It will look something like `https://<project-name>.glitch.me/webhook`.
- [quanta-squire.glitch.me/webhook](https://quanta-squire.glitch.me/webhook)
- 


Token
[EAAQjPJoqXKIBOyVg8I76qZAzSY3WWocO2DVZAiNLLOoITuUVBYMqU3ZBJCgoh14nM434Acrn6nkhInVGBuuE18Iz6A1dYRJRQ82pUoZBONUQgQ3gCgh7P3WZCoVUPh395HV7jV0k9zW2xR0aktK7BZBZAQbiL0MQ5vHVIlmT50ZB8efwejkgXBkp9uYgb13ZAGwTr](https://developers.facebook.com/tools/debug/accesstoken/?access_token=EAAQjPJoqXKIBOyVg8I76qZAzSY3WWocO2DVZAiNLLOoITuUVBYMqU3ZBJCgoh14nM434Acrn6nkhInVGBuuE18Iz6A1dYRJRQ82pUoZBONUQgQ3gCgh7P3WZCoVUPh395HV7jV0k9zW2xR0aktK7BZBZAQbiL0MQ5vHVIlmT50ZB8efwejkgXBkp9uYgb13ZAGwTr)|



Chat gpt sanders api key


#### Conclusion
API for sending message: [Text - Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/messages/text-messages)
[Glitch :](https://glitch.com/edit/#!/quanta-squire-py)
