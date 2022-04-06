All Zuora API requests occur in a test or live environment. API objects in one environment (for example, <span style="text-decoration:underline;">Product</span> objects) aren't accessible in your other environments.

Different Zuora environments have different base URLs. You can use environment-based variables to manage base URLs and the different credentials you have for each environment.

When using a client library you should select the endpoint base URL you want to use:


| **TYPE**           | **WHEN TO USE**                                                                     | **HOW TO USE**                                                                                        | **BASE URL**                      |
|--------------------|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-----------------------------------|
| US Sandbox         | Use this environment as you build your application.                                 | Use test credit cards and accounts. Don’t use actual payment methods, payments or authorizations.     | https://rest.na.zuora.com         |
| US Central Sandbox | Use this environment for UAT and performance testing with product-level data loads. | Use test credit cards. Don’t use actual payment methods, payments or authorizations.                  | https://rest.sandbox.na.zuora.com |
| US Production      | Use this environment when you’re ready to launch.                                   | Use valid credit cards and accounts. Use actual payment methods, payments and payment authorizations. | https://rest.test.zuora.com       |
| EU Sandbox         | Use this environment as you build your application.                                 | Use test credit cards and accounts. Don’t use actual payment methods, payments or authorizations.     | https://rest.sandbox.eu.zuora.com |
| EU Central Sandbox | for UAT and performance testing with product-level data loads.                      | Use test credit cards. Don’t use actual payment methods, payments or authorizations.                  | https://rest.test.eu.zuora.com    |
| EU Production      | Use this environment when you’re ready to launch.                                   | Use valid credit cards and accounts. Use actual payment methods, payments and payment authorizations. | https://rest.eu.zuora.com         |


If you do not have a Zuora tenant, go to [https://www.zuora.com/resource/zuora-test-drive](https://www.zuora.com/resource/zuora-test-drive) and sign up for a test drive.

Go to the [Zuora Developer Community](https://community.zuora.com/communities/community-home?CommunityKey=e2a932b4-50c4-4019-a3e8-362e38714df3) to connect with other developers, report issues or discuss these samples.