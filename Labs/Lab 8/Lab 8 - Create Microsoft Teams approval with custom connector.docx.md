# **Lab 8: Create Microsoft Teams approval with custom connector**

### **Task 1: Setting up the API**

To review the API, follow these steps:

1.  Go to Contoso Invoicing, by navigating to the following link
    <https://contosoinvoicing.azurewebsites.net/>.

2.  To select the documentation link, click on **here** next to ‘You can
    find the API documentation’.

> ![A screenshot of a computer Description automatically
> generated](./media/image1.png)

3.  Review the available operations.

> ![A screenshot of a computer Description automatically
> generated](./media/image2.png)

4.  Close the documentation browser tab or window.

5.  Select the **Open API definition** link.

> ![A screenshot of a computer Description automatically
> generated](./media/image3.png)

6.  Copy the content from the page and save it on notepad as
    swagger.json. You'll use this file later in the exercise.

> ![Screenshot of an arrow pointing to the save as
> button.](./media/image4.png)
>
> ![A screenshot of a computer Description automatically
> generated](./media/image5.png)

7.  Close the definition browser tab or window.

8.  Select the **API Key** link.

> ![A screenshot of a computer Description automatically
> generated](./media/image6.png)

9.  Copy and save your API key to the notepad on your VM because you'll
    need it later.

> ![A screenshot of a computer Description automatically
> generated](./media/image7.png)

### **Task 2: Create a custom connector**

1.  Sign in to Power Automate using <https://make.powerautomate.com/>
    with your given admin tenant credentials.

> ![A screenshot of a computer Description automatically
> generated](./media/image8.png)

2.  Select **Contoso(default)** environment from environment selector.

> ![A screenshot of a computer Description automatically
> generated](./media/image9.png)

3.  In the left navigation pane, click on **More,** then click on
    **Discover all.**

> ![](./media/image10.png)

4.  Navigate to **Data**, under Data select **Custom connectors**.

> ![A screenshot of a computer Description automatically
> generated](./media/image11.png)

5.  On the **Custom connector** page, select **New custom connector**,
    and then **Create from blank** from the dropdown list.

> ![A screenshot of a computer Description automatically
> generated](./media/image12.png)

6.  In the **Connector name** field, enter **TeamsConnector** as name
    for the custom connector, and then select **Continue**.

> ![A screenshot of a computer Description automatically
> generated](./media/image13.png)

7.  In **General Information**, enter a **Description** as **Custom
    connector for Contoso Invoicing API** and a **Host** as
    **contosoinvoicing.azurewebsites.net**.

> ![](./media/image14.png)

8.  Select **Create connector**.

> ![A screenshot of a computer Description automatically
> generated](./media/image15.png)

9.  Don't navigate away from this page.

### **Task 3: Import the OpenAPI definition**

To import the OpenAPI definition, follow these steps:

1.  Select the arrow next to **Connector Name**.

> ![A screenshot of a computer Description automatically
> generated](./media/image16.png)

2.  Select the ellipsis (**...**) button of the connector and then
    select **Update from OpenAPI file**.

> ![A screenshot of a computer Description automatically
> generated](./media/image17.png)

3.  Select **Import**.

> ![A screenshot of a computer Description automatically
> generated](./media/image18.png)

4.  Select the **swagger.json** file that you downloaded in **Task
    1** and then select **Open**.

> ![A screenshot of a computer Description automatically
> generated](./media/image19.png)

5.  Select **Continue**.

> ![A screenshot of a computer Description automatically
> generated](./media/image20.png)

6.  Fill in the host URL
    as !!**contosoinvoicingtest.azurewebsites.net!!** and then
    select **Security**.

> ![A screenshot of a computer Description automatically
> generated](./media/image21.png)

7.  Notice that the fields are filled out from the imported file.

> ![A screenshot of a computer Description automatically
> generated](./media/image22.png)

8.  Don't navigate away from this page.

### **Task 4: Review and adjust definitions**

To review and adjust definitions, follow these steps:

1.  Scroll down on Security page and select the **Definition** tab.

> ![A screenshot of a computer Description automatically
> generated](./media/image23.png)

2.  Take a few minutes to review the operations that were imported.

3.  Notice the blue information circle next to **GetInvoice**.

> ![A screenshot of a computer Description automatically
> generated](./media/image24.png)

4.  Select the **GetInvoice** operation.

> ![A screenshot of a computer Description automatically
> generated](./media/image25.png)

5.  Notice that the operation indicates a missing **Summary**.

> ![A screenshot of a phone Description automatically
> generated](./media/image26.png)

6.  Enter **Get Invoice** as the **Summary** to improve the usability.

> ![A screenshot of a computer Description automatically
> generated](./media/image27.png)

7.  Notice the blue information circle next to
    the **PayInvoice** operation and that it indicates a
    missing **Description**.

> ![A screenshot of a computer Description automatically
> generated](./media/image28.png)

8.  Select **PayInvoice** operation.

> ![A screenshot of a computer Description automatically
> generated](./media/image29.png)

9.  Enter **Pay an invoice** as the **Description**.

> ![A screenshot of a computer Description automatically
> generated](./media/image30.png)

10. Delete both **NewInvoice** operations because you won't use them.

> ![Screenshot showing the delete action button.](./media/image31.png)

11. Select the **GetInvoiceSchema** operation.

> ![A screenshot of a computer Description automatically
> generated](./media/image32.png)

12. Modify the **Visibility** option to **internal** so that people
    don't see it in their action list and then select **Update
    connector**.

> ![A screenshot of a computer Description automatically
> generated](./media/image33.png)

13. Don't navigate away from this page.

### **Task 5: Test the connector**

To test the connector, follow these steps:

1.  Select the **Test** tab from the drop-down under the connector name.

> ![](./media/image34.png)

2.  Select **+ New connection**.

> ![A screenshot of a computer Description automatically
> generated](./media/image35.png)

3.  Paste in the **API Key** that you saved in **Task 1: Review the
    API** and then select **Create connection**.

> ![A screenshot of a computer Description automatically
> generated](./media/image36.png)

4.  Select the **Refresh** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image37.png)

5.  Select **ListInvoiceTypes | Test Operation**.

> ![A screenshot of a computer Description automatically
> generated](./media/image38.png)

6.  You should see the invoice types data in the body area.

> ![](./media/image39.png)

7.  Select **Close** to close the custom connector window.

> ![A screenshot of a computer Description automatically
> generated](./media/image40.png)

### **Task 6: Create an approval flow**

Now that you've created your custom connector, it's time to create your
approval flow that uses the custom connector.

1.  Sign in to Power Automate using <https://make.powerautomate.com/>
    with your given admin tenant credentials.

2.  Select **New flow**, and then select **Instant cloud flow**.

> ![A screenshot of a computer Description automatically
> generated](./media/image41.png)

3.  On the **Build an automated cloud flow** screen, enter flow name as
    **Invoice Flow**, select **Manually trigger a flow** and then select
    **Create**.

> ![](./media/image42.png)

4.  Select **+ icon** to add new step.

> ![](./media/image43.png)

5.  Add an action pane will open. Select **Custom** from the **Connector
    type** dropdown.

> ![A screenshot of a computer Description automatically
> generated](./media/image44.png)

6.  Select a **TeamsConnector** custom connector.

> **Note:** To see TeamsConnector, enter in the blank space near
> connector type.
>
> ![A screenshot of a computer Description automatically
> generated](./media/image45.png)

7.  Select **List Invoices** and then close the List Invoices pane.

> ![A screenshot of a computer Description automatically
> generated](./media/image46.png)

8.  Select **+ icon** to add new step.

> ![A screenshot of a computer screen Description automatically
> generated](./media/image47.png)

9.  Search for "approvals", and then select **Start and wait for an
    approval**.

> ![A screenshot of a computer Description automatically
> generated](./media/image48.png)

10. This will open **Create connection** pane. Select **Create new**.

> ![](./media/image49.png)

11. Select the **Approval type – Approve/Reject - First to respond** ,
    enter **Approve request** as **Title**, under **Assigned to** field,
    enter ‘admin’ and then select **Mod Admin** from suggestion.
    Collapse the pane.

> ![A screenshot of a computer Description automatically
> generated](./media/image50.png)

12. Select **New step.**

> ![A screenshot of a computer screen Description automatically
> generated](./media/image51.png)

13. Enter ‘condition’ in the search box and select **Condition** from
    the Control action.

> ![A screenshot of a computer Description automatically
> generated](./media/image52.png)

14. Select the **Choose a value** text box and then enter responses in
    the search box and select **Responses Approver response** from the
    dynamic content.

> ![A screenshot of a computer Description automatically
> generated](./media/image53.png)

15. Update the remaining condition with the desired result as **is equal
    to** and in third field enter **Approve**.

> ![](./media/image54.png)

16. Select **+ icon** under the **True** condition.

> ![A screenshot of a computer Description automatically
> generated](./media/image55.png)

17. On Add an action pane, select **Custom** from **Connector type**
    dropdown.

> ![A screenshot of a computer Description automatically
> generated](./media/image56.png)

18. Select **TeamsConnector**.

> ![A screenshot of a computer Description automatically
> generated](./media/image57.png)

19. Select **List Invoice Types**.

> ![A screenshot of a computer Description automatically
> generated](./media/image58.png)

20. Select **Save** to save the flow.

> ![](./media/image59.png)

21. Once saving is done, select **Test** to test the flow.

> ![A screenshot of a computer Description automatically
> generated](./media/image60.png)

22. Select **Manually** and then select **Test**.

> ![A screenshot of a phone Description automatically
> generated](./media/image61.png)

23. Check that your apps (Teams Connector and Approvals) are marked as
    green tick and then select **Continue**.

> ![A screenshot of a computer Description automatically
> generated](./media/image62.png)

24. Select **Run flow**.

> ![A screenshot of a computer Description automatically
> generated](./media/image63.png)

25. Select **Done**.

> ![A screenshot of a computer Description automatically
> generated](./media/image64.png)

### **Task 7: Manage approvals generated by the approval flow**

1.  Sign in to Microsoft Teams using <https://teams.microsoft.com/> with
    your given admin tenant credentials.

2.  Select View more apps (…) from left navigation pane, search for
    the **approvals** app, and then select it.

> ![A screenshot of a search engine Description automatically
> generated](./media/image65.png)

3.  View your received and sent approvals.

> ![A screenshot of a computer Description automatically
> generated](./media/image66.png)

4.  Click on **Requested** to take an action that activates your custom
    connector’s trigger.

> ![A screenshot of a computer Description automatically
> generated](./media/image67.png)

5.  Select **Approve**.

> ![A screenshot of a computer Description automatically
> generated](./media/image68.png)

6.  You can now see the status is updated as **Approved**.

> ![A screenshot of a computer Description automatically
> generated](./media/image69.png)

7.  Come back to power automate portal and you can see your flow ran
    successfully.

> ![A screenshot of a computer Description automatically
> generated](./media/image70.png)
