# **Lab 7: Create adaptive card for Teams**

### **Task 1: Install Workflows app in Teams** 

   **Note:** We already have installed Workflows app in Teams in the previous lab. So, you can skip this task and move forward to Taks 2.

1.  Sign into the Microsoft Teams
    using !!**https://teams.microsoft.com/**!! with
    your Office 365 tenant credentials.

     ![A screenshot of a computer Description automatically generated](./media/image1.png)

2.  Click on **View more apps (…)** on the left navigation pane and
    search for the **Workflows** and select it.

    ![A screenshot of a chat Description automatically generated](./media/image2.png)

### **Task 2: Add an action**

1.  Sign in to **Power Automate** using
    !!https://make.powerautomate.com/!! with your given admin tenant
    credentials.

     ![](./media/image3.png)

2.  Select **Contoso(default)** environment from environment selector.

     ![A screenshot of a computer Description automatically generated](./media/image4.png)

3.  Select **My flows** in the left navigation bar. Select **New
    flow** > **Instant cloud flow**.

     ![A screenshot of a computer Description automatically generated](./media/image5.png)

4.  Name your flow as **CloudFLowTest**, select **Manually trigger a
    flow** as the trigger and click on **Create**.

     ![A screenshot of a computer Description automatically generated](./media/image6.png)

5.  In the designer, select **New Step** and click on **Add an action**.

     ![](./media/image7.png)

6.  On the **Add an action** page, search for **Microsoft Teams**,
    select **See more** under the **Microsoft Teams.**

     ![A screenshot of a computer Description automatically generated](./media/image8.png)

7.  Now, select **Post an adaptive card and wait for a response** as the
    action.

     ![A screenshot of a computer Description automatically generated](./media/image9.png)

8.  Under **Post as** field, select Flow bot, under **Post in**, select
    **Channel**.

     ![A screenshot of a computer Description automatically generated](./media/image10.png)

9.  Select the **Team** and the **Channel** to which you'd like to post
    the card.

     Here select **Task Inspection** as team and channel as **AutomateOrg.**
    
     ![A screenshot of a computer Description automatically generated](./media/image11.png)

10. Paste this JSON into the **Message** box.

    '''
    {
    
        "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    
        "type": "AdaptiveCard",
    
        "version": "1.0",
    
        "body": [
    
            {
    
                "type": "TextBlock",
    
                "text": "Poll Request",
    
                "id": "Title",
    
                "spacing": "Medium",
    
                "horizontalAlignment": "Center",
    
                "size": "ExtraLarge",
    
                "weight": "Bolder",
    
                "color": "Accent"
    
            },
    
            {
    
                "type": "TextBlock",
    
                "text": "Header Tagline Text",
    
                "id": "acHeaderTagLine",
    
                "separator": true
    
            },
    
            {
    
                "type": "TextBlock",
    
                "text": "Poll Header",
    
                "weight": "Bolder",
    
                "size": "ExtraLarge",
    
                "spacing": "None",
    
                "id": "acHeader"
    
            },
    
            {
    
                "type": "TextBlock",
    
                "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer vestibulum lorem eget neque sollicitudin, quis malesuada felis ultrices. ",
    
                "id": "acInstructions",
    
    "wrap": true
    
            },
    
            {
    
                "type": "TextBlock",
    
                "text": "Poll Question",
    
                "id": "acPollQuestion"
    
            },
    
            {
    
                "type": "Input.ChoiceSet",
    
                "placeholder": "Select from these choices",
    
                "choices": [
    
                    {
    
                        "title": "Choice 1",
    
                        "value": "Choice 1"
    
                    },
    
                    {
    
                    "title": "Choice 2",
    
                    "value": "Choice 2"
    
                },
    
                    {
    
                        "title": "Choice 3",
    
                        "value": "Choice 3"
    
                    }
    
                ],
    
                "id": "acPollChoices",
    
                "style": "expanded"
    
            }
    
        ],
    
        "actions": [
    
            {
    
                "type": "Action.Submit",
    
                "title": "Submit",
    
                "id": "btnSubmit"
    
            }
    
        ]
    
    }
    '''

     ![](./media/image12.png)

12. Make the following replacements in the JSON.

     **Important:** Do not remove any quotation marks when you do the replacements. You can revise the car choices to suit your needs:

    **Header Tagline Text**: !!Power Automate Poll!!
    
    **Poll Header**: !!Preferred Car Model!!
    
    **Poll Question**: !!Please vote on your preferred car model from the choices listed here.!!
    
    **Replace the latin text with a reason, or business context, related to why you are conducting the poll**: !!We are polling our employees in         order to determine if we should provide personalized parking places that are sized for the most popular cars.!!
    
    **Choice 1 (replace in both places**): !!Tesla!!
    
    **Choice 2 (replace in both places**): !!Lexus!!
    
    **Choice 3 (replace in both places)**: !!Honda!!

     ![A screenshot of a computer Description automatically generated](./media/image13.png)
    
     ![A screenshot of a computer Description automatically generated](./media/image14.png)
    
     ![](./media/image15.png)

12. Close the **Post adaptive card and wait for a response** card.

     ![A screenshot of a computer Description automatically generated](./media/image16.png)

13. Select **New Step**.

     ![](./media/image17.png)

14. Search for **Send an email**  and select one of the **Send an
    email (V2)** actions under Office 365 Outlook.

     ![](./media/image18.png)

15. When prompted **sign in** using the given admin tenant credentials.

     ![](./media/image19.png)

16. Select **Switch to Advance mode** for **To** field.

     ![](./media/image20.png)

17. Click on the **To** field where we enter the input and now select
    **Dynamic content icon**.

     ![](./media/image21.png)

18. Select **body/responder/email** tag from the dynamic content.

     ![A screenshot of a computer Description automatically generated](./media/image22.png)

19. Enter subject function as !!**acPollChoices**!! from the dynamic
    content.

     ![](./media/image23.png)

20. Configure the **Body** of the email as follows. Replace the words in
    curly parentheses "{}" with dynamic tokens:  
    **Your poll response was {acPollChoices}** (acPollChoices is dynamic
    content from the wait for a response action). **It was submitted by
    {User Name}** (User Name is dynamic content from the trigger)

     ![](./media/image24.png)

21. Click on **save**.

     ![A screenshot of a computer Description automatically generated](./media/image25.png)

### **Task 3: Test your adaptive card**

1.  Click on the save button, then click on the Back button on the top
    left of the screen.

     ![A screenshot of a computer Description automatically generated](./media/image26.png)

2.  Close the pop-up.

    ![A screenshot of a computer Description automatically generated](./media/image27.png)

3.  On the **My flows** page, select **CloudFlowTest** click on the
    **Run** button to run the flow.

    ![A screenshot of a computer Description automatically generated](./media/image28.png)

4.  Check that the app connection is complete. Select **Continue**.

    ![A screenshot of a computer Description automatically generated](./media/image29.png)

5.  On the Run flow side pane click on the **Run flow** button.

    ![A screenshot of a computer Description automatically generated](./media/image30.png)

6.  Click on **Done.**

    ![A screenshot of a computer Description automatically generated](./media/image31.png)

7.  Now navigate back to teams page, under team select **Task Inspection
    team > AutomateOrg,** and notice Poll Request card has popped up.

    ![A screenshot of a computer Description automatically generated](./media/image32.png)

8.  Give your vote, here we select **Tesla** and click on **Submit.**

    ![A screenshot of a computer Description automatically generated](./media/image33.png)

    ![A screenshot of a computer Description automatically generated](./media/image34.png)

9.  Go to your mail box to check the poll response. The email
    notification contains the body that shows who submitted the response
    and which car was selected.

    ![A screenshot of a computer Description automatically generated](./media/image35.png)

10. Back on the Power Automate page we can Run history of flow as
    **Succeeded**.

    ![A screenshot of a computer Description automatically generated](./media/image36.png)

11. Congratulations! you’ve just made your first interactive adaptive
    card!
