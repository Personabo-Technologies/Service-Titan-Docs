<div>

::: section
<div>

<div>

</div>

<div>

<div>

# V1 & V2 API payload differences

**I see that a lot of information has been removed from jobs and
projects, and a) an ID is returned instead or b) no information is
returned at all in V2s. What should I do ?**

It\'s likely this information can be found elsewhere. Very little
information was completely removed from our APIs.

If an ID is returned in the response, there\'s a corresponding endpoint
which can give you details based upon that ID. For example, if Job Type
is returned as an ID on the jobs response. There\'s a new Job Type
endpoint which can give you the details like the name, etc.

If a field was returned in V1 that is no longer returned in V2, it\'s
likely there\'s a different endpoint you can use to get the same
information. For example, if you\'re looking for a job\'s invoice, the
invoice endpoint accepts job ID as a parameter even though invoice ID is
not part of the jobs response anymore.

**I used to be able to get key details from a job's history in the GET
Jobs/id. Where\'s this information now?**

There\'s a Job history endpoint where you can get the details you\'re
looking for.

**I used to be able to get a lot of information about the job, including
but not limited to invoices, estimates, campaigns, job types, customers,
and locations from the GET jobs endpoint. How do I get this information
now?**

The jobs endpoint only returns job-specific information now. If an ID is
returned instead of the information you want, use the appropriate
endpoint to get details using that ID. Many endpoints also accept job ID
as a parameter. For example, for invoice details, use the invoice
endpoint and use job ID as a parameter. For endpoints that do not accept
job ID, use the endpoint-specific ID provided in the jobs response and
use the desired. For example, for campaigns use the campaign ID provided
in the jobs response in the campaign endpoint to get additional campaign
details

**How do I find all the jobs on a project ?**

The project\'s endpoint no longer returns job-related information. Use
the jobs endpoint and the project parameter to get a list of all the
jobs associated with a project. You can also use the appointments
endpoint and pass it a project ID if you\'re looking for all of the
appointments from a job that is part of a specific project..

**How do I find all the estimates or invoices from a project ?**

For the estimate and invoice endpoints, you can pass it a project
parameter.

**How do I reschedule a job ?**

To change the date and time of a job, use the appointments endpoint. Use
the specific appointment ID that you want to change.

**How do I assign or un assign a technician from a job ?**

If you\'re assigning or un assigning technicians after the job has been
booked, use the assign endpoint. Indicate which Appointment ID you\'re
trying to assign/un assign.

**How do I know who is assigned to each job and appointment and their
splits ?**

Use the appointment assignments endpoint to know who is assigned to each
job\'s appointment. You can use appointment ID or job ID as parameters.
For splits, use the job splits endpoint and the job ID parameter.

**What are the changes made to Customers, Locations endpoints when
modified filters are used?**

If \"Modified On or After\", and \"Modified Before\" with GET /Customers
and GET /Locations are used: The V2 GET /Customers no longer return
results when a Customer\'s Contacts, nor when a Customer\'s Memberships,
have been updated.  Use the appropriate Contacts and Memberships
endpoints for this information. The same applies to GET /Locations as
well.

\
\

### 

</div>

</div>

</div>
:::

</div>
