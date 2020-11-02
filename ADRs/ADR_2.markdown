# 2. A Message Queuing service is to be used to subscribe to events and updates via (Amazon Simple Queue Service) SQS 

## Status
Accepted

## Context
Client has stated that external sources (such as Smart Fridges and Point of Sale) can communicate using their own API. 
![Image of Context](https://github.com/sebfault/architecure-kata-sandbox/blob/master/ADRs/images/imageSource2.PNG)

## Decision
For those of the API that support subscription based model, we have decided to have queu service that will subscrube to events. These events are fed into data processing where the data is transformed to common model and send down the pipe.

## Consequence
Event based updates will allow the system to always have live updates as these events occur. The users will have access to the most up to date information about product availablity. 
