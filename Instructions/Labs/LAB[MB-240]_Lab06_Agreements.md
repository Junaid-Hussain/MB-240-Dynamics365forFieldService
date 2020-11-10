---
lab:
    title: 'Lab: Agreements'
    module: 'Module 6: Field Service Agreements'
---

Module 6 - Field Service Agreements
=====================
## Practice Lab 6 - Agreements

## Scenario
Worldwide Industries (WWI) provides IT and networking services to their
customers. Their services range from phone system and network installations to
telephoning systems and security system installations. They are going to be
leveraging Dynamics 365 for Field Service for installation and servicing of
these systems for their customers. You are the system implementer that has been
tasked with configuring the application to support the roll-out of the
application. You will be adding and configuring some products that can be
installed and setting up skills and characteristics that will be used as part of
the implementation.

Exercise 1 - Create an Agreement 
================================

In this exercise you will be defining a preventative maintenance agreement that
will generate Work orders monthly and quarterly. Additionally, the customer will
be billed at the end of each month with a Monthly Printer Maintenance fee.

## Task 1 - Create an Agreement to be used for Preventative Maintenance 

1.  In Dynamics 365, navigate to **Field Service**

2.  Click the Site Map in the bottom left and select Service, select **Agreements** under the **Service Delivery** heading.

3.  Click **New** from the Command Bar.

4.  Select **[your prefix ex. mollyc]+ Account** for the **Service Account**.  If you do not see your Account, create a new Account with name *[your prefix ex. mollyc]+ Account*

5.  Under Details set the fields as follows:

    - **Start Date:** Today’s Date

    - **End Date:** 1 Year from Today

6.  Set the **Price List** to **Default Price List** and **Taxable** to **No**.

7.  Click the **Save** to save the agreement and leave it open.

## Task 2 - Setup an Automated Booking for the Agreement

1.  In the agreement that you just created, click on the **New Agreement Booking Setup** button in the
    Booking Setups area.

2.  Configure the Agreement Booking as follows:

    - **Name:** [your prefix ex. mollyc]+ Monthly Printer Service

    - **Auto Generate Work Order**: Yes

    - **Work Order Type:** Service Call

    - **Auto Generate Booking**: No

    - **Estimated Duration:** 1 Hour

    - **Pre Booking Flexibility:** 1

    - **Post Booking Flexibility:** 1

    - **Time Window Start:** 9:00 AM

    - **Time Window End:** 12:00 PM

    - **Generate Work Order Days in Advance**: 2 (to ensure that the work
        order is created right away, determine how many days are left in the
        current month, and use that number or greater for this value)

3.  Save the record and leave it open.

4.  Under **Incidents,** click **New Agreement Booking Incident.**

5.  Select **Service Printer** for Incident Type and click **Save & Close.**

6.  On the Agreement Booking Setup Record, click the ellipsis and select **Booking Recurrence**.

7.  Set the Recurrence Patten as noted below:

    - **Monthly:** on the 1st day of every One Month

    - Start on the 1st day of Next Month

    - End After 12 Occurrences

8.  Verify the changes have saved, and close the Booking Setup Record.

9.  In the agreement that you just created, click on the **New Agreement Booking Setup** button in the
    Booking Setups area.

10. Configure the Agreement Booking as follows:

    - **Name:** [your prefix ex. mollyc]+ Quarterly System Check

    - **Auto Generate Work Order**: Yes

    - **Work Order Type:** Service Call

    - **Generate Work Order Days In Advance:** 5

    - **Priority:** Moderate

    - **Auto Generate Booking**: No

    - **Estimated Duration:** 30 Minutes

    - **Pre Booking Flexibility:** 2

    - **Post Booking Flexibility:** 4

11. Save the record and leave it open.

12. On the Agreement Booking Setup Record, click ellipsis and select **Booking Recurrence**.

13. Set the Recurrence Patten as noted below:

    - **Monthly:** on the 1st day of Every 3 Month

    - Start on the 1st day of Next Month

   - End After 12 Occurrences

14. Verify the changes have saved and close the Booking Setup Record.

15. Locate **the Invoice Setups** Sub-grid, and click the **New Agreement Invoice Setup** button to
    create a new Invoice setup

16. Enter *[your prefix ex. mollyc]+ Monthly Invoice* for the Name, and Click Save

17. If Necessary, expand Invoice Products, click the ellipsis and select **New Agreement Invoice Product** button to add
    Invoice Products

18. Complete the Agreement Invoice Product as follows:

    - **Product:** [your prefix ex. mollyc]+ Monthly Printer Maintenance

    - **Unit:** Primary Unit

    - **Quantity:** 1

    - Click **Save and Close**

19. Close the [your prefix ex. mollyc]+ Monthly Invoice record

20. Return to the Agreement. Change the Agreement System Status from Estimate to
    **Active** and **Save**.
