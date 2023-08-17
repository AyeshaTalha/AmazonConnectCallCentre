# AmazonConnectCallCentre
<h2>Description:</h2>
This project involves creating a call center solution using Amazon Web Services (AWS) services, specifically Amazon Connect and Lex. The goal of this project is to leverage AWS services to build a scalable, efficient, and cost-effective call center solution.
<h2> Key Components and Services used:</h2>

1. Amazon Connect: Amazon Connect is a cloud-based contact center service provided by AWS. It allows you to set up and manage a virtual call center with features such as interactive voice response (IVR), automatic call distribution (ACD), and real-time analytics.

2. Amazon Lex: Amazon Lex is a service for building conversational interfaces using voice and text. It uses natural language understanding (NLU) to process and understand user inputs, enabling the creation of chatbots and virtual agents for call center interactions.

3. AWS Lambda: AWS Lambda is used to run serverless functions that can be integrated with Amazon Connect and Lex. It allows you to execute custom code in response to events, such as incoming calls or user interactions.

4. Amazon S3: Amazon Simple Storage Service (S3) is used to store and retrieve audio files, transcripts, and other media assets related to call center interactions. S3 provides scalable and durable object storage.

5. Amazon CloudWatch: CloudWatch is used for monitoring and logging the call center solution. It allows you to track metrics, collect logs, and set up alarms to ensure the system's performance and availability.
<h2>Project Workflow:</h2>

1. Design call center architecture: Define the call flow, IVR menus, and routing strategies for incoming calls. Determine the integration points with Amazon Lex for natural language understanding and automated responses.

<p align="center">
Call Centre Architecture: <br/>
<p align="center">
<img src="https://imgur.com/NXmevLq.png" height="80%" width="80%">
<br />

<p align="center">
<img src="https://imgur.com/vE1YJEf.png" height="80%" width="80%">
<br />
    
2. Set up Amazon Connect: Configure Amazon Connect to create the call center instance. Define phone numbers, queues, routing profiles, and hours of operation. Customize the IVR prompts and greetings.
<p align="center">
Creating an Amazon Connect Instance: <br/>
<img src="https://imgur.com/QV7bCw6.png" height="80%" width="80%">
<br/>
    
3. Seting up Identity for the Instance<br/>
<p align="center">
<img src="https://imgur.com/wyRDc8C.png" height="80%" width="80%"><br/>
    
4. Creating the Administrator for the instance.This Admin will be used to login on our website later. So do remember the username and password <br/>
<p align="center">
<img src="https://imgur.com/7OVujrX.png" height="80%" width="80%"><br/>
    
5. Seting up the Telephony: <br/>
<p align="center">
<img src="https://imgur.com/gWWE6xO.png" height="80%" width="80%"><br/>
    
6. You can view the S3 Bucket where your Instance Data is Stored. Scroll Down and Press Next.<br/>
<p align="center">
<img src="https://imgur.com/nYBy4sz.png" height="80%" width="80%"><br/>
    
7. Review all your data, Scroll Down and Press Create Instance. <br/>
<p align="center">
<img src="https://imgur.com/YLDGfLZ.png" height="80%" width="80%">
<br/>

8. Click on the Access URL of the Instance And Use the Admin User And Password Which We Set Up Earlier To Sign In<br/>
<p align="center">
<img src="https://imgur.com/Dd6vG2K.png" height="80%" width="80%"> <br/>

9. The Next Step is To Set Hours Of Operation. On the Dashboard Click On the Routing Option And Select Hours Of Operation<br/>
<p align="center">
<img src="https://imgur.com/ukjoJ1V.png" height="80%" width="80%"><br/>

10. Click on Add New Hours. Set a name, Select the Preferred Time Zone And Tht Number Of Working Days.<br/>
<p align="center">
<img src="https://imgur.com/lW4XEp6.png" height="80%" width="80%"><br/>

11. Now we Need to Set Up the Queues. On the Dashboard under the Routing Option, Select Queues.<br/>
<p align="center">
<img src="https://imgur.com/DRDYjE1.png" height="80%" width="80%"><br/>

12. Click on Add Queues. Name the Queue as Technical Queue and Select the Hours Of Operation as NineToFive.<br/>
<p align="center">
<img src="https://imgur.com/9aXeKGg.png" height="80%" width="80%"><br/>

13. Lets Add Another Queue For Sales. Name the Queue as Sales and Select the Hours Of Operation as Basic Hours.<br/>
<p align="center">
<img src="https://imgur.com/ykuFNXi.png" height="80%" width="80%"><br/>

14. Now we Need to Set Up the Routing Profiles.On the Dashboard Under the Users Menu Select Routing Profiles.<br/>
<p align="center">
<img src="https://imgur.com/cH6ToMJ.png" height="80%" width="80%"><br/>

15. Click on add Routing Profile and Add a Sales Routing Profile.Tick the Voice Box for Channel and Select Sales Queue under the Queues bar.
<br/>
<p align="center">
<img src="https://imgur.com/oQ7IDlN.png" height="80%" width="80%"><br/>
<p align="center">
<img src="https://imgur.com/6tDKWhq.png" height="80%" width="80%><br/>

16. Add Another Routing Profile for Technical Support. Tick the Voice Box for Channel and Select Technical Support Queues bar.<br/>
<p align="center">
<img src="https://imgur.com/VGpTv7A.png" height="80%" width="80%"><br/>

17. Lets add some users now. On the dashboard under the Users menu select User Management option.
<p align="center">
<img src="https://imgur.com/YEqcWLE.png" height="80%" width="80%"> <br/>

18. Click on "Add User". Enter all the information for the User and Select the Security Profile as Agent and Routing Profile as Sales.
<p align="center">
<img src="https://imgur.com/xOmlLh1.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/xOmlLh1.png" height="80%" width="80%"> <br/>

19. Lets add another user. Enter all the information for the User, Select the Security Profile as Agent and Routing Profile as Technical Support.
<p align="center">
<img src="https://imgur.com/F4a2jS8.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/m06ET1r.png" height="80%" width="80%"> <br/>

20. Now, we need to create Contact Flows. On the Dashboard, Under the Routing menu select Contact Flows option.
<p align="center">
<img src="https://imgur.com/cqlbtyf.png" height="80%" width="80%"> <br/>

21. Click on Create Contact Flow. Name the Flow as the Main Flow. On the lefthand side, you can see a list of blocks. You can drag and drop these blocks on the righthand side to create the flow. Let's start by creating a Play prompt. Whenever a customer calls in, this prompt will be played to greet the customer.Drag and Drop thr Play Prompt to the righthand side, enter the Message to be played and Publish the flow. 
<p align="center">
<img src="https://imgur.com/mncV6Jy.png" height="80%" width="80%"> <br/>

22. Lets get the customer input to direct them to the desired service. Enter the message to be displayed while getting the input and add three options.
<p align="center">
<img src="https://imgur.com/LfvXQoA.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/e1Apskl.png" height="80%" width="80%"> <br/>

23. Next step is to add the transfer flows to Sales, Technical Support and Order Status queues. The flow will be directed to the queues when the desired option is pressed. Connect the entry points and also connect the error points to disconnect.
<p align="center">
<img src="https://imgur.com/WxvFsEL.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/sBAU8GQ.png" height="80%" width="80%"> <br/>

24. Lets proceed by Creating the contact flow for Sales. Under the Routing menu, select Flows option and click on Create Contact Flow. Give the name for the flow as Sales. From the lefthand side of the menu, drag and drop the set working queue block on the righthand side and select the queue as the Sales queue. Transfervthe call to the Agent by adding the Transfer to Queue block and lastly connect the errors to a disconnect block and Publish the flow.
<p align="center">
<img src="https://imgur.com/8bu2GR0.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/L7hPz91.png" height="80%" width="80%"> <br/>

25. Similarly, lets add the Contact Flow for Technical Support.
<p align="center">
<img src="https://imgur.com/fPfVBlO.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/4lewfY4.png" height="80%" width="80%"> <br/>

26. To Check the Order Status for the customer, we need to get the Order Number as the Customer Input, invoke a Lamda Function that fetches the order status and issue it to the Play Promt which will play the Order Status and then Discoonect the call.
<p align="center">
<img src="https://imgur.com/En64lB1.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/NyGMjok.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/Zw5ysB4.png" height="80%" width="80%"> <br/>

27. Lets Create the Lamda Function to get the Order Status. From the AWS Console, go the AWS Lamda service. Click on Create Function.
Enter the Name of the Function, Runtime as Python 3.9 and click Create Function.
<p align="center">
<img src="https://imgur.com/HqcQ8Nz.png" height="80%" width="80%"> <br/>

28. Now, select the Function created and Scroll down to the Code Source section. The code for this Lamda Function is given above in the LamdaFunctionCode.txt file. Just copy all the code and paste it in the code block and Deploy the code.
<p align="center">
<img src="https://imgur.com/Y36j174.png" height="80%" width="80%"> <br/>

29. To Add the Function to the Contact Flow, click on our Instance in the Amazon Connect console and scroll down to the AWS Lamda block. Select the Lamda Function and Add it and Copy the ARN.
<p align="center">
<img src="https://imgur.com/pGX3oUV.png" height="80%" width="80%"> <br/>

30. Scroll back to the Order Status Flow. Click on the Invoke Lamda Function and add the Lamda Function we just created. Click on Add Paramters and provide OrderNo as the destination key. Select the value to be entered Dynamically. Namespace as system and value as Stored Customer Input and click on Save.
<p align="center">
<img src="https://imgur.com/hq66ZEU.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/JxILwvB.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/Q0HXE8s.png" height="80%" width="80%"> <br/>

31. Next Step would be to add all the Contact Flows we created to the Main Flow. Scroll back to the Main Flow page and Click on the Transfer to Flow promt and select the respective flows for Sales, Technical Support and Order Status.
<p align="center">
<img src="https://imgur.com/AMiQC95.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/F10pEKE.png" height="80%" width="80%"> <br/>

32. The Last step is to claim a Phone Number for our instance. On the Dashboard, under the Channels menu select Phone Numbers. Click on Claim  Number. Select the type as Direct Inward Dialing (DID), Enter the country code and Select the Number. 
<p align="center">
<img src="https://imgur.com/Mh0l6BA.png" height="80%" width="80%"> <br/>
<p align="center">
<img src="https://imgur.com/CiPmMhd.png" height="80%" width="80%"> <br/>


<h2>Benefits of Building a Call Center in AWS using Amazon Connect and Lex:</h2>

1. Scalability: AWS services allow the call center solution to scale up or down based on call volume and agent availability, ensuring optimal performance and customer satisfaction.

2. Cost-effectiveness: With pay-as-you-go pricing and the ability to provision resources as needed, AWS provides a cost-effective solution for building and operating a call center.

3. Automation and efficiency: By leveraging Amazon Lex for automated responses and natural language understanding, the call center can handle a large volume of customer inquiries efficiently, reducing the need for human intervention.                             

4. Integration and extensibility: AWS services, such as Lambda, allow for seamless integration with other systems and the ability to extend the functionality of the call center solution as needed.

5. Real-time analytics: With CloudWatch monitoring and logging, the call center can gain real-time insights into call center performance, agent productivity, and customer satisfaction, enabling continuous improvement.
<br/>
<p align="center">
<img src="https://imgur.com/mncV6Jy.png" height="80%" width="80%"> <br/>
