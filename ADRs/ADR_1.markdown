# 1. CloudWatch events to schedule AWS Lambda Functions. To be used for triggering polling to external APIs

## Status
Accepted

## Context
Client has stated that external sources (such as Smart Fridges and Point of Sale) can communicate using their own API. 

![Image of Context](https://github.com/sebfault/architecure-kata-sandbox/blob/master/ADRs/images/imageSource1.PNG)

## Decision
This serverless architecture can use seperate lambda functions to poll and communicate data from external APIs.
Multiple lambdas can be scheduled to execute on a customized rate (i.e: hit external API endpoint x every y minutes).

If any new system is introduced, the system can simply add another lambda function.
In terms of scaling, AWS lambda functions scales automatically if needed.

## Consequence

There exists a possibilty to not get most updated data when an event happens in between schedule intervals.
This limitation is addressed in ADR 2. Otherwise, the scheduling rate can be adjust to minimize this scenario