
# Azure Build Pipelines

## References

- https://azure.microsoft.com/en-us/services/devops/pipelines/

- Azure Pipelines Documentation
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops

- What is Azure Pipelines?
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/what-is-azure-pipelines?view=azure-devops
    * "Azure Pipelines is a cloud service that you can use to automatically build and test your code project and make it available to other users."

- Key Concepts
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops

- Getting Started
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops
    * "You define your pipeline in a YAML file called azure-pipelines.yml with the rest of your app."
    * See "Feature Availability" table

- Task Types & Usage
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/process/tasks?view=azure-devops&tabs=yaml
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/?view=azure-devops
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/?view=azure-devops#tool
    * https://github.com/Microsoft/azure-pipelines-tasks

  + Build & Release Tasks:
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/?view=azure-devops
      * Android Signing Build & Release Task
        * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/build/android-signing?view=azure-devops
        
  + Add a Build or Release Task
    * https://docs.microsoft.com/en-us/azure/devops/extend/develop/add-build-task?view=azure-devops

  + Download Pipeline Artifacts task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/download-pipeline-artifact?view=azure-devops

  + Download Secure File Task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/download-secure-file?view=azure-devops

  + Jenkins Queue Job task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/build/jenkins-queue-job?view=azure-devops

  + Jenkins Download Artifacts task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/jenkins-download-artifacts?view=azure-devops

  + File Upload Task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/ftp-upload?view=azure-devops

  + Copy Files Task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/copy-files?view=azure-devops&tabs=yaml
  
  + Publish Pipeline Artifacts task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/publish-pipeline-artifact?view=azure-devops

  + Publish Build Artifacts task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/publish-build-artifacts?view=azure-devops

  + Install Apple Provisioning Profile task
    * https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/utility/install-apple-provisioning-profile?view=azure-devops

- Expressions
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/process/expressions?view=azure-devops#functions
    * Re: https://stackoverflow.com/questions/54931739/task-custom-condition-does-a-given-file-exist
      * "There is no built in condition or function that operates off of the presence or absence of a file."
      * "You can write and run a script that sets a variable, then check the contents of the variable."
      * Example:
        * ```$fileExists = Test-Path -Path "$(System.DefaultWorkingDirectory)/file.txt"```
        * ```Write-Output "##vso[task.setvariable variable=FileExists]$fileExists"```
          * See posting for secondary task 
      


- Integration Applications
  + https://docs.microsoft.com/en-us/azure/devops/integrate/?view=azure-devops
    * "You can build custom applications or services that integrate with your Azure DevOps and Team Foundation Server (TFS) accounts by using the REST APIs to make direct HTTP calls, or utilize our .NET Client Libraries."

  + Service Hooks in Azure DevOps Services
    * https://docs.microsoft.com/en-us/azure/devops/integrate/concepts/service-hooks?view=azure-devops
      * "Using the Subscriptions REST APIs, you can programmatically create a subscription that performs an action on an external (consumer) service when a specific event occurs in a project."

  + Service hook consumers for Azure DevOps Services
    * https://docs.microsoft.com/en-us/azure/devops/service-hooks/consumers?view=azure-devops
      * "Use service hook consumers to programmatically create a subscription. The subscription specifies the event, the consumer and the action. Select the consumer that you want to use in your subscription from the following consumers:..."
        * Web Hooks, POST via HTTP
          * https://docs.microsoft.com/en-us/azure/devops/service-hooks/consumers?view=azure-devops#webhooks

- Specify events that trigger pipelines
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/build/triggers?view=azure-devops
    * CI Triggers in Github
      * https://docs.microsoft.com/en-us/azure/devops/pipelines/repos/github?view=azure-devops&tabs=yaml#ci-triggers


- Notifications
  + https://docs.microsoft.com/en-us/azure/devops/notifications/about-notifications?view=azure-devops
    * "Notifications help you and your team stay informed about activity that occurs within your Azure DevOps projects. You're notified when changes occur to work items, code reviews, pull requests, source control files, and builds. You can be notified via email."


- File matching patterns reference
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/file-matching-patterns?view=azure-devops

- YAML schema reference
  + https://docs.microsoft.com/en-us/azure/devops/pipelines/yaml-schema?view=azure-devops&tabs=schema%2Cparameter-schema
    * "This article is a detailed reference guide to Azure Pipelines YAML pipelines. It includes a catalog of all supported YAML capabilities and the available options."




## Visual Studio Marketplace - Azure DevOps 

- https://marketplace.visualstudio.com/search?target=AzureDevOps&category=Azure%20Pipelines&sortBy=Installs

- AWS Toolkit for Azure DevOps
  + https://github.com/aws/aws-toolkit-azure-devops
  + https://docs.aws.amazon.com/vsts/latest/userguide/welcome.html
  + https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.aws-vsts-tools
    * "Tasks for Amazon S3, AWS Elastic Beanstalk, AWS CodeDeploy, AWS Lambda and AWS CloudFormation and more, and running commands in the AWS Tools for Windows PowerShell module and the AWS CLI."
    * "AWSCLI - Interact with the AWSCLI (Windows hosts only)"
    * "AWS Powershell Module - Interact with AWS through powershell (Windows hosts only)"
    * "Beanstalk - Deploy ElasticBeanstalk applications"
    * "CodeDeploy - Deploy with CodeDeploy"
    * "CloudFormation - Create/Delete/Update CloudFormation stacks"
    * "ECR - Push an image to an ECR repository"
    * "Lambda - Deploy from S3, .net core applications, or any other language that builds on Azure DevOps"
    * "S3 - Upload/Download to/from S3 buckets"
    * "Secrets Manager - Create and retrieve secrets"
    * "SQS - Send SQS messages"
    * "SNS - Send SNS messages"
    * "Systems manager - Get/set parameters and run commands"

- Publishing to Apple Store
  + https://github.com/microsoft/app-store-vsts-extension
    * "Visual Studio Team Services (VSTS) extension for performing continuous delivery to the App Store store from your automated CI builds"
  + https://marketplace.visualstudio.com/items?itemName=ms-vsclient.app-store
    * "Provides tasks for publishing to Apple's App Store from a TFS/Azure DevOps build or release pipeline"
    * "The tasks install and use fastlane tools. fastlane requires Ruby 2.0.0 or above and recommends having the latest Xcode command line tools installed on the MacOS computer."
  + https://github.com/fastlane/fastlane
    * "The easiest way to automate building and releasing your iOS and Android apps"

- AWS S3 Upload
  + https://marketplace.visualstudio.com/items?itemName=MFelling.AWSS3Upload

- File Utilities Build Tasks
  + https://marketplace.visualstudio.com/items?itemName=richardfennellBM.BM-VSTS-FileCopier-Tasks


- Changed files
  + https://marketplace.visualstudio.com/items?itemName=touchify.vsts-changed-files

- Download a file
  + https://marketplace.visualstudio.com/items?itemName=Fizcko.azure-devops-download-a-file

- File Operations
  + https://marketplace.visualstudio.com/items?itemName=KirKone.fileoperations


## Azure DevOps Feature Requests - and possible work-arounds

- Run task if file/directory exists #1877
  + https://github.com/MicrosoftDocs/azure-devops-docs/issues/1877
  + Example cited, using script task
    * ```- bash: |```
    * ```    if [ -f your-file-here.txt ]; then```
    * ```      echo "##vso[task.setVariable variable=FILEEXISTS]true"```
    * ```    fi```
    * ```- task: Foo@1```
    * ```  condition: eq(variables.FILEEXISTS, 'true')```


- Add an exists() on Task Custom Condition
  + https://developercommunity.visualstudio.com/idea/366095/add-an-exists-on-task-custom-condition.html


## Third-Party Solutions

- WinScp
  + SFTP/FTPS file transfers in Microsoft Azure WebJob
    * Re: Azure WebJob
      * https://docs.microsoft.com/en-us/azure/app-service/webjobs-create
    * "Starts immediately when the WebJob is created."
  + https://winscp.net/eng/docs/guide_microsoft_azure_webjob_sftp



## Training Resources

- https://azuredevopslabs.com/



## For Comparison: Jenkins Pipeline Capabilities

- https://www.jenkins.io/doc/book/getting-started/

- https://plugins.jenkins.io/
  + File System Trigger
    * https://github.com/jenkinsci/fstrigger-plugin
    * https://plugins.jenkins.io/fstrigger/
      * "The plug-in makes it possible to monitor changes of a file or a set of files in a folder."

- Pipeline Steps Reference
  + https://www.jenkins.io/doc/pipeline/steps/



## Suggesited Books

- Hands-on Azure Pipelines: Understanding Continuous Integration and Deployment in Azure DevOps 1st ed. Edition (July 2020)
  + https://www.amazon.com/Hands-Azure-Pipelines-Understanding-Integration/dp/1484259017/

- Agile Project Management with Azure DevOps: Concepts, Templates, and Metrics Paperback – (April 2019)
  + https://www.amazon.com/Agile-Project-Management-Azure-DevOps/dp/1484244826/
  
- Operations Anti-Patterns, DevOps Solutions, Jeffrey D. Smith, Manning Publications (MEAP, est. Fall 2020)
  + https://www.manning.com/books/operations-anti-patterns-devops-solutions

- Effective DevOps at Scale, Jennifer Davis, Ryan Daniels, O'Reilly Publishing (2016)
  + https://azure.microsoft.com/en-us/resources/effective-devops/
  + Note: 410 pages, *Free Book*
  

## Articles of possible interst

### 2019
- How I Failed My Way to Success with Azure Pipelines
  + https://toastit.dev/2019/02/06/how-i-failed-my-way-to-success-with-azure-pipelines/
  + https://toastit.dev/2019/02/17/how-i-failed-my-way-to-success-with-azure-pipelines-part-2-release/
