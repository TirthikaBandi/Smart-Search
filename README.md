# Smart-Search

SMART SEARCH is an application that simplifies your searches of content in videos. In case you are looking for a particular topic inside a lecture video you don't have to waste time navigating through the whole video looking for that specific part SMART SEARCH will do it for you. You can just type in the topic and get to the part of the video where the topic has been talked about by clicking on the timestamp thus generated. So storing the user data and the lectures and deploying an application will be a good option. For deploying this application I will use AWS platform.


# Services to be used:

AWS media and AI/ML services:

•	Amazon Transcribe: An automatic speech recognition (ASR) service that makes it easy for you to add speech-to-text capability to your applications.
•	Amazon Elastic Transcoder: Media transcoding in the cloud. It is designed to be a highly scalable, easy-to-use, and cost-effective way for you to convert (or “transcode”) media files from a source format. You can create versions that play back on devices like smartphones, tablets, and PCs.
•	Amazon CloudSearch: A managed service in the AWS Cloud that makes it simple and cost-effective to set up, manage, and scale a search solution for your website or application.

# Other AWS Services:

•	AWS Lambda: Lets you run code without provisioning or managing servers. You pay only for the compute time that you consume.
•	Amazon API Gateway: A fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale.
•	Amazon S3: An object storage service that offers industry-leading scalability, data availability, security, and performance.

# Solution:

This solution gets created in three parts:

•	User interactive frontend:
o	Creating a profile.
o	Uploading dashboard with lectures.
•	Ingesting the AV file:
o	Uploading the MP4 file to an S3 bucket.
o	Transcoding the media file into audio format.
o	Transcribe the audio file into text.
o	Indexing the contents into Amazon CloudSearch.
o	Testing the index in CloudSearch.
•	Searching for content:
o	Creating a simple HTML user interface for querying content.
o	Listing the results and rendering them from an S3 bucket using CloudFront.
