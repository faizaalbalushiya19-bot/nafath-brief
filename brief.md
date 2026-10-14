Version: NAFATH-V2
Track:  Data

## Overview
The emergency 5G service relies on a combination of six different IT domains to ensure reliable communication. The software will be responsible for the manner in which applications make requests and retries without making any unwanted alterations. Artificial intelligence enables the prediction of network congestion, while cross-validation enables the confirmation of whether the predictions apply effectively to new data. The mobile applications must be functional even when there is no connectivity and should synthesize the information once the connectivity is regained. The networking domain employs 5G network slicing to segment and prioritize the emergency traffic. The cybersecurity domain offers a systematic approach to cyber attacks by enabling containment and restoration. The data engineering domain structures the information about the usage such that the service activities can be compared across regions and days.

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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
