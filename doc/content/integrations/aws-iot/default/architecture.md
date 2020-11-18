---
title: "Architecture"
description: ""
weight: 10
---

The AWS IoT Core integration is a serverless deployment that scales automatically as your deployment grows.

<!--more-->

![Default integration architecture](../architecture.svg)

The key resources deployed in your AWS account are:

- Cross-account role for {{% tts %}} to connect to your AWS IoT Core MQTT endpoint;
- AWS Lambda functions to create the thing type and configure the integration as pub/sub in {{% tts %}};
- AWS Lambda functions for claiming and creating devices, and for handling uplink and downlink messages;
- IoT Core rules to trigger the Lambda functions based on topics and attributes.

This is a serverless deployment: there are no compute resources being deployed. AWS only charges for usage, which is driven by traffic. The only continuous charges are by IoT Core connectivity from {{% tts %}} to your AWS account. All permissions are the minimum permissions for the integration to function.
