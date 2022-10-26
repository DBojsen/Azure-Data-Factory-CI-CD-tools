---
layout: default
title: Deployment task
nav_order: 2
has_children: true
has_toc: false
---
# <span style="color:darkcyan">Deployment of Data Factory resources</span>

## <span style="color:darkcyan">Add deployment task</span>
First you need to add the task to your pipeline.\
Search for `deploy data factory` to quickly get to it:\
<img src="../assets/1_AddTask.png">\

## <span style="color:darkcyan">Basic setup of the deployment task</span>
Now you need to configure it:\
<img src="../assets/2_BasicSetup.png">\
| Setting             | Description                                                                              |
|:--------------------|:-----------------------------------------------------------------------------------------|
| ARM Connection      | A service connection with at least contributor role on the Data Factory instance         |
| Subscription Id     | The id of the subscription where your ADF is (preferably from a variable)                |
| Resource Group Name | Name of the Resource Group, where your ADF is. (preferably from a variable)              |
| ADF Name            | The name of the ADF resource                                                             |
| Data Factory Folder | If you publish your ADF files as an artifact called ADF, then the default should be fine |
| Remove artifacts    | Should the task cleanup no longer relevant resources?                                    |