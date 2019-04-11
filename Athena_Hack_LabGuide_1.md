#Athena Hack - Cisco Webex Lab Guide#

##Prerequisites##

* A [Cisco Webex](https://www.webex.com)

* A [Built.io](http://built.io) account

* A [Giphy](http://giphy.com) account

* Download Webex Teams Desktop https://www.webex.com/team-collaboration.html

##Creating a Webex Teams Bot##
In this section you will create a Webex Teams Chatbot from the Webex developer pages.

To create you webex teams bot log into [deveoper.webex.com](https://https://developer.webex.com)

1. Select the Bots "Automate workflows and gain efficiencies in Webex"

2. Click the "Create a Bot" button

3. Fill in the Bot Name and Username, select and Icon and give it a short description and select "Add Bot"
![alt text](Athena_Images1/botcreate1.png "Logo Title Text 1")

4. Your bot will be created and an Access Token and Bot ID will be generated.
![alt text](Athena_Images1/botcreate2.png "Logo Title Text 1")

PLEASE MAKE A COPY OF YOUR ACCESS TOKEN AND BOT ID. ONCE YOU LEAVE THIS PAGE YOU CAN NOT RETRIEVE IT AND A NEW TOKEN WILL NEED TO BE GENERATED

5. Click "ADD BOT" and your bot is ready to chat.

##Creating a Webex Teams Room##
In this section you will download the Webex Teams desktop client, create a new space and add your bot to the space.

1. If you have not already done so, Go to [Cisco Webex](https://www.webex.com) homepage and select "Team Collaboration". This will take you to the Teams download page.


2. Select "Download Teams" and install.

3. Once teams is installed create a new teams space
![alt text](Athena_Images1/teamscreateaspace.png "Create a Teams Space")


3. Give your new space a name *(optionally you can add your bot name at this stage or we can do it later)*
![alt text](Athena_Images1/teamscreateaspace2.png "Create a Teams Space")

4. If you have not already added your bot do it now by selecting clicking dotted circle top right and selecting "Add People"
![alt text](Athena_Images1/teamsaddbot.png "Create a Teams Space")

5. Type the name of the Bot you created.
![alt text](Athena_Images1/teamsaddbot2.png "Create a Teams Space")

COOL! Now you have a teams space and a bot. We now need to teach it how to talk and do stuff.

##Creating a Built.io Workflow for your Bot##

In this section we will build a workflow in built.io that will instruct our bot to perform some functions.
We will use a standard Webex Teams workflow template

If you have not already done so, log in or sign up [Built.io](http://built.io) and [Giphy](http://giphy.com) account

1. Once you have logged in to built.io you will see this default screen
![alt text](Athena_Images1/builtdefaultscreen.png "Create a Teams Space")

2. select "Library" and you will see a list of pre-defined workflows. We want to select the "Webex Teams BOT" workflow
![alt text](Athena_Images1/builtdefaultadd.png "Create a Teams Space")

3. The Webex Teams Bot workflow will be added to your default project
![alt text](Athena_Images1/builtaddfromlibrary2.png "Create a Teams Space")

4. Select the worflow and then click it to open the dialogue
![alt text](Athena_Images1/builtwebexteamsbot.png "Create a Teams Space")
Now we start to populate the workflow with the Webex Teams information generated in the previous steps

5. From the dialoge box select "Connect to Cisco Webex Teams Bot"
![alt text](Athena_Images1/builtaddnewbot.png "Connect to Bot")

6. Give the Bot a name and insert the Bot Token you recored in the prevous Bot creation steps
![alt text](Athena_Images1/builtaddbottoken.png "Add Bot Token")

7.Now we need to add our space ID. To do this we need to go back to [deveoper.webex.com](https://https://developer.webex.com) and select documentation. We are looking for API REFERENCE and Rooms. [Shortcut here](https://developer.webex.com/docs/api/v1/rooms)

8.Once you are in the rooms API documentation you will find the Rooms API Calls. Select "LIST ROOMS"
![alt text](Athena_Images1/teamsroomlist.png "Find Space ID")

9.The API form is populated for you. Jsut press "Run"
![alt text](Athena_Images1/teamsroomlist2.png "Find Space ID")

10.The API request will be made and the Response will list all rooms assocaited with your webex account.
![alt text](Athena_Images1/teamsroomlist3.png "Find Space ID")
Find the room ID associated with the space you created earlier. (In the example above its the first room. Copy the "ID" from the response. For exmaple "Y2lzY29zcGFyazovL3VzL1JPT00vNzM0ODIzNzAtNWJiMC0xMWU5LTgzY2QtMGQ1YWM4YWM2OGMx"
Remember to remove the quotes)

11.Go back to built.io and Add the Room ID to you built.io workflow
![alt text](Athena_Images1/builtaddroom.png "Find Space ID")
Leave "User Email ID" blank and in the "Has File(s) box select "FALSE" from the drop down.
Leave Trigger Execution as default "if other user posts a message"

12.Now you will need your Giphy API. You get this by logging into [deveopers.giphy.com](https://https://developers.giphy.com) with your Giphy credentials you created earlier. If you didn't create a Gihpy account now.

13.Click the "Create an App" button


![alt text](Athena_Images1/giphycreatebutton.png "Find Space ID") and give you app an name and description select "Create New App"

14.You will now be presented with your very own Giphy API Key *(Make a copy of this)*
![alt text](Athena_Images1/giphykey.png "Find Space ID")

15.Now back to built.io and select a new Giphy Connection
![alt text](Athena_Images1/builtaddgiphykeybox.png "Find Space ID")

16.Add the Key

![alt text](Athena_Images1/builtaddyourgiphykey.png "Find Space ID")

17.Reenter your Webex Bot and Room ID
![alt text](Athena_Images1/builtaddyourbotandspaceagain.png "Find Space ID"), click "Import This Workflow"

18. Lastly, check you workflow is SAVED and ON
![alt text](Athena_Images1/builtensureswitchedon.png "Find Space ID")

##Testing it All Works##

1. Go to your webex Team desktop and into the space you created earlier with the Bot in it. Say "hello" to your Bot (remember to address the bot directly with an "@")

![alt text](Athena_Images1/teamsbottalk.png "Find Space ID")

and....drop the mic! You have a working chatbot with integrations.
![alt text](Athena_Images1/hilarious.png "Find Space ID")

2.
