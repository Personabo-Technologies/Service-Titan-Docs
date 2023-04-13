<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Create an Application, API scopes and an App key

Login to My Apps tab on the dev portal. From here you can manage your
existing apps, add new apps, choose the API scopes, add tenant IDs for
anyone you want to make your app visible to and subscribe to and
generate an app key. 

[New apps]{.underline}

To add new apps: 

1.  Click New Apps. 

2.  Enter an application name, organization name, the home page URL of
    your organization and Tenant IDs. \

</div>

<div>

[Add Tenant IDs]{.underline}

You should add tenant IDs of the customers (a.k.a tenants) that you want
to make your app visible. You can add/delete tenant IDs anytime. Every
ServiceTitan customer will have at-least one tenant ID. If you do not
know your tenant ID, please reach out to your ST admin with your
organization.

[API scopes]{.underline}

Choose the list of API scopes that your application uses. Your app can
use View or Modify or View and Modify as options. The scopes that you
have selected will be displayed to the app subscriber also known as a
resource owner who can be the ServiceTitan admin of your organization.
This admin after viewing the app details and API scopes, can generate
and share the Client ID and Secret Key with your app.

Note: API scopes are not editable after saving and generating an
application key. If you want to modify your API scopes, then you must
click add new apps and follow the steps to add the app as new.

[App key]{.underline}

After completing the steps to add a new app, your application key will
be generated. ServiceTitan identifies your application by the app key.
You need to embed the application key into your app and pass it along
with an access token to make a successful API call.

Note: App key is not environment specific. Your app key generated in the
integration environment works for production calls and vice versa. ** **

[Delete Application]{.underline}

If you delete an application, your app key also gets deleted and
ServiceTitan will no longer identify your app.

\
\
\

\

</div>

</div>

</div>
:::

</div>
