<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Memberships APIs

**Membership**

Customers purchase memberships for services performed. Memberships
consist of discounts, recurring services, and accounting settings.
Memberships can last for a fixed amount of time or they can be ongoing.
They can be billed upfront, monthly, quarterly, every other month,
biannual, and annually. 

[Membership Types]{.underline}---The template used when a membership is
sold to a customer. Users set up the discounts, recurring services, and
other settings that the membership will have.

[Customer Memberships]{.underline}---A single instance of a membership
type on a customer's record. Customer Memberships inherit the settings
of a membership type but can be customized if needed.

[Recurring Service Types]{.underline}---The template used when a
recurring service is created for a location. Users set up the job
details and how often the recurring service events will take place on a
membership. 

[Location Recurring Services]{.underline}---A single instance of a
recurring service type on a location record. Typically created when a
membership is sold but can also be added directly to a Location. They
inherit the settings of a recurring service type but can be customized
if needed.

[Recurring Service Events]{.underline}---They are created based on the
frequency details of a service location's recurring services. They are
booked into jobs or associated with already existing jobs. 

Pricebook items set up as sale or renewal tasks are added to an estimate
to initiate a membership. As soon as a sale or renewal task is added to
an invoice, that customer is a member. The customer is not considered a
member until the estimate is converted to an invoice. 

Customer memberships can be viewed on a customer record in ServiceTitan
and on the location records they apply to. A customer membership has to
be for one or all locations attached to a customer. If a membership is
ongoing, that membership does not need to be renewed because it will
last until the customer requests to cancel. If a membership is fixed,
that membership will expire after the defined amount of time and that
customer should be sold a renewal task to renew the membership.

Memberships utilize two different types of invoice templates. Billing
templates and recurring service templates. Billing templates are used to
bill a member on a set schedule. For example, if the membership is
monthly, ServiceTitan will reference a billing template to generate the
invoice every month. Recurring service invoice templates are used when
recurring service events are booked into jobs.

High level use cases for these APIs:

-   Get information about membership types or recurring service types

-   Get all memberships using deferred revenue

-   Get all recurring service types set to a particular duration type

-   Get key information about customer memberships, location recurring
    services, or recurring service events

-   Get all active customer memberships

-   Get all active customer memberships within a date range

-   Get all customer memberships that expire within a date range

-   Get all recurring service events in a particular status

-   Sell a membership

-   Create a membership sale invoice

-   Edit a customer membership or location recurring services

-   Update billing templates

-   Add or remove services from recurring service invoice templates\

</div>

</div>

</div>
:::

</div>
