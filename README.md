
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
- Python 3 .
  
Optional:
- Docker for local testing.

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/rajnishshaw/sam-world.git
cd sam-world
```

### 2. Build

You can build the project using SAM CLI.

```bash
sam build
```

### 3. Test Locally (Optional)

You can test the function locally using the SAM CLI.

```bash
sam local start-api
```

Then, you can use browser, `curl` command or Postman to hit the local API endpoint.
```bash
http://localhost:3000/hello
```

### 4. Deploy to AWS:


```bash
sam deploy --guided
```
Please provide the info as per prompt.

After the deployment is successful, the API endpoint will be displayed in the Outputs section of the terminal.you can use browser, `curl` command or Postman to hit the local API endpoint.



## Cleanup

To delete the sample application that you created, use the AWS CLI. Assuming you used your project name for the stack name, you can run the following:

```bash
sam delete --stack-name "helloSAM"
```

## License

This project is open-source and available under the MIT License.

