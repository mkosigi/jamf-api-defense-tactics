# jamf-api-defense-tactics
Resources and best practices for securely managing credentials in Jamf API calls. Covers risks, mitigation strategies, and tools like Jamf Pro webhooks, AWS API Gateway, AWS Secrets Manager, AWS EventBridge and Lambda functions for secure API authentication.

## Resources
### [Jamf Pro Webhooks](https://developer.jamf.com/developer-guide/docs/webhooks)
Learn how to use Jamf Pro webhooks to automate tasks and integrate with other systems by sending real-time data to specified endpoints.
### [Jamf Pro Extension Attributes](https://developer.jamf.com/developer-guide/docs/extension-attributes)
Understand how to use extension attributes in Jamf Pro to collect custom data from managed devices, enhancing your device management capabilities.
### [Jamf Pro API Overview](https://developer.jamf.com/jamf-pro/docs/jamf-pro-api-overview)
Get an overview of the Jamf Pro API, including authentication, endpoints, and examples to help you interact programmatically with Jamf Pro.
### [Jamf Pro SDK for Python](https://github.com/macadmins/jamf-pro-sdk-python)
A python client library for the Jamf Pro APIs and webhooks.
### [AWS API Gateway Documentation](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html)
Explore AWS API Gateway, a fully managed service that makes it easy to create, publish, maintain, monitor, and secure APIs at any scale.
### [Using AWS Lambda Authorizers with API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-use-lambda-authorizer.html)
Learn how to use AWS Lambda functions as authorizers for API Gateway to control access to your APIs.
### [AWS EventBridge API Gateway Target](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-api-gateway-target.html)
Discover how to use Amazon EventBridge to route events to API Gateway targets, enabling event-driven architectures.
### [AWS EventBridge Event Bus](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-event-bus.html)
Understand the concept of an event bus in Amazon EventBridge and how it can be used to manage and route events.
### [AWS EventBridge Rules](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-rules.html)
Learn how to create rules in Amazon EventBridge to match incoming events and route them to targets for processing.
EventBridge Rule Example: 

```json
{
"detail": {
"event": {
"groupAddedDevicesIds": [{
"exists": true
}],
"jssid": [11] 
}
},
"detail-type": ["UpdateEAFromAssetTag"],
"source": ["com.jamf.dev"]
}
```
The above rule will match webhook requests for the smart group with jssID 11, if there is any new device added to the group. Additionally, the `detail-type` and `source` must also match.

### [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
Get started with AWS Lambda, a serverless compute service that lets you run code without provisioning or managing servers.
### [AWS Lambda with Python](https://docs.aws.amazon.com/lambda/latest/dg/lambda-python.html)
Explore how to write AWS Lambda functions in Python, including setup, deployment, and best practices.
### [AWS Secrets Manager Documentation](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html)
Learn about AWS Secrets Manager, a service to help you protect access to your applications, services, and IT resources without the upfront cost and complexity of managing your own hardware security module (HSM) infrastructure.
