# **Lab 3 - Create a canvas app from a list in Microsoft Teams** 

### **Task 1: Add a list to a Teams channel**

1.  Sign into the **Microsoft Teams**
    using !!https://teams.microsoft.com/!!
    with your Office 365 tenant credentials.

3.  Select **Teams** from the left navigation pane and then select
    **TestChannel** where you want to add a list. 

     ![A screenshot of a computer Description automatically generated](./media/image1.png)

4.  Click on the **Add a tab** icon.

     ![A screenshot of a computer Description automatically generated](./media/image2.png)

5.  Search **Lists** and click on **Lists**.

    ![A screenshot of a search results Description automatically generated](./media/image3.png)

6.  Click on **Save**.

    ![A screenshot of a computer Description automatically generated](./media/image4.png)

7.  On the **Welcome to Lists** page, click on **Create a list** tab.

    ![A screenshot of a computer Description automaticallygenerated](./media/image5.png)

8.  Select a template that matches your scenario, here we have selected
    **Event itinerary** template.

     ![A screenshot of a computer Description automatically generated](./media/image6.png)

9.  Scroll through the template to see the default columns that come
    with it.

     ![A screenshot of a computer Description automatically generated](./media/image7.png)

10.  Scroll down and select **Use template**.

     ![A screenshot of a computer Description automatically generated](./media/image8.png)

11. Give the list a name – !!Event itinerary!! and description – !!Event list!!,
    keep the default chosen color and icon or you can change the color
    and icon and then select **Create**.

     ![A screenshot of a computer Description automatically generated](./media/image9.png)

12. The list is created with the same columns that are in the template. 

     ![A screenshot of a computer Description automatically generated](./media/image10.png)

### **Task 2: Create an app from a list in Microsoft Teams**

1.  On the newly created list, select **More command (…)** and then
    select **Integrate.**

     ![A screenshot of a computer Description automatically generated](./media/image11.png)

2.   Select **Power Apps** > **Create an app**.

     ![A screenshot of a computer Description automatically generated](./media/image12.png)
    
3.  In the modal that appears, enter the name as !!Event Itinerary app!!
    for your app and then select **Save**.

     ![A screenshot of a computer Description automatically generated](./media/image13.png)
    
     **Note:** Ignore the pop-up. App will open in editing mode.
    
     ![A screenshot of a computer Description automatically generated](./media/image14.png)

4.  The app will be created using the data from your list.

    ![A screenshot of a computer Description automatically generated](./media/image15.png)

### **Task 3: Customize your app by adding and configuring controls**

1.  To add new screen to the app, select **+New screen** from the Tree
    view.

     ![](./media/image16.png)

2.  Select **Success** screen.

     ![](./media/image17.png)

3.  Double click on the **Success message**: **This was
    successfully completed**.

     ![](./media/image18.png)

4.  Change the success message to !!New event itinerary successfully
    completed!!.

     ![](./media/image19.png)

5.  To explore more customization options, from the **Tree view**,
    with **Screen3** selected, select **Insert**. Select
    the **Button** control under **Input**.

     ![A screenshot of a computer Description automatically generated](./media/image20.png)

6.  The button will appear at top left corner of the canvas.

     **Note:** Adjust the sliding bar to see the button.
    
     ![A screenshot of a computer Description automatically generated](./media/image21.png)

7.  Drag the button below the success message as shown in the image
    below. Resize the button just by pulling its corner.

     ![A screenshot of a video Description automatically generated](./media/image22.png)

8.  With the button selected on the canvas or from the tree view, select
    **Text** property from the **property selector** and chnage it to !!"Done"!!.

     ![](./media/image23.1.png)

9.  With the button selected on the canvas or from the tree view, select
    **OnSelect** property from the **property selector** and change it to !!Navigate(Screen1);!!.

     ![A screenshot of a computer Description automatically generated](./media/image24.1.png)

10. Save the app using **save icon**.

    ![](./media/image25.png)

### **Task 4: Publish App to Teams**

1.  Select **Publish to Teams** to publish your app to a channel where
    your Microsoft list is located.

    ![A screenshot of a computer Description automatically generated](./media/image26.png)

2.  On the **Publish** page click **Next.**

    ![A screenshot of a computer Description automatically generated](./media/image27.png)

3.  Select **+ icon** next to **TestChannel**.

    ![A white background with black text Description automatically generated](./media/image28.png)

4.  On the **Power Apps** page, click on **Save and close** button.

    ![A screenshot of a computer Description automatically generated](./media/image29.png)

5.  Select **Teams** from the left navigation pane.

    ![](./media/image30.png)

6.  Select **TestChannel** and then you can see the list and the app.

    ![](./media/image31.png)
