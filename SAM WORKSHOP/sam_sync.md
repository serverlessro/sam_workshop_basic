# SAM SYNC

The command `sam sync`  synchronizes your project declared in an AWS SAM template to the AWS Cloud.
`sam sync` breaks down the project into 2 parts.
- Code 
- Configuration 

### Code
`sam sync` considers the following as Code
- lambda function Code
- lambda layer code
- Step functions amazon states language
- Api gateway Open API

### Configuration
- Everything else

Let's make an update to our lambda function and use the `sam sync` command to push the update to the cloud in seconds.
```python
 {
        "statusCode": 200,
        "body": json.dumps({
            "message": "hello world",
            # "location": ip.text.replace("\n", "")
        }),
    }
```

to 

```python
 {
        "statusCode": 200,
        "body": json.dumps({
            "message": "hello world, Welcome to Ghana AWS Meetup",
            # "location": ip.text.replace("\n", "")
        }),
    }
```
Now, run the command `sam sync --stack-name {stack-name} --code` and watch the app deploy under 10 seconds 

![](../img/f.png)
![](../img/g.png)

The sam sync command verifies each of the code types present and synchronizes the sources to the cloud. 
This example uses an API Gateway REST API and two Lambda functions. 
AWS SAM skips the REST API because there is no external OpenAPI file for this project. 
However, the Lambda functions and their dependencies are synchronized.

You can limit the synchronized resources by using the `--resource` flag with the `--code` flag:

This command limits the synchronization to Lambda functions

```
sam sync --stack-name blog --code --resource AWS::Serverless::Function

```
Other available resources are `AWS::Serverless::Api`, `AWS::Serverless::HttpApi`, and `AWS::Serverless::StateMachine`.

You can target one specific resource with the `--resource-id` flag to get more granular:

```
sam sync --stack-name blog --code --resource-id HelloWorldFunction
```

Or 
```
sam sync --stack-name blog --code --resource-id HelloGhanaFunction
```