# Contrall your IoT home applinces using IBM IoT platform and Node Red.
----------------------------------------------------------------------------------------------------

### Create your Application on IBM Cloud

1. Create an account or Log in to IBM Cloud http://edit

2. Click on Catalog > Boilerplates > Internet of Things Platform Starter.

![1](https://user-images.githubusercontent.com/36006325/41722508-d6156ecc-7579-11e8-98f0-b399b3b9fbb9.png)

3. Enter a name for your application. Name must be unique. Then, click Create.

![2](https://user-images.githubusercontent.com/36006325/41722563-fea70a4e-7579-11e8-85ab-461f60a198af.png)

4. When your app is running, select the app URL or type it into the browser to open the Node-RED flow editor

![4](https://user-images.githubusercontent.com/36006325/41722643-2f775700-757a-11e8-9093-5e5d935a4d03.png)

You should see Flow 1 running on IBM Cloud with a virtual thermometer. For now, you’ll work with the flow in the red square as shown below:

![5](https://user-images.githubusercontent.com/36006325/41722728-62b73de2-757a-11e8-96d4-30735890518f.png)




# Terjmat - Translation Chatbot with Node-RED


## Overview
Terjmat is a multi-language translation service integrated with Telegram application to make the translation easy by using IBM services. IBM's Language Translator is one of the best language translation service, it has the capability to connect to other IBM's services. These services can be linked to Telegram application using Node-RED app. When you link them, users can use the translation in an easy way by sending text or voice to your bot. In this guide, we shall go through the steps involved in creating a Node-RED boilerplate available in IBM Cloud and link Terjmat to a Telegram as the user interface using Node-RED flows in under 20 minutes by using only IBM Cloud services.
## Learning objectives
After completing this project, you will understand how to;
- [Create a Node-RED flow](#creating-node-red)
- [Create a Telegram bot](#creating-a-telegram-bot)
- [Create a translator dialog using Language Translator, Speech to Text, Text to Speech IBM services](#create-the-flow)
- [Integrate Node-RED with Telegram as an interface for Terjmat](#configure-the-telegram)
## Prerequisites
In order to complete this project, you will need the following prerequisites:
- [IBM Cloud](https://www.ibm.com/cloud/) account - sign up if you don't have an account yet.
- [Language Translator](https://github.com/watson-developer-cloud/node-red-labs/blob/master/basic_examples/language_translator/README.md) service
- [Language Identification](https://github.com/watson-developer-cloud/node-red-labs/blob/master/basic_examples/language_identification/README.md) service
- [Speech to Text](https://github.com/watson-developer-cloud/node-red-labs/blob/master/basic_examples/speech_to_text/README.md) service
- [Text to Speech](https://github.com/watson-developer-cloud/node-red-labs/blob/master/basic_examples/text_to_speech/README.md) service
- [Node-RED starter](https://console.bluemix.net/catalog/starters/node-red-starter)
- Install Telegram Application on your Mobile Phone.

## Estimated time
- Creating a bot on Telegram should take less than 5 minutes
- Developing the complete application on Node-RED should take a maximum 20 minutes.
- Overall the time for completing this project should take approximately 25 minutes.
## Building the Translation app


### Creating Node-RED
To create and configur Node-RED app, go to your IBM Cloud account and click Catalog then choice Starter Kits from the lift side then choice Node-RED Starter as shown in the following figure.

![`Translator`](images/3.png)



After that, Fill-out the fields to create IoT Platform:
- App name: has to be unique in the IBM cloud domain.
- Host name: will be filled out automatically based on the App name.

click on Create 
![`Translator`](images/4.png)

Then, wait seconds until shows the application shows Running and click on Visit App URL

![`Translator`](images/5.png)

After that, for first time, it will ask you to setup the username and password. Please follow the instruction to secure your editor so only authorized users can access it. 

<img src="images/6.png" width="50%" height="40%" >

Then, click on "Go to your Node-RED flow editor".

![`Translator`](images/7.png)

### Configure the Telegram 
Now, this is Node-RED editer and we need to add Telegram nodes, so select manage palette from the top right menu.

![`Translator`](images/8.jpg)

At the manage palette menu click on the Install tab then search for telegram. After that, install node-red-contrib-telegrambot and close the palette menu.

![`Translator`](images/9.png)

Search for telegram nodes from the upper left filter section then drag and drop Telegram receiver and Telegram sender nodes.  
![`Translator`](images/10.png)
Double click on the Telegram receiver node and click on the pencil icon for configuring your bot credentials

![`Translator`](images/11.png)

Fill the bot-name and token fields according to the bot credentials you created earlier.

![`Translator`](images/12.png)

In Telegram sender node select the bot credentials you created in Telegram receiver node (example_bot in my case).

![`Translator`](images/13.png)

Now you have configured the Telegram part on Node-RED. You can test it by connecting the Telegram receiver node to the Telegram sender node.

![`Translator`](images/14.png)

You can send a message to your bot on Telegram and it will echo the message you wrote. That's because we forwarded the message payload directly to the Telegram sender.

<img src="images/15.jpg" width="50%" height="40%" >


