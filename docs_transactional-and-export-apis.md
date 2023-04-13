<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Transactional APIs & Data Export APIs

ServiceTitan has two sets of APIs to solve the consumer use cases
better. Historically ST supported only Transactional APIs and now we are
adding new Data Export APIs. 

**Transactional APIs:** The Transactional API is a lightweight API. It
is meant for moving targeted, small loads of data in and out of
ServiceTitan.

HTTP methods supported: GET, PUT, POST, DEL, PATCH

When to use Transaction APIs:

-   When you have to create, update and delete data.

-   When you have to pull small amounts of data out of ServiceTitan. Say
    for a limited time interval and or when you want to apply filters.

**Data Export APIs:** When you want to pull loads of data out of
ServiceTitan frequently. The URL structure will have /export in the path
to indicate that it is a data export API.

Example: GET /memberships/v2/tenant/{tenant}/export/recurring-services

 HTTP methods supported: GET 

When to use Data Export APIs:

-   When you want a full snapshot of the data and refresh it as
    frequently as you want. These APIs will return active, inactive,
    deleted data with no filters applied and for more historical data
    pull outs from ServiceTitan. 

-   When you have data warehousing needs using these APIs will be more
    efficient. 

Note: Only few highly adopted APIs have these data export endpoints and
not all. When there is no data export API, you can use the regular GET
endpoints as needed. We will periodically keep adding new data export
endpoints as needed. 

</div>

</div>

</div>
:::

</div>
