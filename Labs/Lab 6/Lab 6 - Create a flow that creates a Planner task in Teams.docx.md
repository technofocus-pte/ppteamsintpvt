# **Lab 6: Create a flow that creates a Planner task in Teams**

### **Task 1: Create a new channel and a Plan**

1.  Sign into the Microsoft Teams
    using [**https://teams.microsoft.com/**](urn:gd:lg:a:send-vm-keys) with
    the given admin tenant credentials.

![A screenshot of a computer Description automatically
generated](./media/image1.png)

2.  Select **Teams** on the left navigation pane and click on the **plus
    icon** to **Create and join teams and channels**.

![A screenshot of a computer Description automatically
generated](./media/image2.png)

3.  Click on **Create team**.

![A screenshot of a computer Description automatically
generated](./media/image3.png)

4.  Give name - **Task Inspection**, name your channel –
    **AutomateOrg**. Click on **Private**.

![A screenshot of a computer Description automatically
generated](./media/image4.png)

5.  Select **Public**.

![A screenshot of a computer Description automatically
generated](./media/image5.png)

6.  Now, select **Create**.

![A screenshot of a computer Description automatically
generated](./media/image6.png)

7.  Select **Skip** on Add members to **Task Inspection** window.

![A screenshot of a computer Description automatically
generated](./media/image7.png)

8.  You can now see the new team.

![A screenshot of a computer Description automatically
generated](./media/image8.png)

9.  From the left navigation pane, click on **View more apps (…)** and
    select **Planner**.

![A screenshot of a phone Description automatically
generated](./media/image9.png)

10. If you come across the pop-up that says **Welcome to Planner**,
    select **Get Started**.

![A screenshot of a computer Description automatically
generated](./media/image10.png)

11. Close the information pop-up window.

![A screenshot of a computer Description automatically
generated](./media/image11.png)

12. On the left side Navigation pane, click on the **+New plan** tab.

![A screenshot of a computer Description automatically
generated](./media/image12.png)

**Note:** If you don’t see +New plant, expand the Planner section as
shown below.

![A screenshot of a computer Description automatically
generated](./media/image13.png)

13. On the **Create new** page, select **Simple Plan.**

![A screenshot of a computer Description automatically
generated](./media/image14.png)

14. Select **Use template.**

![A screenshot of a computer Description automatically
generated](./media/image15.png)

15. On the **Create a plan from a template** page, name the plan as
    **Automate tasks,** Assign **Task inspection** group and click on
    **Create.**

![A screenshot of a computer Description automatically
generated](./media/image16.png)

16. You can see the newly created task.

**Note:** Close if any pop-up appears.

![A screenshot of a computer Description automatically
generated](./media/image17.png)

### **Task 2: Create a new flow**

To create a new flow, follow these steps:

1.  Navigate to teams by following the link
    [**https://teams.microsoft.com/**](urn:gd:lg:a:send-vm-keys) .

2.  From the left navigation pane, click on **View more apps (…)**,
    search for workflows and click on **Add** button to add workflows to
    teams

> ![A screenshot of a computer Description automatically
> generated](./media/image18.png)

3.  On the **Workflows** page, from the **Home** tab, select **+ New
    flow**, which takes you to the **Create** tab.

> ![A screenshot of a computer Description automatically
> generated](./media/image19.png)

4.  In the **Create** tab, notice that the menu down the left side gives
    you the option to select templates related to the task you’re trying
    to automate.

> ![A screenshot of a computer Description automatically
> generated](./media/image20.png)

5.  Select **+ Create from blank** in the top right of the screen.

> ![A screenshot of a computer Description automatically
> generated](./media/image21.png)

6.  Notice how **Power Automate** initiates a new flow within Teams.
    Rename your flow by selecting the word *Untitled* in the upper left
    of the menu bar and type in **Autoflow1** as new name. Next, we
    create the flow.

> ![A screenshot of a computer Description automatically
> generated](./media/image22.png)
>
> ![A screenshot of a computer Description automatically
> generated](./media/image23.png)

### **Task 3: Build the flow in Power Automate editor**

1.  In the **Search connectors and triggers** search field, search for
    “Teams when a new channel" and select the trigger **When a new
    channel message is added**.

![A screenshot of a computer Description automatically
generated](./media/image24.png)

2.  To have the flow monitor the correct Teams channel for new messages,
    make selections from both the **Team – Task
    Inspection** and **Channel - AutomateOrg** dropdowns as.

![A screenshot of a computer Description automatically
generated](./media/image25.png)

3.  Select **New step** to continue.

> ![A screenshot of a computer Description automatically
> generated](./media/image26.png)

4.  Now let's add a condition to search the subject of the messages to
    see if they have the word "task" in them. In the **Choose an
    operation** menu, select **Condition** from the available actions.
    (If you don't see it, enter **Condition** in the search field and
    then select it from the search results.)

![A screenshot of a computer Description automatically
generated](./media/image27.png)

5.  Within the **Condition** step, select the **Choose a value** field
    to view the available dynamic content. From the list of dynamic
    content, scroll down and select **Message subject**. (Alternatively,
    you can input *subject* in the Search field to narrow the results.)

![A screenshot of a computer Description automatically
generated](./media/image28.png)

6.  In the middle drop-down menu, select **contains**.

![A screenshot of a computer Description automatically
generated](./media/image29.png)

7.  Enter **task** in the box on the right.

> ![A screenshot of a computer Description automatically
> generated](./media/image30.png)

8.  Now, when the **Message subject** contains the word "task," it
    performs actions in the **If yes** area. The conditions in Power
    Automate are case-sensitive, so you need to add a few more
    conditions to detect common variations such as "Task" and "TASK."
    Select **+ Add** and then select **+ Add Row**.

![A screenshot of a computer Description automatically
generated](./media/image31.png)

9.  Use the same condition each time with **Message subject** from
    dynamic content. Add a two more conditions to detect common
    variations such as "Task" and "TASK." Change the condition to **Or**
    as shown below.

![A screenshot of a computer Description automatically
generated](./media/image32.png)

10. The **Condition** action provides two options for further
    actions, **If yes** and **If no**. If the condition is true, then we
    create a new Planner task. We don't need any actions if the
    condition is false, so we leave the **If no** condition blank. In
    the **If yes** condition box, select **Add an action**.

![A screenshot of a computer Description automatically
generated](./media/image33.png)

11. In the search box enter **planner** and then select **Create a
    task** from the results.

![A screenshot of a computer Description automatically
generated](./media/image34.png)

12. The **Create a task** step appears in the **If yes** field for
    your **Condition** step. Fill out the needed information for the
    Planner task as in this table.

Group ID: **Task Inspection**

Plan ID: **Automate tasks**

Title: Select dynamic content **Message body content**

Start Date Time: Select dynamic content **Message creation timestamp**

![A screenshot of a computer Description automatically
generated](./media/image35.png)

13. When you complete the task, select **Save** at the bottom of the
    editing window, or in the toolbar to complete the flow.

![A screenshot of a computer Description automatically
generated](./media/image36.png)

### **Task 4: Test the flow**

1.  To send a message to the Teams channel that the flow is monitoring.
    Here, select Teams from left navigation pane and then select
    **AutomateOrg** channel under **Task Inspection** team.

![A screenshot of a computer Description automatically
generated](./media/image37.png)

2.  Click on **Start a post** button on the channel page.

![A screenshot of a computer Description automatically
generated](./media/image38.png)

3.  In the subject line, enter a subject including the word **Task** and
    enter the message as **New task for the team, this is urgent, please
    start working on this ASAP.** And click on the **Post** button.

![A screenshot of a computer Description automatically
generated](./media/image39.png)

4.  The Teams connector checks for a new message in three-minute
    intervals. Click on the **View more apps (…)** and select
    **Planner**.

![A screenshot of a computer Description automatically
generated](./media/image40.png)

5.  Select **My Tasks** from the left navigation menu for the Planner.
    The planner will show a new task assigned under the plan name
    **Automate tasks.**

![A screenshot of a computer Description automatically
generated](./media/image41.png)

6.  To see the flow’s run history, click on the **View more apps (…)**
    and select **Workflows**.

![A screenshot of a computer Description automatically
generated](./media/image42.png)

7.  Click on **Automateflow1.**

![A screenshot of a computer Description automatically
generated](./media/image43.png)

8.  From the **Home** tab, select the flow that you created, listed
    under **Flow name**. The details screen view shows you more
    information on your flow and the **28-day run history**.

> ![A screenshot of a computer Description automatically
> generated](./media/image44.png)
