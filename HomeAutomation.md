# Contrall your IoT home applinces using IBM IoT platform and Node-RED.
----------------------------------------------------------------------------------------------------

## Overview

IoT technology is the devices’ future. Home automation is one of IoT application which helps to solve many problems and give us plenty of accessibility like controlling the devices by a website or smartphone app. This project is a sample of home automation devices which you can apply it to other home devices. 




## Learning objectives
After completing this project, you will understand how to;
- Using a Node-RED in Raspberry Pi

- [Create a Node-RED flow](#creating-node-red)
///
- [Create a translator dialog using Language Translator, Speech to Text, Text to Speech IBM services](#create-the-flow)
- [Integrate Node-RED with Telegram as an interface for Terjmat](#configure-the-telegram)
## Prerequisites
In order to complete this project, you will need the following prerequisites:
- [IBM Cloud](https://www.ibm.com/cloud/) account - sign up if you don't have an account yet.

- [Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform)
- [Node-RED starter](https://console.bluemix.net/catalog/starters/node-red-starter)
- Raspberry Pi 3




## Estimated time
- Creating a bot on Telegram should take less than 5 minutes
- Developing the complete application on Node-RED should take a maximum 20 minutes.
- Overall the time for completing this project should take approximately 25 minutes.



### Create Watson IoT Devices in IBM Watson IoT Platform 

After creating an Internet of Things Platform in IBM Cloud, click on Launch to go to IBM IoT Platform page.

![`Internet_of_Things_Platform`](images/Internet_of_Things_Platform.png)

Then go to Devices tab form the left side and **click** on ADD Device. **Note:_Remember Your Organization ID_**

![`Create-Watson-IoT-Devices`](images/Create-Watson-IoT-Devices.png)

Fill all the important information.







![`Create-Watson-IoT-Devices2`](images/Create-Watson-IoT-Devices2.png)

Fill the authentication Token or keep it empty to be generated for you.

![`Create-Watson-IoT-Devices3`](images/Create-Watson-IoT-Devices3.png)

These are important information to access to this device. **Save and keep them safe**.

![`Create-Watson-IoT-Devices4`](images/Create-Watson-IoT-Devices4.png)


 
### Configure your Node-RED application on Raspberry pi

#### Add ibm-watson-iot Nodes to your Node-RED
Check your Nodes pane on the left side if it has an ibm-watson-iot nodes as it shown in folloing figure. 

![`IBMWatson-IoT`](images/IBMWatson-IoT.png)

\* *skip this step if you have* \*
If you don't have, select manage palette from the top right menu.

![`Translator`](images/8.jpg)

At the manage palette menu click on the Install tab then search for ```ibm-watson-iot```. After that, install node-red-contrib-ibm-watson-iot and close the palette menu.

![`ibm-watson-iot`](images/ibm-watson-iot.png)


Search for **Watson IoT** nodes from the upper left filter section then drag and drop it.  







![`Configur-Watson-IoT`](images/Configur-Watson-IoT.png)


Double click on the node and click on the pencil icon for configuring your watson IoT credentials

![`Configur-Watson-IoT2`](images/Configur-Watson-IoT2.png)

Fill the all the important fields according to the your devices credentials on IBM Watson IoT platform that created earlier.
\* **Note:** write your server as the following ; ```[your_organizer_id].messaging.internetofthings.ibmcloud.com```

![`Configur-Watson-IoT3`](images/Configur-Watson-IoT3.png)

Click on **Deploy** to check if your node is connected successfully. 



![`Configur-Watson-IoT4`](images/Configur-Watson-IoT4.png)



If shows *disconnected* and all the information correct, go to **Logs** under your device in IBM Watson IoT platform. You'll see the same message because the security. **_Save your IP_**




![`Configur-Watson-IoT5`](images/Configur-Watson-IoT5.png)

Then go to **Policies** and click on the pencil icon next to *Whitelist* to add your IP.




![`Configur-Watson-IoT6`](images/Configur-Watson-IoT6.png)

Add your IP address that showed earlier to Whitelist.



![`Configur-Watson-IoT7`](images/Configur-Watson-IoT7.png)


Redeploy your Node-RED flow. Now you have configured the Watson IoT part on Raspberry Pi.


![`Configur-Watson-IoT8`](images/Configur-Watson-IoT8.png)






### Create Watson IoT APP in IBM Watson IoT Platform 

Go to *IBM Watson IoT platform* and click on **Apps**. *Generate API key* then save your credentials and keep them safe.

![`Create-Watson-IoT-APP`](images/Create-Watson-IoT-APP.png)


### Configure your Node-RED application on IBM Cloud


Open your Node-RED on IBM Cloud then drag and drop IBM IoT.



![`Configur-IBM-IoT`](images/Configur-IBM-IoT.png)

Then double click on the node and click on the pencil icon for configuring your IBM IoT credentials
![`Configur-IBM-IoT2`](images/Configur-IBM-IoT2.png)

Fill all fields according to the your API credentials on IBM Watson IoT platform that created earlier.

\* **Note:** write your server as the following ; ```[your_organizer_id].messaging.internetofthings.ibmcloud.com```

![`Configur-IBM-IoT3`](images/Configur-IBM-IoT3.png)

### Create your Node-RED flow on Raspberry pi

[Sample_IoT_application_flow](Sample_IoT_application_flow)

![`Node-red-in-Raspberry-pi`](images/Node-red-in-Raspberry-pi.png)

### Create your Node-RED flow on IBM Cloud



![`Node-red-in-Cloud`](images/Node-red-in-Cloud.png)
![`Node-red-in-Cloud-UI`](images/Node-red-in-Cloud-UI.png)


## Building an IoT application

### Configure IBM IoT platform

Now, this is Node-RED editer and we need to add IBM Watson IoT nodes, so select manage palette from the top right menu.

![`Translator`](images/8.jpg)

At the manage palette menu click on the Install tab then search for ```node-red-contrib-ibm-watson-iot```. After that, install node-red-contrib-telegrambot and close the palette menu.

![`Translator`](images/ibm-watson-iot.png)

Search for telegram nodes from the upper left filter section then drag and drop Telegram receiver and Telegram sender nodes.  
![`Translator`](images/10.png)



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


