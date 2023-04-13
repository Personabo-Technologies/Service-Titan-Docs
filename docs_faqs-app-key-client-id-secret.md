<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Dev Portal, App key and Client ID & Secret Key

**How do I login to the My apps tab ? **

In order to login to the My Apps tab of the dev portal, your
ServiceTitan admin needs to establish you as a user in your
organization\'s integration environment or the production environment
instances. Once you are established with user credentials, you can use
those credentials to login to the My Apps tab. 

**How is the app key generated ?**

After you login to the My Apps tab of the dev portal, you will create an
app, add tenant IDs, and choose API scopes. Once these steps are
completed and saved, your app key is generated.

**Can I edit my API scopes ?**

No. Once you have selected your API scopes, and generated an app key,
you cannot modify the API scopes. If you want to change the API scopes,
you need to follow the process of creating an app again, choose the
modified API scopes and generate a new app key. 

**Who and how should the Client ID & Secret Key be generated ?**

User with admin permissions (that is who has to \'Manage API Application
Access\' permission) will review applications requesting access to the
resources and will generate a Client ID and Secret Key for that app and
then share it with the developer of that application.

**I** **am a ServiceTitan customer and have multiple tenants. Can a
single pair of Client ID & Secret work for all tenants ?**

No. Since Client ID & Secret Key are unique to each ServiceTitan tenant,
you need to obtain an application and tenant specific Client ID & Secret
Key from each tenant.

**Multiple ServiceTitan customers will use the app I am creating. Will
the same app key, Client ID and Secret Key work for all of them ?**

Since the app key represents the application, you can use the same key
for multiple customers/tenants. Since Client ID & Secret Key are unique
to each ServiceTitan tenant, you need to obtain an application and
tenant specific Client ID & Secret Key from the ServiceTitan admin of
each customer/tenant. For example, if you have an application that will
be used by 10 ServiceTitan customers/tenants, you need to obtain 10
Client IDs & Secrets Keys but can use the same app key. 

**Why are Tenant IDs added while creating an app ?**

As an application developer you need to add the Tenant IDs of the
customers whom you want to let to use your app. By adding Tenant IDs,
ServiceTitan admins at the customer organizations can discover your app
and would be able to generate and enable the Client ID & Secret Key and
share it with you. You can add any number of tenant IDs, and can add and
remove tenant IDs at any time even after the app has been created. 

**Does ServiceTitan follow OAuth 2.0 protocol ?**

Yes, with the advent of V2 APIs ServiceTitan now uses the OAuth 2.0
machine to machine client credentials grant flow.

**What are some other changes ?**

If \"Modified On or After\", and \"Modified Before\" filters are used
with GET /Customers and GET /Locations: The V2 GET /Customers no longer
return results when a Customer\'s Contacts, nor when a Customer\'s
Memberships have been updated. Use the appropriate Contacts and
Memberships endpoints for this information. The same applies to GET
/Locations

\

### 

</div>

</div>

</div>
:::

</div>
