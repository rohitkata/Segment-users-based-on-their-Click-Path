# Segment-users-based-on-their-Click-Path

## Introduction:

Online services are increasingly becoming dependent on their visitor participation to understand their customers’ behavior. This study focuses on understanding the customer journey from the lens of website state-to-state clicks. Our solution provides a way to segment the customer based on clickstream data and helps understand unique journey patterns taken by a customer group
The various potential paths to traverse on the web platform led to almost no user having identical journeys. To address this, we developed a model to estimate if customer's journeys were similar enough and then grouped all users with similar journeys into their own segment.

## Rationale for this approach:

The main rationale for coming up with this approach was to reduce the complexity, reduce processing time and increase the number of customers that can be clustered. Generally, for this kind of clustering problems, the first step is to find pair wise scores and then use that score to cluster users into segments. Say, you have 20,000 customers. You will have to compare customer 1 with every other customer. This could lead to 20000 square calculations which is computationally very expensive. With addition of new customers, there will be an exponential increase in calculations. This method espouses this traditional approach and can can be utilized for large number of customers.

## Methodology

Step 1: Obtain a customer matrix for every customer. Customer matrix captures the event sequence of the user in the order they occur

Step 2: Collate all the customer matrices to obatin a Final Matrix. Final matrix captures the event sequence of the all the users in the order they occur

Step 3: Feed the final matrix as an input for K- means clustering. Alternately, utilize cosine similarity distance in K- means algorithm rather than Euclidean distance.

## Results

I was succesfully able to cluster 20,000 customers into 4 segments. Each segment represented unique characteristics.
