Zuora uses conventional HTTP response codes to indicate the success or failure of an API request. In general: Codes in the 2xx range indicate success. Codes in the 4xx range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a payment attempt failed, etc.). Codes in the 5xx range indicate an error with Zuora's servers.

Some 4xx errors that could be handled programmatically include an error code that briefly explains the error reported.

Attributes

**type** enum

**code** string

For some errors that could be handled programmatically, a short string indicating the error code reported.

**message** string

A human-readable message providing more details about the error. 

**param** string

If the error is parameter-specific, the parameter related to the error. For example, you can use this to display a message near the correct form field.

Related guide: <span style="text-decoration:underline;">Error Handling</span>.