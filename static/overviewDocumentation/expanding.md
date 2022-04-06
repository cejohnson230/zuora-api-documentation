Many objects allow you to request additional information as an expanded response by using the expand request parameter. This parameter is available on all API requests, and applies to the response of that request only. Responses can be expanded in two ways.

In many cases, an object contains the ID of a related object in its response properties. For example, a Billing Document will have an associated Account ID. Those objects can be expanded inline with the expand request parameter. 

In some cases, such as the Invoices associated with an Account object, there is related information that is not included in responses by default. You can request these fields as an expanded response by using the expand request parameter. 

You can expand recursively by specifying nested fields after a dot (.). For example, requesting <code>billing_document.payment_method</code> on an account will expand the billing documents attribute into a list of full Billing Document objects, and will then expand the <code>payment_method</code> attribute on those billing documents into a full Payment Method object.

You can use the expand param on any endpoint which returns expandable fields, including list, create, and update endpoints.

Expansions on list requests start with the data property. For example, you would expand data.accounts on a request to list payment methods and associated customer accounts. 

Expansions have a maximum depth of four levels (so for example, when listing payments, <code>data.billing_document.subscription.payment_method</code> is the deepest allowed).

Finally, you can expand multiple objects at once by identifying multiple items in the expand array.

Related Guide: <span style="text-decoration:underline;">Expanding responses</span>.