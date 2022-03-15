
!!!
sam sync --stack-name blog --code --resource AWS::Serverless::Function
!!!

You can further limit the synchronized resources by using the `--resource` flag with the `--code` flag:

This command limits the synchronization to Lambda functions

```
sam sync --stack-name blog --code --resource AWS::Serverless::Function

```
Other available resources are `AWS::Serverless::Api`, `AWS::Serverless::HttpApi`, and `AWS::Serverless::StateMachine`.

