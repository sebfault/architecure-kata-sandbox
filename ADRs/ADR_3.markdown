# 3. External events/updates will all be normalized before entering API Gateway

## Status
Accepted

## Context
ADR1 and ADR2 require separate processing of the flows. 

## Decision
We decided to use lambda functions to normalize the data from different systems, before being processed into our storage and servers. For each external API data, we will have a lambda function that will receive the data and transform this data into our data model.

## Consequence
This approach will allows us to process data from different sources seemlessly, allowing each individual lamda to be updated and tested independently. 
