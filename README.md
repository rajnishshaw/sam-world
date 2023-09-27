
# Overview
AWS Serverless Application Model (SAM) is an extension of AWS CloudFormation that makes it easier to build and deploy serverless applications. SAM provides a simplified way to define the AWS resources needed for a serverless application, including Lambda functions, API Gateway APIs, and DynamoDB tables.

# Benefits :

**Simplified development:** SAM can help you to develop serverless applications more quickly and easily.

**Reduced errors:** SAM's higher-level syntax can help to reduce the risk of errors in your templates.

**Increased productivity:** SAM provides a number of features that can help you to be more productive, such as the ability to test your applications locally and to deploy them with a single command.

# About Project helloSAM

This project contains source code and supporting files for a serverless application that you can deploy with the SAM CLI. It includes the following files and folders.

- hello_world - Code for the application's Lambda function.
- events - Invocation events that you can use to invoke the function.
- tests - Unit tests for the application code. 
- template.yaml - A template that defines the application's AWS resources.

The application uses several AWS resources, including Lambda functions and an API Gateway API. These resources are defined in the `template.yaml` file in this project. You can update the template to add AWS resources through the same deployment process that updates your application code.

## Prerequisites

- [AWS CLI](https://aws.amazon.com/cli/) installed and configured.
- [AWS SAM CLI](https://aws.amazon.com/serverless/sam/) installed.
- Python 3.6 or higher.
  
Optional:
- Docker for local testing.

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/your-repo-url
cd your-repo-folder
```

### 2. Initialize SAM Project (If starting from scratch)

```bash
sam init --runtime python3.9 --name my-http-api-runtime-info
```

### 3. Navigate to the Project Directory

```bash
cd my-http-api-runtime-info
```

### 4. Test Locally (Optional)

You can test the function locally using the SAM CLI.

```bash
sam local start-api
```

Then, you can use `curl` or Postman to hit the local API endpoint.

### 5. Deploy the API

First, package the application:

```bash
sam package --output-template packaged.yaml
```

Next, deploy it to AWS:

```bash
sam deploy --template-file packaged.yaml --stack-name my-http-api-runtime-info-stack --capabilities CAPABILITY_IAM
```

After the deployment is successful, the API endpoint will be displayed in the Outputs section of the terminal.



## Cleanup

To delete the sample application that you created, use the AWS CLI. Assuming you used your project name for the stack name, you can run the following:

```bash
sam delete --stack-name "hellosam"
```

## License

This project is open-source and available under the MIT License.

