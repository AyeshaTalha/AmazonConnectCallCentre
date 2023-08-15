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
    
<p align="center">
Seting up Identity for the Instance<br/>
<img src="https://imgur.com/wyRDc8C.png" height="80%" width="80%"><br/>
    
<p align="center">
Creating the Administrator for the instance.This Admin will be used to login on our website later. So do remember the username and password <br/>
<img src="https://imgur.com/7OVujrX.png" height="80%" width="80%"><br/>
    
<p align="center">
Seting up the Telephony: <br/>
<img src="https://imgur.com/gWWE6xO.png" height="80%" width="80%"><br/>
    
<p align="center">
You can view the S3 Bucket where your Instance Data is Stored. Scroll Down and Press Next.<br/>
<img src="https://imgur.com/nYBy4sz.png" height="80%" width="80%"><br/>
    
<p align="center">
Review all your data, Scroll Down and Press Create Instance. <br/>
<img src="https://imgur.com/YLDGfLZ.png" height="80%" width="80%">
<br/>

<p align="center">
Click on the Access URL of the Instance And Use the Admin User And Password Which We Set Up Earlier To Sign In<br/>
<img src="https://imgur.com/Dd6vG2K.png" height="80%" width="80%"> <br/>

<p align="center">
The Next Step is To Set Hours Of Operation. On the Dashboard Click On the Routing Option And Select Hours Of Operation<br/>
<img src="https://imgur.com/ukjoJ1V.png" height="80%" width="80%"><br/>

<p align="center">
Click on Add New Hours. Set a name, Select the Preferred Time Zone And Tht Number Of Working Days.<br/>
<img src="https://imgur.com/lW4XEp6.png" height="80%" width="80%"><br/>

<p align="center">
Now we Need to Set Up the Queues. On the Dashboard under the Routing Option, Select Queues.<br/>
<img src="https://imgur.com/DRDYjE1.png" height="80%" width="80%"><br/>

<p align="center">
Click on Add Queues. Name the Queue as Technical Queue and Select the Hours Of Operation as NineToFive.<br/>
<img src="https://imgur.com/9aXeKGg.png" height="80%" width="80%"><br/>

<p align="center">
Lets Add Another Queue For Sales. Name the Queue as Sales and Select the Hours Of Operation as Basic Hours.<br/>
<img src="https://imgur.com/ykuFNXi.png" height="80%" width="80%"><br/>

<p align="center">
Now we Need to Set Up the Routing Profiles.On the Dashboard Under the Users Menu Select Routing Profiles.<br/>
<img src="https://imgur.com/cH6ToMJ.png" height="80%" width="80%"><br/>

<p align="center">
Click on Add Routing Profile and Add A Sales Routing Profile.Tick the Channel Box to Voice and Select Sales Queue under the Queues bar.<br/>
<img src="https://imgur.com/oQ7IDlN.png" height="80%" width="80%"><br/>
<img src="https://imgur.com/6tDKWhq.png" height="80%" width="80%><br/>
4. Create Amazon Lex bots: Design and build conversational bots using Amazon Lex. Define intents, slots, and utterances to handle different types of customer inquiries and automate responses.

5. Integrate Amazon Connect and Lex: Configure Amazon Connect to use Amazon Lex bots for handling customer interactions. Set up call flows and routing rules to direct calls to the appropriate Lex bot based on customer inputs.

6. Develop custom Lambda functions: Write and deploy Lambda functions to extend the functionality of Amazon Connect and Lex. This can include custom logic for call routing, data retrieval from external systems, or integration with other AWS services.

7. Store call center data: Set up S3 buckets to store call recordings, transcripts, and other media assets generated during call center interactions. Configure permissions and access control for secure storage.

8. Monitor and analyze: Use CloudWatch to monitor the performance and health of the call center solution. Set up alarms and notifications for critical metrics, such as call wait times or system failures. Analyze call center data to gain insights and improve customer service.
<h2>Benefits of Building a Call Center in AWS using Amazon Connect and Lex:</h2>

1. Scalability: AWS services allow the call center solution to scale up or down based on call volume and agent availability, ensuring optimal performance and customer satisfaction.

2. Cost-effectiveness: With pay-as-you-go pricing and the ability to provision resources as needed, AWS provides a cost-effective solution for building and operating a call center.

3. Automation and efficiency: By leveraging Amazon Lex for automated responses and natural language understanding, the call center can handle a large volume of customer inquiries efficiently, reducing the need for human intervention.                             

4. Integration and extensibility: AWS services, such as Lambda, allow for seamless integration with other systems and the ability to extend the functionality of the call center solution as needed.

5. Real-time analytics: With CloudWatch monitoring and logging, the call center can gain real-time insights into call center performance, agent productivity, and customer satisfaction, enabling continuous improvement.
<br/>
