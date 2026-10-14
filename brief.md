Version: NAFATH-V2
Track:  Data

## Overview
The emergency 5G service relies on a combination of six different IT domains to ensure reliable communication. The software will be responsible for the manner in which applications make requests and retries without making any unwanted alterations. Artificial intelligence enables the prediction of network congestion, while cross-validation enables the confirmation of whether the predictions apply effectively to new data. The mobile applications must be functional even when there is no connectivity and should synthesize the information once the connectivity is regained. The networking domain employs 5G network slicing to segment and prioritize the emergency traffic. The cybersecurity domain offers a systematic approach to cyber attacks by enabling containment and restoration. The data engineering domain structures the information about the usage such that the service activities can be compared across regions and days.
My selected track is Data, focusing on accurate data management and reliable reporting to support emergency response decisions.
## Software
The different HTTP methods differ from each other depending on whether they are safe or idempotent. GET and HEAD methods are called safe since they are intended to retrieve information from the server, whereas the PUT and DELETE methods are idempotent since calling them multiple times produces the same result as calling them once.

Resource: RFC 9110 - HTTP Semantics - https://www.rfc-editor.org/rfc/rfc9110

## AI
Overfitting takes place if the model is trained too precisely to learn even the noise in the training data, and it fails to work effectively on unseen data. The problem of overfitting in the case of the 5G operator may be seen as accurate prediction of congestion on historical data but ineffective prediction when it comes to real-world networks.

Resource: Scikit-learn - Cross-validation: evaluating estimator performance - https://scikit-learn.org/stable/modules/cross_validation.html

## Mobile
The responder's mobile application needs to notify the user when it is offline and save any relevant data locally. This ensures that no update is lost and which actions need to be synchronized are identified by the software. When the connection comes back, the mobile application needs to ensure that it synchronizes properly. Any sensitive data should be secured on the mobile device.

Resource: Android Developers - Offline-first architecture - https://developer.android.com/topic/architecture/data-layer/offline-first

## Networking
Network slicing in the 5G network means that operators can create several virtual networks using the same physical network. Each slice will have its unique parameters, which may include capacity, latency, and dependability. Having a slice dedicated to emergency workers would ensure that these communications will be prioritized, even in the case of network congestion. Moreover, the slice can separate emergency communications from those of consumers. Nevertheless, network slicing is not enough to guarantee connectivity during outages and cyber-attacks.

Resource: 3GPP - Network Slicing - https://www.3gpp.org/technologies/network-slicing

## Cybersecurity
The incident response life cycle comprises of preparation, detection and analysis, containment, eradication, recovery, and lessons learned. In the case of an attack on the emergency 5G service, the teams go through all these phases by adhering to set procedures, detecting any unusual behavior, investigating threats, minimizing harm, eliminating malware, and ensuring that operations become safe once again. In the end, there is an evaluation of the entire incident, as well as improvement in the security controls.

Resource: NIST - Computer Security Incident Handling Guide - https://csrc.nist.gov/pubs/sp/800/61/r2/final

## Data
The star schema contains one central fact table that is connected directly to other dimension tables. The snowflake schema contains normalized dimension tables where the data redundancy is lower. However, for creating more joins, a snowflake schema can be used. In case of creation of the report on 5G service utilization by region and day, a star schema can be considered suitable due to simple understanding and querying of date and region dimensions.

Resource: Microsoft Learn – Star schema guidance – https://learn.microsoft.com/en-us/power-bi/guidance/star-schema

## Misconception in My Track
It is a misconception that a snowflake schema is always a superior choice over a star schema due to reduced redundancy of data. The correct answer really lies in what is needed for the purpose of reporting, complexity of the query, and maintenance. A star schema is generally better suited for reporting purposes since the fact table is directly related to dimension tables. A snowflake schema will have the dimensions normalized into another table, thus reducing the redundancy of data, but with increased number of joins. This makes the star schema suitable for emergency 5G service usage reports based on regions and days.Resource: 1.Microsoft Learn  2.Star schema guidance 

https://learn.microsoft.com/en-us/power

## Open Question
How can the operator detect and remove duplicate usage records to ensure accurate daily reports by region?
