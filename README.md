![License](https://img.shields.io/badge/license-MIT-blue.svg)  
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)  

# sctp-wk14-2.14-serverless

## Table of Contents
- [Does SNS guarantee exactly deliver once to subscribers?](#1)
- [What is the purpose of the Dead-letter Queue (DLQ)? This is a feature available to SQS/SNS/EventBridge?](#2)
- [How would you enable a notification to your email when messages are added to the DLQ?](#3)

<a id="1"></a>
### Does SNS guarantee exactly deliver once to subscribers?
```
No, Amazon Simple Notification Service (SNS) doesn't guarantee that messages will be delivered to subscribers. Instead, SNS uses a best-effort delivery mechanism. 
Explanation
•	SNS matches messages to subscribers who have subscribed to a topic. 
•	SNS attempts to deliver messages in the order they were published. 
•	SNS retries failed deliveries using a backoff function. 
•	SNS doesn't support native mechanisms to ensure that messages are received only once. 
```
<a id="2"></a>
### What is the purpose of the Dead-letter Queue (DLQ)? This is a feature available to SQS/SNS/EventBridge?
```
The Dead-letter Queue (DLQ) is a feature available in Amazon SQS, Amazon SNS, and Amazon EventBridge that helps improve the resiliency and reliability of message processing systems.

The main purpose of a Dead-letter Queue is to capture messages that could not be processed successfully after multiple retry attempts. This prevents the system from losing messages or continuously retrying indefinitely, which could cause performance issues.

```
<a id="3"></a>
### How would you enable a notification to your email when messages are added to the DLQ?
```
Amazon Simple Notification Service (SNS) with Amazon CloudWatch alarms can be used to enable email notifications when messages are added to the Dead-letter Queue (DLQ) in AWS.
```

