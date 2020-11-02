# 6. Topics will be created using Amazon Simple Notificatio Service (SNS) to enable commmunication via SMS

## Status
Pending

## Context
Users require to receive item availablity via SMS.

## Decision
We decided to use SNS as our SMS server in order to send message to users regarding item availability. 

## Consequence
This service supports other type of communications allowing us to use the same service for multiple communication methods such as SMS, email, and others. 
