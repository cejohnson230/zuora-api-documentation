All top-level API resources have support for bulk fetches via "list" API methods. For instance, you can list accounts, list subscriptions and list billing documents. These list API methods share a common structure, taking an optional cursor parameter: cursor.

Zuora uses cursor-based pagination via the cursor parameter. The cursor parameter takes the `end_cursor` value returned in the response returned from a previous request. Objects are returned, by default, in reverse chronological order. 

**Parameters**

cursor optional 

A cursor for use in pagination. cursor defines your place in the list. For instance, if you make a list request and receive 100 objects, with `end_cursor="76683efa-4b25-4716-a5c1-852b2162fcdb"`, your subsequent call can `include cursor= "76683efa-4b25-4716-a5c1-852b2162fcdb"` in order to fetch the next page of the list.

**List Response Format**

data array

An array containing the actual response elements, paginated by any request parameters.

`end_cursor` string

A cursor you can use to fetch the next page of the list.