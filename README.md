# Python Backend Service for AWS CI/CD 

This project serves as a guide for executing a Jenkins pipeline within an AWS setting utilizing AWS DevOps resources like CodeBuild, S3 Buckets, and CodeDeploy.



## appspec.yml :  Application Specification File
The AppSpec file, a YAML or JSON formatted document, is integral for CodeDeploy to manage deployments. This file needs to be located at the root directory of your application's source code. CodeDeploy utilizes the AppSpec file to:


* Dictate the elements to be installed from Amazon S3 or GitHub repositories on instances.
* Determine the lifecycle event hooks to execute in relation to the deployment lifecycle events. These events generally include starting and stopping application scripts.


## buildspec.yml: Build Specification File
A build spec, framed in YAML, comprises build commands and relevant settings, which CodeBuild leverages to carry out a build. The Buildspec YAML file is part and parcel of the source code. This self-explanatory file enables necessary installations by accessing the EC2 instance console directly. It also copies the listed artifacts to designated directories before the CodeDeploy deployment phase starts.



