# Build a Serverless Web Application:
  using **AWS Lambda**, **Amazon API Gateway**, **AWS Amplify**, **Amazon DynamoDB**, and **Amazon Cognito**.
  
## Basic Overview:
  We will develop a simple **serverless web application** that will allow users to request rides. In order to submit the request and dispatch a nearby ride, the application will interface with a RESTful web service on the backend and provide users with an HTML-based user interface where they can specify the location where they would like to be picked up. 
  Before requesting rides, users will also be able to register with the service and log in through the application.
  
## Application architecture:
  The application architecture uses **AWS Lambda, Amazon API Gateway, Amazon DynamoDB, Amazon Cognito, and AWS Amplify Console**.
  
  ### Amplify Console, Lambda and API Gateway: 
  Amplify will provides continuous deployment and hosting of the static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser. JavaScript executed in the browser sends and receives data from a public backend API built using **Lambda** and **API Gateway**. 
  
  ### Amazon Cognito: 
  Cognito will provide user management and authentication functions to secure the backend API.
   
  ### DynamoDB: 
  Finally, DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

## Architecture Diagram:
![image](https://user-images.githubusercontent.com/71292230/200560540-4e54df56-2b6d-4a56-a2a6-72ee92f2d798.png)



- **Static Web Hosting**:
AWS Amplify hosts static web resources including HTML, CSS, JavaScript, and image files which are loaded in the user's browser.

- **User Management**:
Amazon Cognito provides user management and authentication functions to secure the backend API.

- **Serverless Backend**:
Amazon DynamoDB provides a persistence layer where data can be stored by the API's Lambda function.

- **RESTful API**:
JavaScript executed in the browser sends and receives data from a public backend API built using Lambda and API Gateway.


### Resources:

https://www.youtube.com/watch?v=5RVT3BN9Iws


https://aws.amazon.com/getting-started/hands-on/build-serverless-web-app-lambda-apigateway-s3-dynamodb-cognito/
