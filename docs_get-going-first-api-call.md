<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Make your first API call

**We recommend you develop and test in the Integration environment 
before switching to production. **

[Steps to make a successful API call]{.underline} 

First your application should call the ServiceTitan OAuth API and passes
Client ID & Secret Key for authorization. If the authorization is
successful, you will get back an access token. 

Next your application should call the resource API endpoint and pass the
access token along with the app key. If the validation is successful,
then your GET/PUT/POST/DELETE operation will be successful. 

\
[HTTPS protocol]{.underline}

All ServiceTitan API resources are protected by Secure Sockets Layer
(SSL) encryption. Any call you make to a ServiceTitan API resource must
use the HTTPS scheme in the URL. SSL establishes an encrypted link
between the ServiceTitan resource server and your application. This link
ensures that all data passed between the resource server and your
application remains private.

**Using cURL to make your first ServiceTitan API Call**

The cURL command line tool below is used to retrieve an OAuth 2.0 access
token and make a simple call to the ServiceTitan API.

To obtain an access token\

1.  Make a call to the Auth token endpoint using a REST URL. You have to
    pass your ClientID and ClientSecret. Example REST URL format:
    https://auth-integration.servicetitan.io/connect/token

-   client_id

-   client_secret

-   grant_type---This should be  set to "client_credentials"Additional
    helpful information

[Example cURL command for retrieving an access token:]{.underline}\

</div>

<div>

<div>

<div>

<div>

*[Request:]{.underline}*

*curl \--request POST \\*\
*  \--url https://auth-integration.servicetitan.io/connect/token \\*\
*  \--header \'Content-Type: application/x-www-form-urlencoded\' \\*\
*  \--data grant_type=client_credentials \\*\
*  \--data client_id=%client_id% \\*\
*  \--data client_secret=%client_secret% \\*

*Running the above command returns a JSON block similar to the following
example:*

*[Response]{.underline}*

\
*{*

*  \"access_token\":
\"eyJhbGciOiJSUzI1NiIsImtpZCI6IkM2QTRDMjA2MjE3OEYyMEI4NzkyNjg2MTJGNkMwNEE1NzUwRjU3NzdSUzI1NiIsInR5cCI6ImF0K2p3dCIsIng1dCI6InhxVENCaUY0OGd1SGttaGhMMndFcFhVUFYzYyJ9.eyJuYmYiOjE2MjkxNDYyODksImV4cCI6MTYyOTE0NzE4OSwiaXNzIjoiaHR0cHM6Ly9wdWJsaWMtYXBpLWF1dGguc3QuZGV2IiwiY2xpZW50X2lkIjoiY2lkLjl2Ym9hNXRiYmEzMGpuaXN6ZG8wMWZ0NGwiLCJ0ZW5hbnQiOiI4NDUwIiwianRpIjoiNTRBNzM0RkJFNzBFQzU4Q0VFM0U3NUMxNjNDMUU0NjUiLCJpYXQiOjE2MjkxNDYyODksInNjb3BlIjpbInRuLmFjYy5pbnZvaWNlczpyIl19.coWQGRmbQmE9G-KADciVQeiXXoGm-g5y4_B79SUSYezCi6S7x3_W506vsCTPq7iPwEe5XGAofiWFEWf2v8CSq1cQJrIVVisHqTeygUbAYRBcj1iuNA6fCGvl72wY8uh0F_IzJ8UVp6Vdvklvupl3zelakJNVlmA0dSYtQnc9RN2whKNrqEuUDJRD5aYctAUv6z\_-WpedMueOfAn8iUXcxvgbS4vXc96aZQX-v-0VLS7ZE457Y-HMhEPPGZ5UV27CHrZd6ohyJ-GldI849SJsQnwPjjeyJqjF_bb9PpDqxzKyzeS1f_bptPNahwYmGFYWnqZNw4fHjIQFdmzHl_3BOw\",*

*  \"expires_in\": 900,*

*  \"token_type\": \"Bearer\",*

*  \"scope\": \"tn.acc.invoices:r\"*

}

</div>

</div>

</div>

</div>

<div>

[Making a call to the ServiceTitan Resource API ]{.underline}

Now that we have successfully retrieved an access token, we can use it
to make our first call to the ServiceTitan Resource API.

For this example, we'll use the simple
https://api-integration.servicetitan.io/accounting/v2/tenant/{tenant}/invoices
endpoint to show that we can successfully contact the ServiceTitan API
server and return information. Again, we'll use cURL to show this.

</div>

<div>

<div>

<div>

<div>

*[Request:]{.underline}*

*curl \--request GET \\*\
*\--url
https://api-integration.servicetitan.io/settings/v2/tenant/985798691/employees
\\*\
*\--header \'Authorization: \<access token\>\' \\*\
*\--header \'ST-App-Key: \<app key\>\'*

*Where \<access token\> is the string value for the access token we
retrieved in the previous step.*

\<app key\> is the application key (see Create an App).

*If we execute the above cURL command with a valid access token, it
returns a JSON block similar to this example:*

*Response:*

*{*

* \"page\": 1,*

*  \"pageSize\": 50,*

*  \"totalCount\": 1,*

*  \"hasMore\": false,*\
*  \"data\": \[*

*  {*

*\"id\": 1679,*

*\"syncStatus\": \"Pending\",*

*\"summary\": null,*

*\"referenceNumber\": \"1676\",*

*\"invoiceDate\": \"2021-07-19T00:00:00Z\",*

*\"dueDate\": \"2021-07-19T00:00:00Z\",*

*\"subTotal\": \"0.00\",*

*\"salesTax\": \"0.00\",*

*\"salesTaxCode\": null,*

*\"total\": \"0.00\",*

*\"balance\": \"0.00\",*

*\"customer\": {*

*   \"id\": 1673,*

*   \"name\": \"Customer\"*

*},*

*\"customerAddress\": {*

*   \"street\": \"801 North Brand Boulevard\",*

*   \"unit\": null,*

*   \"city\": \"Glendale\",*

*   \"state\": \"CA\",*

*   \"zip\": \"91203\",*

*   \"country\": \"USA\"*

*},*

*\"locationAddress\": {*

*   \"street\": \"801 North Brand Boulevard\",*

*   \"unit\": null,*

*   \"city\": \"Glendale\",*

*   \"state\": \"CA\",*

*   \"zip\": \"91203\",*

*   \"country\": \"USA\"*

*},*

*\"businessUnit\": {*

*   \"id\": 319,*

*   \"name\": \"Plumbing - Service\"*

*},*

*\"termName\": \"Due Upon Receipt\",*

*\"createdBy\": \"admin\",*

*\"batch\": null,*

*\"modifiedOn\": \"2021-07-19T20:35:38.2876004Z\",*

*\"adjustmentToId\": null,*

*\"job\": null,*

*\"projectId\": null,*

*\"royalty\": {*

*   \"status\": \"Pending\",*

*   \"date\": null,*

*   \"sentOn\": null,*

*   \"memo\": null*

*},*

*\"employeeInfo\": {*

*   \"id\": 21,*

*   \"name\": \"admin\",*

*   \"modifiedOn\": \"2021-06-22T16:23:12.9688553Z\"*

*},*

*\"commissionEligibilityDate\": null,*

*\"items\": null,*

*\"customFields\": null*

*  }*

*\]*\

</div>

</div>

</div>

</div>

<div>

**Additional helpful information**

[Working with cURL and Postman]{.underline}

You can use these popular web development test tools to explore the
capabilities of the ServiceTitan API without having to fully build out
your application. In the following sections, we use these tools to
illustrate how you can make your first call to the ServiceTitan API. If
you are unfamiliar with these tools, here are some helpful resources to
get you started:\

-   cURL

-   cURL GitHub Repository README

</div>

</div>

</div>
:::

</div>
