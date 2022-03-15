# Sam sync

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

### Using sam sync (no options)
The `sam sync` command with no options deploys or updates all infrastructure and code like the sam deploy command.
So underneath, `sam sync` runs `sam build`, then synchronizes your application to the cloud.

```
sam sync --stack-name sam-workshop-basic
```
Let's see it in Action. Go to your application and run the above code from the terminal.

