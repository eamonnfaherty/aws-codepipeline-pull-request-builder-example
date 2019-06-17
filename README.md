# pr-builder
# Description
This sample will create a pull request builder using source code from Github.com and using AWS Codebuild as the CICD
tool.


## Parameters
The list of parameters for this template:

### Owner 
Type: String 
Default: eamonnfaherty 
Description: The Owner of the github.com repo 
### Repo 
Type: String 
Default: aws-codepipeline-pull-request-builder-example 
Description: The name of the github.com repo 
### BuildSpecFileName 
Type: String 
Default: pr-builder-buildspec.yaml 
Description: The name of the buildspec to use from the github repo 
### OAuthResourceArn 
Type: String  
Description: The Arn of the credentials resource to use.  You can generate an Arn by importing your credentials using:
``` bash
aws codebuild import-source-credentials
```
 

## Resources
The list of resources this template creates:

### BuildRole 
Type: AWS::IAM::Role 
Description: The IAM Role used to run the codebuild job.  Customise this if you need add extra permissions. 
### BuildProject 
Type: AWS::CodeBuild::Project  

## Outputs
The list of outputs this template exposes:

