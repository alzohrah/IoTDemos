# Analyze picture using IBM watson and Node Red.
----------------------------------------------------------------------------------------------------

## Overview

Analyzing picture become easier recently by using IBM Watson Visual Recognition. It will analyze the picture and give you all objects inside the picture with the percentage of accuracy. This project is a sample of visual recognition web app to analyze picture and detect an object. 

## Learning objectives
After completing this project, you will understand how to;
- Using a Node-RED.

- [Create Watson IoT Devices in IBM Watson IoT Platform](#Create-Watson-IoT-Devices-in-IBM-Watson-IoT-Platform)
- [Configure your Node-RED application on Raspberry pi](#Configure-your-Node-RED-application-on-Raspberry-pi)

- [Create Watson IoT APP in IBM Watson IoT Platform](#Create-Watson-IoT-APP-in-IBM-Watson-IoT-Platform)
- [Configure your Node-RED application on IBM Cloud](#Configure-your-Node-RED-application-on-IBM-Cloud)
- [Create your Node-RED flow on Raspberry pi](#Create-your-Node-RED-flow-on-Raspberry-pi)
- [Create your Node-RED flow on IBM Cloud](#Create-your-Node-RED-flow-on-IBM-Cloud)

## Prerequisites
In order to complete this project, you will need the following prerequisites:
- [IBM Cloud](http://ibm.biz/iot-cloud-signup) account - sign up if you don't have an account yet.
- [Node-RED starter](https://console.bluemix.net/catalog/starters/node-red-starter)
- [IBM Watson Visual Recognition](https://console.bluemix.net/catalog/services/visual-recognition)


## Estimated time
- Creating a Watson IoT Devices on IBM Watson IoT Platform should take less than 10 minutes.
- Creating your Node-RED application on Raspberry pi should take less than 10 minutes.
- Creating your Node-RED application on IBM Cloud should take less than 10 minutes.
- Developing the complete application on Node-RED should take a maximum 20 minutes.
- Overall the time for completing this project should take approximately 50 minutes.



### Create IBM Watson Visual Recognition

Open your IBM Cloud account then **click** on _Catalog_ --> _AI_ --> _Visual Recognition_ 
![`watson_visual_recognition1`](images/watson_visual_recognition1.png)

Type a unique service name then click **Create**.

![`watson_visual_recognition2`](images/watson_visual_recognition2.png)

After creating the service, **save the credentials and keep them safe**.

![`watson_visual_recognition5`](images/watson_visual_recognition5.png)


 
### Create the flow. 


Copy the code form the [visual recognition flow](visual_recognition_flow.json) and import it into _IBM Cloud Node-RED_ clipboard:



![`Import_flow`](images/Import_flow.png)


Your flow should look like the following figure. 


![`watson_visual_recognition3`](images/watson_visual_recognition3.png)

### Configure IBM Watson Visual Recognition on Node-RED

Double click on visual recognition node then fill the following; API Key, Service Endpoint, and choose Classify an image on Detect. 

Finally, click on Deploy button in the upper right.

To see your application, go to ```[yourdomain] /upload ```

![`watson_visual_recognition6`](images/watson_visual_recognition6.png)

**_Congratulations!!_**

