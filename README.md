# Braintree subscription with Appbase

![alt tag](http://g.recordit.co/iD9jgKlLZx.gif)  

First install the node packages by running following command:
```
npm install
```   

To Start the server:
```
npm start
```    

To Build it for production:
```
npm run build
```   


## Dive into Codebase

Appbase and Braintree can be really powerful to update the pricing plan of the user on the certain condition. For this project, we are changing the pricing plan of the user based on the number of API calls made by the user. One can simulate the number of API calls from the frontend module.


The integration is divided into two sub modules:
 - Frontend Module: Simulates the API call and update the value in Appbase
 - Backend Module: Webhooks make the request to server and server updates the pricing plan for the user in the braintree.

 When you update number of API call, it gets updated in the Appbase. In Appbase, webhooks are configured on the threshold that defines the pricing plan. So when the condition is made, the request is made on the backend module. 

 To configure the webhooks, one is required to run the curl statement that are available in the webhook file.

 This project ends the polling to check if the number of API calls has reach the threashold to change the pricing plane which otherwise would have required.