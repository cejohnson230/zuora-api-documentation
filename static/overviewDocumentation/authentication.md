The Zuora API uses OAuth tokens to authenticate requests. You can view and manage the client credentials the API libraries use to generate these tokens for you in Zuora Central.

Take the following steps to create authentication credentials and add them to your server-side code:



1. Create a dedicated user for making API calls. See [Create an API user](https://knowledgecenter.zuora.com/Billing/Tenant_Management/A_Administrator_Settings/Manage_Users/Create_an_API_User) for details. This step must be performed by a Zuora administrator from your organization who has a company email address.
2. Create an OAuth client for the user. This step must be performed by an administrator.
    1. In Zuora, navigate to Settings > Administration > Manage Users, and click the user name (in hypertext) that is created in step 1.
    2. In the New OAuth Client section on the user profile page, enter a client name, and click create. A new window will open showing the client ID and client secret.
    3. Note down the client ID and client secret. You’ll need them to configure your client. This is a one-time process. See Create an OAuth client for a user for details.
3. Configure the library with your keys so that it can make requests to the Zuora API.

**Java**
```
String CLIENT_ID = System.getenv("CLIENT_ID");

String CLIENT_SECRET = System.getenv("CLIENT_SECRET");

String ENDPOINT = System.getenv("ENDPOINT_BASE");

ZuoraClient zuoraClient = new ZuoraClient(CLIENT_ID, CLIENT_SECRET, ENDPOINT);
```
To protect your tenant from unauthorized access be sure not to share your credentials in publicly accessible areas such as GitHub or client-side code.

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.