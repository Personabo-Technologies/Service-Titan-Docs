<div>

::: section
<div>

<div>

</div>

<div>

<div>

# V2 API and Webhooks

**What\'s new in V2 APIs and why should I use them ?**

We are making many exciting changes and a few key ones are below:

-   We are introducing OAuth 2.0 Client Credentials: Machine-to-Machine
    grant type. This new design standard would give you (as a resource
    owner of the data) more control over how you want to allow apps to
    access your resources. If you like the level of access the app
    requests, you can enable and share your Client ID and Secret Key.
    ServiceTitan admins within your organization can enable and disable
    Client IDs and Secret Keys.

-   We are introducing a new app key---once you create your application
    on the developer portal and choose the API scopes your application
    wants, your app key is generated. 

-   We are eliminating the concept of API keys which existed in V1. Now
    you need a Client ID, Secret Key and an app key to make a successful
    API call. 

-   We are introducing a new developer portal, which will be the hub for
    application developers. The developer portal will have all the tools
    required for a successful integration. It includes documentation and
    API references with all required API attributes, try-it-out
    functionality to send a mock request instantly(coming soon), and an
    app creation flow.

-   We are realigning the payloads of some APIs. The data you are
    currently getting through one API might be moved to another API
    endpoint. This means you will continue to get the same data but
    through a different API call. We are doing this to improve
    performance and security.

-   We are offering new integration environment which is an equivalent
    to a sandbox environment for development and pre-production testing
    activities. 

    Note: We will be sunsetting V1 APIs by the end of July 2022. So you
    should migrate to V2 APIs by then to avoid interruption.

\
**What\'s required to make a successful API call ?**

You need your app key generated from the integration or production
environments. App keys are NOT environment specific. 

You need to obtain an environment specific Client ID and Secret Key from
the ServiceTitan admins in our customer's organization. For making calls
in the integration environment you need to obtain a Client ID & Secret
Key generated in the integration environment. 

For making calls in the production environment you need to obtain a
Client ID & Secret Key generated in the production environment. 

**I am currently subscribed to webhooks. What is the impact?**

There is no impact on your current subscription to web hooks and how you
are receiving events through them. You will continue to receive the
events uninterrupted without you having to make any changes. However, if
you are taking subsequent actions such as calling V1 API endpoints after
receiving the event, you should migrate to calling the V2 API endpoints.
V1 APIs will be sunsetting in July 2022. Please see the V1 sunset
section of FAQs for more information.

**Are you planning to launch V2 webhooks?**

 It\'s one of our roadmap items and we are working on it. We will keep
you posted when we get there. Currently there is no established ETA. 

**Can I still subscribe to the existing version of webhooks?**

At the moment we are restricting new subscriptions to the current
version of webhooks. You have to wait for a few months until we launch
the new V2 webhooks. If you have already subscribed you should not have
any impact and will continue to receive the events. 

**Are you implementing any rate limiting on API calls ?**

Yes. Our current default is 60 calls per second per application. Please
contact us if you have any concerns about this. We will evaluate on a
case by case basis.

**I don\'t see all the V1 APIs present in V2 yet. When are the remaining
APIs releasing ?**

</div>

<div>

<div>

<div>

<div>

**Endpoints**

</div>

</div>

<div>

<div>

**Integration environment availability**

</div>

</div>

<div>

<div>

**Production environment availability**

</div>

</div>

<div>

<div>

Invoices, Payments, Payment Terms, Payment Types, Tax Zones, Leads,
Tags, Technician Shifts, Capacity, Appointment Assignments, Installed
Equipment, Vendors, Purchase Orders, Call Reasons, Jobs, Appointments,
Job Cancel Reasons, Job Hold Reasons, Job Types, Projects, Campaigns,
Campaign Costs, Membership Types, Customer Memberships, Recurring
Service Types, Recurring Services, Recurring Service Events, Invoice
Templates, Timesheet Codes, Activity Codes, Job Splits, Payroll
Adjustments, Payrolls, Technician Payrolls, Employee Payrolls, Gross Pay
Items, Materials, Services, Equipment, Categories, Discounts and Fees,
Estimates, Employees, Technicians, Business Units,Task Management Data,
Tasks, Calls

</div>

</div>

<div>

<div>

Currently available

</div>

</div>

<div>

<div>

Currently available

</div>

</div>

<div>

<div>

Inventory Bills, Bookings, Customers, Locations, Tag Types, GPS Pings,
Zones, Non-Job Appointments, Adjustments, Returns, Transfers, Receipts

</div>

</div>

<div>

<div>

Currently available

</div>

</div>

<div>

<div>

Currently available

</div>

</div>

</div>

</div>

</div>

</div>
:::

</div>
