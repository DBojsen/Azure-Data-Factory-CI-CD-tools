---
layout: default
title: ADF CI/CD Tools
nav_order: 1
permalink: /
---
# <span style="color:darkcyan">Welcome to Azure Data Factory CI/CD tools</span>

## <span style="color:darkcyan">Introduction</span>
Hi, and welcome to my Azure Data Factory CI/CD tools Extension documentation page.\
\
This is a tool that I'm maintaining in my personal time, although I would like to thank my employeer <a href="https://www.kapacity.dk/" target="_blank">twoday Kapacity</a> for allowing me to build this based on knowledge and experience I have gained while working as a Principal Architect there for the past many years.

## <span style="color:darkcyan">Why create a deployment tool</span>
Until recently, the <a href="https://learn.microsoft.com/en-us/azure/data-factory/continuous-integration-delivery#cicd-lifecycle" target="_blank">best practice from Microsoft</a> to deploy Data Factory resources involved a manual step in the UI, which IMHO is a complete no-go in a CI/CD scenario.\
They have since created a <a href="https://learn.microsoft.com/en-us/azure/data-factory/continuous-integration-delivery-improvements#continuous-deployment-improvements" target="_blank">new way of doing this</a>, that requires a build step that builds the json files into ARM templates.\
I still feel that this process should be simpler and more user friendly.\
\
In twoday Kapacity we have been deploying Data Factory resources for several years through a massive PowerShell script that essentially used the Data Factory REST APIs to deploy everything.\
\
This extension builds upon the experience we have gathered doing this, and simplifies the process a lot also.

## <span style="color:darkcyan">Prerequisites</span>

### <span style="color:darkcyan">Validation task</span>
There are no prerequisites to start using the validation task.\
Just install the extension and setup branch policies with build validation for any relevant branches.
Head over to the [Validation task documentation](Validation/) for more info\
(* please note that this task has not yet been released)
### <span style="color:darkcyan">Deployment task - Azure</span>
Before you can start using this task to deploy your Data Factory resources, a few things needs to be in place first:
- Your 3 (or more environments) with a Data Factory resource in each
- Any global parameters needed should already have been configured
- Any KeyVault linked services should have been configured and deployed (the extension will take care of all other Linked Services)
- If you need to use one (or more) Self Hosted Integration Runtimes, they should already have been configured.

In my opinion, these prerequisites belongs as part of your infrastructure setup (preferably using Infrastructure as Code), and not as part of deploying Data Factory resources.
### <span style="color:darkcyan">Deployment task - Azure DevOps</span>
You need to have a service connection configured for each environment, that have at least contributor rights on the Data Factory resource.\
In most cases, you should already have one, that have contributor rights to the entire resource group, that you use to deploy other resources such as IaC, Database or the likes.
## <span style="color:darkcyan">Install and configure extension</span>
It's as simple as going to <a href="https://marketplace.visualstudio.com/items?itemName=DavidBojsen.dbojsen-datafactory-cicd-tools" target="_blank">Azure Data Factory CI/CD tools on Visual Studio Marketplace</a> and click [Get it free].\
You will need to have the right permission setup, in order to do this.
Please see <a href="https://learn.microsoft.com/en-us/azure/devops/marketplace/request-extensions?view=azure-devops" target="_blank">the Microsoft documentation</a> for details.

## <span style="color:darkcyan">Troubleshooting</span>
If you are having issues using this extension, please first look at the [troubleshooting](troubleshooting.html) page.\
If you do not find the solution there, please feel free to create an issue (see next topic)
### <span style="color:darkcyan">Issue tracker on GitHub</span>
You will find the <a href="https://github.com/DBojsen/Azure-Data-Factory-CI-CD-tools/issues" target="_blank">issue tracker here</a>.\
Please do a search before creating an issue, to see if it has already been reported.
### <span style="color:darkcyan">Feature requests</span>
Feature requests are very welcome.\
Please use the issue tracker mentioned in the previous section to report them.\
\
\
I do hope that you enjoy my work.\
Best regards

David