<div>

::: section
<div>

<div>

</div>

<div>

<div>

# Accounting APIs

**Invoices  **

Invoices detail where the work was performed, the customer the work was
performed for, what work was performed, or what goods were sold, as well
as how much the customer has agreed to pay. ServiceTitan also provides
other details like general ledger account mapping. 

[Job invoices]{.underline}---The most common type of invoice in
ServiceTitan. A job invoice is generated the moment a job is booked. Job
invoice details are added by a technician using the ServiceTitan mobile
app or by an office employee. Job invoices details can transfer from
estimates that have been sold and converted to a job. 

[Membership invoices]{.underline}---Membership invoices details the
actions taken on a membership. A membership invoice is dependent on what
is agreed to in a membership and where in the life of the membership a
user is taking the action. Membership invoice types include:

-   Sales invoice---Records the sale of a membership and activates the
    membership. 

-   Billing invoice---Records the recurring subscription charge for a
    membership. For example, a monthly payment on a 12-month membership.

-   Service invoice---Records the work performed by a technician as part
    of the membership agreement.

-   Balance cancellation invoice---Records the unperformed work that is
    no longer expected to be completed. Balance cancellation invoices
    are not refunding the customer for any money collected for the
    membership. This type of invoice is generated when a membership
    expires or when a customer cancels services.

-   Refund invoice---Records the unperformed work that is no longer
    expected to be completed. Refund invoices are refunding the customer
    for money collected for the membership. This type of invoice is
    generated when a membership expires or when a customer cancels
    services.

[Point of sale invoice]{.underline}---Record sales made from within the
business and carry no association to a service location or a job.  

[Project invoice]{.underline}---Used to charge a customer for work
performed across multiple jobs at the same location. Project invoices
are often sent out at different points during a project.

[Financing invoice]{.underline}---Used to record work performed for a
customer when a different party is responsible for payment. Financing
invoices consist of two invoices:

-   One records the work performed by a technician at a specific
    location

-   The second transfers the balance owed to the party responsible for
    payment 

[Refund invoice]{.underline}---Write off revenue and return the payment
that was previously recorded by another invoice.

[Balance write-off invoice]{.underline}---Clear outstanding balances on
an existing invoice where it's no longer expected for the customer to
pay.

\
High level use cases for these APIs:

-   All invoice types can be requested from the same API endpoint.
    However, the information returned may vary depending on the workflow
    the invoice type relates to. 

-   Get, create, and update invoices and invoice details

-   In some circumstances, users can delete certain invoice details.

**Payments**

Payment details include basic information like payment method, the
invoice the payment is applied to, and how much the customer is paying.
ServiceTitan also provides other details like general ledger (GL)
account mapping.

[Due on receipt payments]{.underline}---A payment collected at the same
time work is performed. The invoice these payments are applied to
typically have no term applied or a term similar to Due Upon Receipt. 

[Membership billing payments]{.underline}---A payment collected at the
same time a membership billing invoice is generated in the office.
Memberships must be configured to generate membership payments and
customer payment information, such as credit card information, must be
stored in ServiceTitan.

[Term payments]{.underline}---A payment collected from the customer
after work was completed. These payments carry term conditions such as
when payment is due. These payments can be recorded by an office user,
or via statements that were sent to the customer.

[Deposits]{.underline}---A payment collected from a customer before work
is done. 

[Unapplied payments]{.underline}---A payment collected from a customer
that has not yet been applied to an invoice. 

[Multi-invoice payments]{.underline}---A payment collected from a
customer that is then applied to more than one invoice. 

[Refund payments]{.underline}---A payment where money is given back to a
customer after it was collected. Refund payments are used to capture
actions like refunding for a price adjustment, refunding due to an
escalation, or refunding an overpayment balance. 

High level use cases for these APIs:

-   All payment types can be requested from the same API endpoint.
    However, the information returned may vary depending on the workflow
    the payment type relates to. 

-   Get, create, and update payments and payment details.

**Payment terms**

Payment terms are agreements between a customer and vendor in regards to
how payment is made. Payment terms can be attached to invoices and bills
to notify both the business and the customer when payment is due.

\
High level use cases for these APIs:

-   Query payment terms details

    -   Creation of any new payment term must be done in ServiceTitan

    -   Payment term details will appear in the response when an invoice
        or bill transaction is queries

</div>

<div>

**Bills**

A document listing the amounts owed to a supplier by the recipient is
known as a vendor invoice. A supplier prepares and issues an invoice
when a customer orders goods and services on credit.

Vendor invoices include the amounts owed, sales taxes, freight and
delivery charges, the date by which the payment should be made, and
where to send the payment.

Things to know:

-   Bills are commonly tied directly to a purchase order and are
    generated when items on the purchase order are received

-   Bills cannot be updated through API. The corresponding purchase
    order can be updated, which will result in a new bill reflecting the
    changes

High-level use case for these APIs:

-   Retrieve information about bills

**Tax Zones**

Details of a tax zone vary by the location of customers, as well as the
types of work a business offers.Tax zones are commonly added to a
customer location, then automatically added to the invoice. 

High level use cases for these APIs:

-   Query tax zone details like the name of the tax zone and the tax
    rate

    -   Creation of any new tax zones must be done in ServiceTitan

    -   Tax zone details will appear in the response when an invoice
        transaction is queried

</div>

</div>

</div>
:::

</div>
