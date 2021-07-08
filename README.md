<<<<<<< HEAD

# Cloud Foundry - Hello World Sample using NodeJS

## Description
This is a "Hello World" application for the SAP Cloud Platform Cloud Foundry Environment that spans over several chapters (branches). You will learn:  
- How to develop a simple RESTful API in Node.js
- How to persist data in a PostgreSQL DB
- How to perform authentication and authorization
- How to develop a UI served by the API

## How do I access the tutorial?

This tutorial is in multiple steps.  To view the steps, go to the branch menu, and select one of the steps

![branch menu](img/branch-menu.png)

## Prerequisites
To make this sample application work for you, please make sure you have:
- A basic knowledge of Node.js
- An account on SAP Cloud Platform, for example, a [trial account](https://account.hanatrial.ondemand.com/) you may [sign up](https://account.hanatrial.ondemand.com/register) for. For more information about the Sign up process, see this [blog](https://blogs.sap.com/2017/05/16/sap-cloud-platform-trial-now-includes-cloud-foundry/).

## Download and Installation
Please [clone this project to your local computer](https://help.github.com/articles/cloning-a-repository/).

Then check out the branches one by one in sequence, and follow the instructions from the respective README document.

## Support
This project is 'as-is'. We do not provide support and will not make changes. You are welcome to make changes to improve the project but we are not available for questions or support of any kind. 

## License
Copyright (c) 2017 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, v. 2 except as noted otherwise in the [LICENSE](LICENSE) file.  
=======
# Chapter 1: Basic Implementation of a Node.js Web Service

## Learning Goal
Having finished this chapter, you should be able to run a small Node.js Web service on your local machine and you'll be able to deploy it to SAP Cloud Platform Cloud Foundry Environment.

## Prerequisites
- You [signed up](https://account.hanatrial.ondemand.com/register) for a [trial account](https://account.hanatrial.ondemand.com/) in SAP Cloud Platform, or you have a productive account.
- Once you got your account, you performed the steps described in [Getting Started with Cloud Foundry](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/b8ee7894fe0b4df5b78f61dd1ac178ee.html).
- You have basic knowledge about [Node.js: Development](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/3a7a0bece0d044eca59495965d8a0237.html), for example, [Create a Node.js Application](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/772b45ce6c46492b908d4c985add932a.html) and [SAP NPM Registry](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/fe672690385a4541b45622a9088f4503.html). Please make sure that you bookmark these pages: Later [SAP Node.js Packages](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/92f1bce8f72946c180d198e21f74a68c.html) and [Secure Node.js Applications](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/3a8e4372f8e74d05b4ed03a484865e08.html) are also relevant.
- For more information about working with NPM registry, see this [blog](https://blogs.sap.com/2017/05/16/sap-npm-registry-launched-making-the-lives-of-node.js-developers-easier/).


## Step 1: Configure NPM on your machine to ensure all subsequent NPM calls work.
Execute the following command:
```
npm config set @sap:registry https://npm.sap.com
```

## Step 2: Run the service locally.
- Clone this repo to your machine.  
- In the folder you cloned into, execute the `npm install` command.  
- To start the server, execute the `nodejs server.js` command.  
- To get all users or the details of one user, browse `http://<ip>:8088/users` or `http://<ip>:8088/users/2`.  
- To add another entry to the list of users using the POST operation use, for example, the `Postman` extension of Chrome. (PUT and DELETE are not yet implemented). To test these operations, import the file `SAP-CP-CF_Hello_World.postman_collection.json` from this repository into `Postman`.  


## Step 3: Push to Cloud and run the service.
To log on, access your endpoint with the following command:
```
cf api https://api.cf.eu10.hana.ondemand.com
```
or: 
```
cf api https://api.cf.us10.hana.ondemand.com
```
(depending upon the landscape your account was created in)  
To log on use the following command:
```
cf login
```
If you have access to more than 1 org or space, execute the following command:
```
cf target -o ORG -s SPACE
```
To deploy the application to SAP Cloud Platform Cloud Foundry Environment, execute the following command:
```
cf push --random-route
```
For more information on these commands, see [Getting Started with Cloud Foundry](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/b8ee7894fe0b4df5b78f61dd1ac178ee.html) and [Deploy an Application](http://docs.cloudfoundry.org/devguide/deploy-apps/deploy-app.html).


Check the output of this command, and write down the URL created for the application.  
As a result you should be able to browse `https://<URL for your app>/users`.  
If you want to use the `Postman` collection above, please adjust the URL for the requests in the Cloud folder to the allocated `<URL for your app>`.



>>>>>>> 1a92fe98e87f4e8b6d9fd346d89a52a55c67e0eb


