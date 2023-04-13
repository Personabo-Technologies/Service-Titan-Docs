<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Sales & Estimates APIs

**Estimates**

Before any work is done on a job, an estimate is built. Estimates
consist of different items from a user's pricebook such as services,
equipment, and materials. If a customer accepts an estimate then the
status of the estimate will be updated to Sold and the appropriate
person will get credit for the sale. One or multiple estimates can be
provided depending on the situation.

[Services]{.underline}---Services are what technicians are doing while
on a job. For example, replacing a capacitor or installing an emergency
valve.

[Materials]{.underline}---Materials are the items used by a technician
to complete a service. In the previous example the materials would be
the capacitor and the emergency valve.

[Equipment]{.underline}---Large ticket items that will be installed. For
example, condensers or furnaces are equipment.  

[Status]{.underline}---Status is used to track where the estimate
stands. Whether it has been sold, dismissed, or still open.

[Sold By]{.underline}---Sold by keeps track of which managed technician
sold the estimate. Unmanaged technicians cannot sell estimates.

When a technician arrives at a location, they will diagnose the issue
then add items to an estimate, or estimates. Customers can accept or
decline the estimate. If the customer accepts and the technician can do
the work quoted at that time then they will perform the work on the same
job. If they do not have the ability/parts then another job will be
booked by a CSR to perform the work quoted at a later time. If an
estimate is not accepted it can be followed up on at a later time. If,
when following up, it is determined a sale cannot be made the estimate
is dismissed. 

High level use cases for these APIs:

-   Add an estimate to a job

-   Add items to an estimate

-   Mark an estimate as sold

    -   A managed technician sold by is required when performing this
        request

    -   If marked as sold via API then it will automatically be marked
        to perform work later and a CSR will have to book the job

-   Mark an estimate as dismissed

-   Unsell an estimate

    -   Can only unsell if no signature has been collected and if the
        estimate hasn't been booked out into a job

-   Retrieve a list of all estimates by these filters:

    -   Job Id

    -   Sold By

    -   Status

    -   Sold On Date Range

    -   Total Amount Range\

</div>

</div>

</div>
:::

</div>
