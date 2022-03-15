You can target one specific resource with the `--resource-id` flag to get more granular:

```
sam sync --stack-name blog --code --resource-id HelloWorldFunction
```
This time sam sync ignores the HelloGhanaFunction and only updates the HelloWorldFunction declared with the command’s--resource-id flag.
<br />
Or
```
sam sync --stack-name blog --code --resource-id HelloGhanaFunction
```