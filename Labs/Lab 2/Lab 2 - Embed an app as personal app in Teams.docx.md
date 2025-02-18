# **Lab 2 - Embed a model-driven app as personal app in Teams (preview)** 

### **Task 1: Create a database on existing environment**

1.  Sign into **Power Platform admin center**
    using !!**https://admin.powerplatform.microsoft.com**!!
    with the given admin tenant credentials.

     ![A screenshot of a computer Description automatically generated](./media/image1.png)

2.  Select **Environments** from the left navigation pane. Click on the **Contoso (default)** environment.

     ![](./media/image2.png)

3.  In the **Add Dataverse** section and click on **+ Add Dataverse**.

     ![A screenshot of a computer Description automatically generated](./media/image3.png)

4.  **Add Dataverse** pane is now opened. Toggle the button for **Deploy
    sample apps and data** to **Yes** and then select **Add.**

     ![A screenshot of a computer Description automatically generated](./media/image4.png)

5.  This will take 2-3 minutes, and the environment will be prepared.
    You should see the state as **Ready** and the Dataverse is also
    added.

     **Note:** You can refresh the page if the environment takes too long to be ready.
    
     ![A screenshot of a computer Description automatically generated](./media/image5.png)

### **Task 2: Create a Model-driven app in Power Apps**

1.  Sign into Power Apps
    using !!**https://make.powerapps.com**!!
    with the given admin tenant credentials.

2.  From the environment selector, select the **Contoso (default)**
    environment.

     ![](./media/image6.png)

3.  Select **+Create** from the left navigation pane and then select
    **Blank app**.

     ![A screenshot of a computer Description automatically generated](./media/image7.png)

4.  Select **Create** in the **Blank app based on Dataverse** tile.

     ![A screenshot of a computer Description automatically generated](./media/image8.png)

5.  On the **New Model Driven App** page, enter the following details,
    and then click **Create**:

     **Name**: Enter a name for the app, !!**Account tracking**!!
    
     **Description**: !!**This is my first model-driven app**!!
    
     ![A screenshot of a computer Description automatically generated](./media/image9.png)

5.  Select **Add page** on the command bar, and then select **Dataverse
    table**.

     ![A screenshot of a computer Description automatically generated](./media/image10.png)

6.  Select **Account**, and then select **Add**.

     ![A screenshot of a computer Description automatically generated](./media/image11.png)

7.  Your app with the account table is displayed similarly to how it
    appears to users at run time when published.

     ![A screenshot of a computer Description automatically generated](./media/image12.png)

8.  Select **Save and Publish** from the toolbar.

     ![A screenshot of a computer Description automatically generated](./media/image14.png)

### **Task 3: Play your app**

1.  Select **Play** from the toolbar.

     ![A screenshot of a computer Description automatically generated](./media/image15.png)

2.  This opens a new tab. To create a record, select **+ New**.

     ![A screenshot of a computer Description automatically generated](./media/image16.png)

3.  Fill up the following information then select **Save & Close**.

     **Account Name:** !!Test account!!
    
     **Phone:** !!123456!!
    
     **Address 1: City:** !!Richmond!!
    
     **Address 1: Country/Region:** !!United States!!
    
     ![A screenshot of a computer Description automatically generated](./media/image17.png)

### **Task 4: Embed the app in Teams as a personal app**

1.  Sign into Power Apps using !!https://make.powerapps.com/!! and ensure
    that you are in **Contoso (default)** environment.

     ![A screenshot of a computer Description automatically generated](./media/image18.png)

2.  Select **Apps** from the left navigation pane.

     ![A screenshot of a computer Description automatically generated](./media/image19.png)

3.  Select **More actions** (...) for the **Account tracking** app you
    want to share in Teams, and then select **Share** > **Add to
    Teams**.

     ![](./media/image20.png)

4.  **Add to Teams** panel opens on the right-side of the screen. Select **Add to Teams**.

     ![](./media/image21.png)

5.  You will be navigated to open the Teams. Select **Cancel** on the
    pop-up that says **Open Microsoft Team?** And then select **Use the
    web app instead**.

     ![A screenshot of a computer Description automatically generated](./media/image22.png)

6.  Select **Add** on Account tracking app’s pane that appears on the
    screen.

     ![A screenshot of a computer Description automatically generated](./media/image23.png)

7.  The pane now shows that the app added successfully then select
    **Open**.

     ![A screenshot of a computer Description automatically generated](./media/image24.png)

8.  You can see that app is now opened in the Teams and is also added to
    left navigation pane.

     ![A screenshot of a computer Description automatically generated](./media/image25.png)
