# Amazon Kinesis Data Analytics

Amazon Kinesis Data Analytics is the easiest way to transform and analyze streaming data in real time with Apache Flink. Apache Flink is an open source framework and engine for processing data streams. Amazon Kinesis Data Analytics reduces the complexity of building, managing, and integrating Apache Flink applications with other AWS services.

Amazon Kinesis Data Analytics takes care of everything required to run streaming applications continuously, and scales automatically to match the volume and throughput of your incoming data. With Amazon Kinesis Data Analytics, there are no servers to manage, no minimum fee or setup cost, and you only pay for the resources your streaming applications consume.


## Goal

To setup and configure your application with Amplify Analytics and record an analytics event.

## Prerequisites

1- Install and configure Amplify CLI

2- An iOS application targeting at least iOS 11.0 with Amplify libraries integrated
For a full example of creating a iOS Xcode project, please follow project setup walkthrough

## Set up Analytics backend

Run the following command in your project's root folder. The CLI will prompt configuration options for the Analytics category such as Amazon Pinpoint resource name and analytics event settings.

```
amplify add analytics
```

```
amplify push
```

