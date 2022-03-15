# Sam sync watch
!!!
sam sync --stack-name sam-workshop-basic --watch
!!!

The `sam sync --watch` option tells AWS SAM to monitor for file changes and automatically synchronize when changes are detected.
If the changes include configuration changes, AWS SAM performs a standard synchronization equivalent to the `sam sync` command.
If the changes are code only, then AWS SAM synchronizes the code with the equivalent of the `sam sync --code` command.

The first time you run the `sam sync` command with the  `--watch` flag, AWS SAM ensures that the latest code and infrastructure are in the cloud. 
It then monitors for file changes until you quit the command:

Run the `sam sync --stack-name sam-workshop-basic --watch` command, watch the application build and sync with the cloud. 

Then make a change in any lambda handler, hit save and watch the code autosync