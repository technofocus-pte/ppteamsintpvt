# **Lab 4: Customize sample app templates**

## **Exercise 1: Use sample app templates in Microsoft Teams**

Several sample app templates are available for use in Microsoft Teams
that you can use. You can choose the sample app template that best fits
your business requirement and quickly install it to get started. Sample
app templates created with Power Apps typically consist of multiple
components such as apps, flows, and tables.

### **Task 1: Extract AppPackages and locate TeamsCustomApp**

1.  Navigate to **C:\Labfiles** on the VM and look for
    **AppPackages.zip** file.

    ![](./media/image1.png)

2.  Extract the ZIP file by right click on the **AppPackages.zip** and
    then click on **Extract all**.

    ![](./media/image2.png)

3.  Click on **Extract**.

    ![A screenshot of a computer Description automatically generated](./media/image3.png)

4.  In the **AppPackages** folder go to the '**Milestones**' folder. Find
    the **TeamsCustomApp.zip** file. Note this file location, we need
    this in next task.

   ![](./media/image4.png)

### **Task 2: Upload the app via the Teams client**

1.  Go to **Teams** in your web browser, by following the link
    !!https://teams.microsoft.com/!!. If required, sign in with the given tenant admin credentials.

    ![](./media/image5.png)

2.  Navigate to **Apps** click on **Manage your apps**.

    ![A screenshot of a computer Description automatically generated](./media/image6.png)

3.  Click on **Upload an app**.

    ![A screenshot of a computer Description automatically generated](./media/image7.png)

4.  Select **Upload an app to your org’s app catalog.**

    ![](./media/image8.png)

5.  Navigate to **TeamsCustomApp.zip** file, the one we have extracted
    in the previous task and click on **Open**.

    ![](./media/image9.png)

6.  Once the upload is complete, on the page of **Built for your
    organisation > Milestones** click on **Add**.

    ![](./media/image10.png)

7.  On the pop-up card, click on **Add.**

    ![A screenshot of a computer Description automatically generated](./media/image11.png)

8.  Select the channel - **TestChannel** in the **Test Team** and click **Go**
    to continue.

    ![](./media/image12.png)

9.  Another pop-up card will show up. Click **Save** to start the
    installation.

    ![](./media/image13.png)

10. Installation will take around 5 minutes, once the installation is
    complete we can start using the app.

11. If prompted allow the **App permissions**

    ![A screenshot of a computer Description automatically generated](./media/image14.png)

12. If, **"Manage projects effectively by key
    milestones"** page appears, click on **Continue.**

   ![A screenshot of a computer Description automatically generated](./media/image15.png)

13. Your app is ready to use.

   ![A screenshot of a computer Description automatically generated](./media/image16.png)

   **Note:** This App can be uploaded via the Teams admin center also.

## **Exercise 2: Open the sample app templates in Power Apps Studio**

### **Task 1: Open the Sample app template**

1.  Sign in to Teams by following the link
    !!**https://teams.microsoft.com/**!!. If you are on Teams, then follow
    the next step.

    ![](./media/image5.png)

2.  Select **View more apps (…)** Select **Power Apps**.

    ![](./media/image17.png)

3.  Select **Build** tab.

    ![](./media/image18.png)

4.  Select the team environment where you installed the sample app
    template. Here the team environment is **Test Team**.

    ![](./media/image19.png)

5.  Select **Installed apps**.

    ![](./media/image20.png)

6.  Select the sample app template that you installed i.e. **Milestones** app.

    ![A screenshot of a computer Description automatically generated](./media/image21.png)

    **Note :** The page will take 2-5 minutes to load, if the loading fails,
      close the browser, open Teams and repeat from step 2.

7.  If prompted, select **Save and reload**.

    ![](./media/image22.png)
   
    **Note:** If pop-up appears saying ‘**This app is read-only’** then
    select **Got it** and then select **Override** on the canvas screen.
   
    ![](./media/image23.png)
   
    ![](./media/image24.png)

### **Task 2: Remove sample data**

   When you install sample app templates, the tables might be pre-populated
   with sample data. The following table lists the sample app templates and
   the list of tables with the sample data to be removed:
   
1.  Make sure you are still on the Power Apps editor window and that the Milestone app is opened select **Data** from the left pane.

    ![A screenshot of a computer Description automatically generated](./media/image25.png)

2.  Select **More actions (…)** next to the table name **Project Milestones**.
    Select **Edit data**.

    ![A screenshot of a computer Description automatically generated](./media/image26.png)

3.  Select the rows that you want to delete in the sample data, here we
    select the **Feedback** row containing sample data, and click on
    **Delete 1 record(s)**.

    ![](./media/image27.png)

4.  Close the visual editor.

    ![A screenshot of a computer Description automatically generated](./media/image28.png)

### **Task 3: Add your logo to the loading screen**

1.  Select **Tree view** from the left pane.

    ![A screenshot of a computer Description automatically generated](./media/image29.png)

2.  Ensure that you are on **Loading Screen.**

    ![A screenshot of a computer Description automatically generated](./media/image30.png)

3.  Click on the **image** on the screen as shown in the image below.

    ![A screenshot of a computer Description automatically generated](./media/image31.png)

4. From the properties pane that opens on the right side of the screen, select **Image** drop-down.

    ![A screenshot of a computer Description automatically generated](./media/image34.png)

5.  From the drop-down select **+ Upload**.

    ![A screenshot of a computer Description automatically generated](./media/image35.png)

6.  You can select an image for your company or you can use sample image from
    **C:\Labfiles** and then select **Open**.

    **Note**: If a pop-up appears that says "**A file with that name is alreay exists**" then select **Replace**.  

    ![A screenshot of a computer Description automatically generated](./media/image36.png)

### **Task 4: Change the screen background color**

   **Note:** The Milestone app leverages global theme variables to ensure consistent
   user experience. If you modify a screen fill, the modified screen will
   no longer use the standard app theme.

1.  Considering you are still on the Power Apps editor window and
    Milestone app is opened.

2.  Select Tree view from the left pane. Select **About Screen** from
    **Tree view**.

    ![A screenshot of a computer Description automatically generated](./media/image42.png)

3.  Select **Fill** from the property list on the top left.

    ![](./media/image43.png)

4.  In formula bar, replace the formula with the color that you want.
    Here we enter **blue** and select the formula **Color.Blue** from
    the suggestion.

    ![A screenshot of a computer Description automatically generated](./media/image44.png)

5.  Screen background fill color will be set to the selected background
    color.

   ![A screenshot of a computer Description automatically generated](./media/image45.png)

### **Task 5: Publish app updates to Teams**

1.  Select **Save** from the top-right.

    ![A screenshot of a computer Description automatically generated](./media/image46.png)

2.  Select **Publish to Teams**

    ![A screenshot of a computer Description automatically generated](./media/image47.png)

3.  Select **Next**.

    ![A screenshot of a computer Description automatically generated](./media/image48.png)

4.  Select **+ icon** next to **TestChannel**.

    ![A screenshot of a computer Description automatically generated](./media/image49.png)

5.  You can see that **Milestone** app is added to **TestChannel** and then click on
    **Save and close**.

    ![A screenshot of a computer Description automatically generated](./media/image50.png)
