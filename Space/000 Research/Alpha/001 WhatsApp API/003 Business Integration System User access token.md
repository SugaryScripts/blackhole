# Main
WaBa and then webhooks

[WhatsApp Business Platform](https://developers.facebook.com/docs/whatsapp/), consist 3 primary app:
- Cloud API, hosted by META      | default choose this
- [On-Premises API](https://developers.facebook.com/docs/whatsapp/on-premises)                 | Deploy with docker
- Business Management API       | is required regardless of which u choose
[Get Started - WhatsApp Business Management API](https://developers.facebook.com/docs/whatsapp/business-management-api/get-started/#business-integration-system-user-access-tokens)
	- [[003-001 Setup WhatsApp Business Platform]]

[Get Started - Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/get-started)

#### 


# Read More
url:: [Get Started - WhatsApp Business Management API](https://developers.facebook.com/docs/whatsapp/business-management-api/get-started/#business-integration-system-user-access-tokens)
### Business Integration System User Access Tokens

Business Integration System User access tokens are scoped to individual onboarded customers and should be used by Tech Providers and Solution Partners when accessing onboarded customer data.

> HIGHLIGHT
These tokens are useful for apps that perform programmatic, automated actions on customer WhatsApp Business Accounts, without having to rely on input from an app user, or requiring future re-authentication.

To generate a Business Integration System User access tokens, you must implement Embedded Signup (configured with Facebook Login for Businesses) and exchange the code returned to you when a customer completes the flow.

See the [Embedded Signup](https://developers.facebook.com/docs/whatsapp/embedded-signup) document and the [Business Integration System User access tokens](https://developers.facebook.com/docs/facebook-login/facebook-login-for-business#business-integration-system-user-access-tokens) document to learn more about these tokens and how they are generated.