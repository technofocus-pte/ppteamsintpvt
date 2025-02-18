# **Lab 5: Build a canvas app to have a conversation about your business data in a Teams app**

### **Task 1: Create a new Team**

1. Sign into the **Microsoft Teams** using !!https://teams.microsoft.com/!! with the given admin tenant credentials. To create a new team,          select the **Teams** tab, and then select **+ icon** (Create and join teams and channels) on the top left of the navigation
   pane.

     ![A screenshot of a computer Description automatically generated](./media/image1.png)

2.  Select **Create Team.** 

     ![A screenshot of a computer Description automatically generated](./media/image2.png)

3.   Give the team a name such as !!Calls and Meetings Integration!!,
    enter the name of the channel as !!Business Conversation!! and then
    click on **Private**.

     ![A screenshot of a computer Description automatically generated](./media/image3.png)

4.  Select **Public**.

     ![A screenshot of a computer Description automatically generated](./media/image4.png)

5.  Select **Create**.

     ![A screenshot of a computer Description automatically generated](./media/image5.png)

6.  For now, select **Skip** on **Add members to Calls and Meetings
    Integration**.

     ![A screenshot of a computer Description automatically generated](./media/image6.png)
    
     The new team gets created, and is listed under the Teams tab.
    
     ![A screenshot of a computer Description automatically generated](./media/image7.png)

### **Task 2: Create a new app**

1.  Select **(…) View more apps** and then select **Power Apps** from
    the left-pane.

     ![A screenshot of a computer Description automatically generated](./media/image8.png)

2.  Select **+ New app** under **Recent apps**.

     ![A screenshot of a computer Description automatically generated](./media/image9.png)

3.  Select the team **Calls and Meetings Integration**, and then
    select **Create**.

     ![A screenshot of a computer Description automatically generated](./media/image10.png)

4.  The process for creating the app will take 2-3 minutes, if it takes more than that then refresh the window and repeat the above steps (Step       1 - 3).

     ![A screenshot of a computer Description automatically generated](./media/image11.png)
    
     ![A screenshot of a computer Description automatically generated](./media/image12.png)
    
    The app gets created and Power Apps Studio opens to allow editing the
    app.

5.  Enter a name for the app, such as !!Conversation app!! and
    select **Save**.

     ![A screenshot of a computer Description automatically generated](./media/image13.png)
    
     **Note:** If you see the pop-up that says ‘This app is read-only’ then
     select **Got it** and then select **Override** on the yellow note.
    
     ![A screenshot of a computer Description automatically generated](./media/image14.png)
    
     ![A screenshot of a computer Description automatically generated](./media/image15.png)

6.  The app is created with a default gallery on **Screen1**.

     ![A screenshot of a computer Description automatically generated](./media/image16.png)

### **Task 3: Add Teams as a connector**

1.  Select **Data** from the left-pane, select **+ Add data**, and then
    select **Connectors**.

     ![A screenshot of a computer Description automatically generated](./media/image17.png)

2.  Scroll down and select **See all connectors**.

     ![A screenshot of a computer Description automatically generated](./media/image18.png)

3.  Search for and select **Microsoft Teams** connector.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image19.png)

4.  Click on **Connect** button on the Microsoft Teams side pane.

     ![A screenshot of a computer Description automatically generated](./media/image20.png)

5.  You can see that Teams connector is now added.

     ![A screenshot of a computer Description automatically generated](./media/image21.png)

### **Task 4: Add a new table to capture company record**

    We need to add a table to maintain a list of companies we'll use as the company record, and to start a conversation about it.

1.  Select **Data** from the left-pane. Select **+ Add data** and then
    select **Create a new table**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image22.png)

2.  On **Create a new table page,** click on **Start with a blank
    table.**

     ![A screenshot of a computer Description automatically generated](./media/image23.png)

3.  Select **pencil icon** next to **New table** to give a name. Enter
    the name as !!Company!! and then select **Save**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image24.png)

4.  After adding the Display name, add following company names in the table
    column one by one by hitting the Enter key and then click on **Save
    and close**.

     !!Microsoft!!, !!Infosys!!, !!Accenture!!, !!Wipro!!, !!Dell!! and !!Google!!.
    
     ![A screenshot of a computer Description automatically generated](./media/image25.png)

### **Task 5: Add a new screen to select the customer**

    Next, we'll add a screen to the app so that users can select the customer that they want to have the conversation about.

1.  In the tree view, select **+ New screen.**  Select **List**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image26.png)
    
     A new screen gets added with a gallery list.
    
     ![A screenshot of a computer Description automatically generated](./media/image27.png)

2.  Double-click on **TemplateGalleryList1** under **Screen2** and replace it by the new title !!Companies List!!.

     ![A screenshot of a computer Description automatically generated](./media/image28.png)
    
     ![A screenshot of a computer Description automatically generated](./media/image29.png)

3.  With the **Companies List** selected from the **Tree view**, click on
    drop-down for **Data source** under the **Properties** pane.

     ![A screenshot of a computer Description automatically generated](./media/image30.png)

4.  Select **Companies** as the data source for the gallery.

     ![A screenshot of a computer Description automatically generated](./media/image31.png)

5.  The list of companies that was added shows up in the
    gallery **Companies List**.

     ![A screenshot of a computer Description automatically generated](./media/image32.png)

6.  Delete **Screen1** from the tree view. Click on **(…)** in front of
    **Scrren1** and then select **Delete**.

     ![A screenshot of a computer Description automatically generated](./media/image33.png)

7.  Double click on Screen2 in the tree view and rename it
    to **Screen1**.

     ![A screenshot of a computer Description automatically generated](./media/image34.png)

### **Task 6: Add a new table to capture the conversation details**

    We need to add another table to capture the details such as the Teams
    conversation ID, team, and channel related to a conversation started in
    the app.

1.  Select **Data** > **+ Add data** > **Create new table**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image35.png)

2.  Select the **Start with a blank table** template to build a new
    table.

     ![A screenshot of a computer Description automatically generated](./media/image23.png)

3.  Click on the **Pencil** icon, beside **New table**. Enter table name
    as !!Conversation!!.  Click on **Save**.

     ![A screenshot of a computer Description automatically generated](./media/image36.png)

4.  Click on **+ New column** and add a new column enter the details and
    then select **Save**.

     **Display name:** !!Team!!
    
     **Data type:** Text
    
     ![A screenshot of a computer Description automatically generated](./media/image38.png)
    
     Repeat the procedure and add the following columns to the conversation table.
    
     **Column:** !!Team Channel!!, **Type:** Text
    
     **Column:** !!Team Name!!, **Type:** Text
    
     **Column:** !!Channel Name!!, **Type:** Text
    
     **Column:** !!Company!!, **Type:** Lookup, related table= Company
    
     ![A screenshot of a computer Description automatically generated](./media/image39.png)

5.  You can now see new columns are now added to the table and then
    select **Save and close**.

     ![A screenshot of a computer Description automatically generated](./media/image40.png)

### **Task 7: Add a new screen to start or join a conversation**

    Now, we'll add a new screen where the app user can start or join aconversation.

1.  In the tree view, select **+ New screen** > **Blank layout**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image41.png)

2.  Update the **Fill** property of the screen to !!RGBA(224, 224, 237, 1)!!.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image42.png)

3.  Select **+** (Insert) > **Input** > **Button**.

     ![A screenshot of a computer Description automatically generated](./media/image43.png)

4. Double-click on the **Button1** under the **Screen3** from the **Tree view** and rename it to !!startaconversation_Button!!.

   ![A screenshot of a computer Description automatically generated](./media/image4.1.png)

   ![A screenshot of a computer Description automatically generated](./media/image4.2.png)
   
5.	Update the properties of the **startaconversation_Button** by selecting it one by one from **Property selector**.
   
   **Text**: !!"Start a conversation"!!
   
   **OnSelect**: !!Set(enterMessage,true)!!

   ![A screenshot of a computer Description automatically generated](./media/image5.1.png)

6.	Select **startaconversation_Button** on the canvas and drag it at the place shown in the image below.

   ![A screenshot of a computer Description automatically generated](./media/image6.1.png)

7.	Select **+ (Insert)** > **Input** > **Combo box**.

   ![A screenshot of a computer Description automatically generated](./media/image7.1.png)

8.	Double-click on the **ComboBox1** under **Screen3** and rename it to !!team_Combobox!!.

   ![A screenshot of a computer Description automatically generated](./media/image8.1.png)

9.	Update the following properties of the **team_Combobox** by selecting it one by one from **Property selector**.
    
   **Items**:  !!MicrosoftTeams.GetAllTeams().value!!
   
   **Text**: !!"Team"!!
   
   **Tooltip**:  !!"Team"!!
   
   **Visible**:  !!enterMessage!!

   ![A screenshot of a computer Description automatically generated](./media/image9.1.png)

10. Select **team_Combobox** on the canvas and drag it under the **startaconversation_Button** as shown in the image below.

    ![A screenshot of a computer Description automatically generated](./media/image10.1.png)

11. Add another combo box, rename it to !!channel_Combobox!!, update the following properties and then drag it below the **team_Combobox**.

   **Items**: !!If(!IsBlank(team_Combobox.Selected.id),MicrosoftTeams.GetChannelsForGroup(team_Combobox.Selected.id).value)!!
   
   **Text**: !!"Channel"!!
   
   **Tooltip**: !!"Channel"!!
   
   **Visible**: !!enterMessage!!

   ![A screenshot of a computer Description automatically generated](./media/image11.1.png)

   **Note**: Do not place it immediately below Start a conversation button. There is teams_Combobox button which is invisible right now. To view    that you can select it from Tree view. 

12. Select **+ (Insert)** > **Input** > **Text box**.

   ![A screenshot of a computer Description automatically generated](./media/image12.1.png)
   
13. Rename the Text box to !!message_TextBox!!, update the following properties of the textbox and then drag it below the **channel_Combobox**.

    **Value**:	""
    
   **Placeholder**:	!!“Type message here”!!
   
   **Visible**: !!enterMessage!!

   ![A screenshot of a computer Description automatically generated](./media/image13.1.png)

14. Select **+ (Insert)** > **Input** > **Button**.

   ![A screenshot of a computer Description automatically generated](./media/image14.1.png)
   
15. Rename the Button to !!submit_Button!!, update the following properties of the button and then drag it below the **message_TextBox**.

    **Text**:	!!"Submit"!!
    
   **Visible**: !!enterMessage!!

    ![A screenshot of a computer Description automatically generated](./media/image15.1.png)

17. From the **Property selector**, select the **OnSelect** property of the **submit_Button** and copy the following formula.

   '''
   
   Patch(Conversations,Defaults(Conversations),{'New column':"1",Team:team_Combobox.Selected.id,'Team Channel':channel_Combobox.Selected.id,Company:'Companies List'.Selected});

   
   Set(enterMessage,false); 
   
   Reset(team_Combobox);
   
   Reset(channel_Combobox);
   
   Reset(message_TextBox);
   
   '''

   ![A screenshot of a computer Description automatically generated](./media/image16.1.png)

### **Task 8: Update the gallery OnSelect Property**

1.  Select **Screen1** from the tree view and then select
    the **Companies List** gallery.

2.  Set the **OnSelect** property of the gallery item to **Navigate
    (Screen3)**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image57.png)

### **Task 9: Save and publish the app**

1.  Select **Save** on the top-right to save the app.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image58.png)

2.  Select **Publish** on the top-right to publish the app.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image59.png)

3.  Select **Next**.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image60.png)

4.  Select **+ icon** next to **Business Conversation** channel. You can
    see the Conversation app is added to the channel. Select **Save and
    Close** to complete the publishing of the app.

     ![](./media/image61.png)

### **Task 10: Testing the app**

    Run the app in preview mode or go to the team in which the app iscreated.

1.  Select **Test** icon.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image62.png)

2.  The Companies gallery should show up as the first screen. Select one
    of the companies.

     ![A screenshot of a computer AI-generated content may be incorrect.](./media/image63.png)

3.  You should only see **Start a conversation** button.

   ![A screenshot of a computer AI-generated content may be incorrect.](./media/image3.1.1.png)

4.  Select **Start a conversation**.

5.  Additional fields should show up:

    - Team (dropdown with a list of teams)

    &nbsp;

    - Channel (dropdown list of channels within the selected team)

    &nbsp;

    - Message box (text box to type in the message to be sent to the
      team)

    &nbsp;

    - Submit button (to submit the message)
  
   ![A screenshot of a computer AI-generated content may be incorrect.](./media/image5.1.1.png)

6.  Select a team.

7.  Select a channel within the team.

8.  Enter message.

9.  Select **Submit**. All the additional fields/controls get hidden.

10. The data entered in the app will create a new record in **Coversations** table. To check that, select **Data** from the left navigation pane of the Power Apps editor, click on **More actions (...)** infront of the **Conversations** table and then select **Edit data** to see the data in the table. 

    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.1.1.png)
    
    ![A screenshot of a computer AI-generated content may be incorrect.](./media/image10.1.2.png)
