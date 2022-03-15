# INTRODUCTION  
### AWS SAM ACCELERATE
AWS SAM(Serverless Application Model) is an open source IaC(Infrastructure As Code) framework created by the AWS Team to help
developers build and test Serverless Applications.
<br />    

It provides a shorthand syntax to express functions, APIs, Databases and Event source mappings.
<br />

When building serverless apps with SAM, we use the SAM CLI to locally build, test and debug applications defined by SAM templates.
<br />

The 2 major commands used to carry out these tasks are `sam build` and `sam deploy --guided`.
<br />

So after making changes to your application, you have to build and deploy the application to the cloud using the above commands.
<br />
Due to the high latency of deploying after each change is made, developers started looking for other options.
Luckily, the SAM Team listened and built **SAM ACCELERATE**.

# WHAT IS SAM ACCELERATE 
> AWS SAM Accelerate aims to increase infrastructure accuracy for testing with sam sync, incremental builds, and aggregated feedback for developers.

It comes with a set of features that aim at reducing deployment latency, and enabling developers to test their code quickly against production AWS services in the cloud.
<br />

Let's Get Started.

