<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Inventory APIs

**Inventory**

In order to record the purchase of items for business use, a purchase
order must be created within ServiceTitan. A purchase order records that
items were ordered from a vendor, to be shipped to a location.** **

[Vendors]{.underline}---The vendor or supplier of what was purchased

[Purchase Orders]{.underline}---The record of the purchase. Records that
items were ordered from a vendor, to be shipped to a location.

Purchase orders are assigned a purchase order type, and the costs are
booked against a specific business unit, which are used for
categorization and reporting. A purchase order can be associated with a
specific job, project, and technician to facilitate additional
reporting. Once created, a purchase order will proceed through various
statuses as it is sent and subsequently fulfilled, in whole or in part,
by the vendor.

Each purchase order is associated with a specific vendor. Each vendor
must be configured with their main address. A vendor can be configured
with the contact information of a primary contact, default settings for
the applicable tax rate, and how purchase orders are to be delivered.

Things to know:

-   Vendors, business units, and inventory locations must be configured
    before a purchase order can be associated with them

-   Jobs, projects, and technicians must be created before the purchase
    order can be associated with them

-   Purchase orders are created in Pending status.

-   A purchase order status cannot be updated through API. The current
    status can be retrieved as part of the GET call payload.

-   Once a purchase order has been exported from ServiceTitan to an
    accounting system, it can no longer be edited.

\
High level use cases for these APIs:

-   Retrieve information about vendors

-   Create a vendor

-   Retrieve information about purchase orders, including their current
    status

-   Create a purchase order\

</div>

</div>

</div>
:::

</div>
