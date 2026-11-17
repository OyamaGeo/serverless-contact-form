# Serverless Contact Form – AWS

A serverless contact form application built using Amazon API Gateway, AWS Lambda, Amazon DynamoDB and Amazon SNS.

## Project Overview

This project demonstrates the design and implementation of an event-driven, serverless contact form application using Amazon Web Services (AWS).

The application provides an API endpoint through which users can submit contact messages. AWS Lambda processes incoming requests, stores submitted information in DynamoDB and triggers email notifications through Amazon SNS.

The project demonstrates practical experience with serverless architecture, AWS service integration, IAM permissions, application troubleshooting and cloud monitoring.

## System Architecture

The application follows a serverless, event-driven architecture that uses managed AWS services to process and store contact form submissions without requiring dedicated server infrastructure.

### Architecture Diagram

![Serverless Contact Form Architecture](architecture.png)

### Application Workflow

1. **User Submission:** A user submits a contact form request through the API endpoint.
2. **API Gateway:** Amazon API Gateway receives the HTTP POST request through the `/submit` endpoint.
3. **Request Processing:** AWS Lambda processes and validates the incoming request.
4. **Data Persistence:** Lambda stores the contact submission in an Amazon DynamoDB table.
5. **Notification Trigger:** Lambda publishes a notification message to an Amazon SNS topic.
6. **Email Notification:** Amazon SNS delivers an email notification to confirmed subscribers.

## AWS Services Used

| AWS Service | Purpose |
|---|---|
| Amazon API Gateway | Provides the HTTP API endpoint for contact submissions. |
| AWS Lambda | Processes requests and coordinates application operations. |
| Amazon DynamoDB | Stores submitted contact form information. |
| Amazon SNS | Sends email notifications when submissions are received. |
| AWS IAM | Controls permissions and secure access between AWS services. |
| Amazon CloudWatch | Collects execution logs for monitoring and troubleshooting. |

## Implementation

The application was implemented by integrating multiple AWS services into a complete serverless workflow.

Key implementation activities included:

- Configuring an API Gateway endpoint to receive HTTP POST requests.
- Developing a Lambda function to process contact form submissions.
- Integrating DynamoDB for persistent storage.
- Configuring SNS to deliver email notifications.
- Establishing IAM permissions for Lambda to interact with the required AWS services.
- Using CloudWatch logs to monitor Lambda execution and investigate application errors.

## Testing and Troubleshooting

During implementation, several integration and configuration issues were identified and resolved.

The troubleshooting process covered:

| Issue Identified | Resolution |
|---|---|
| Missing `uuid` dependency | Corrected the Lambda deployment package to include the required dependency. |
| DynamoDB write permission errors | Updated the Lambda execution role permissions. |
| SNS publish permission errors | Corrected IAM permissions for SNS publishing. |
| Unconfirmed SNS email subscription | Confirmed the email subscription. |
| Lambda timeout configuration | Reviewed and adjusted the function timeout. |
| API Gateway integration errors | Tested and corrected the API integration configuration. |

CloudWatch execution logs were used to identify errors, investigate root causes and verify successful function execution.

IAM permissions were reviewed and adjusted to follow the principle of least privilege.

## Results and Validation

The completed application successfully demonstrated the end-to-end contact submission workflow.

Verified outcomes included:

- API Gateway successfully returned HTTP `200 OK` for a successful submission.
- Contact form submissions were stored in DynamoDB.
- SNS successfully published notification messages.
- Email notifications were delivered to confirmed subscribers.

These results demonstrate successful integration between the API, compute, database and notification components.

## Security and Reliability Considerations

The project incorporates important AWS cloud engineering practices:

- IAM-based access control between AWS services.
- Permission management for Lambda execution roles.
- CloudWatch logging for operational visibility.
- Managed serverless services to reduce infrastructure administration.
- Structured testing to identify and resolve integration failures.

For production deployment, additional considerations include API authentication, request validation, input sanitisation, protection against abuse, sensitive-data handling and appropriate monitoring.

## Technical Skills Demonstrated

- AWS Serverless Architecture
- Amazon API Gateway
- AWS Lambda
- Amazon DynamoDB
- Amazon SNS
- AWS IAM
- Amazon CloudWatch
- API Integration and Testing
- Cloud Troubleshooting
- IAM Permission Management
- Root Cause Analysis

## Key Takeaways

This project strengthened my practical understanding of how independently managed AWS services work together to deliver a complete application.

It also provided hands-on experience in diagnosing service integration failures, analysing execution logs, resolving IAM permission issues and validating an end-to-end serverless workflow.

**Project Focus:** AWS Cloud Engineering | Serverless Computing | Application Integration | Troubleshooting
