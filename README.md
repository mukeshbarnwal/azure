# azure
My learnings about Azure

Azure is a cloud-based platform where we can perform various operations including machine learning operations, setting up pipelines, create and host web servers. Infact anything that we can do on our local system. Azure provides range of services in this regard enabling ease of deployment, tracking, monitoring and servicing. 

When I entered into Azure platform for the first time, I found it too overwhelming as to what each of these services and features are. Gradually with time and increased understading, I got to know various terms, features and services. And things started to make sense. 

I will discuss what I have learnt through my journey with Azure ML which is a specific service for Machine learning operations such as if we want to fetch and store data, fit a machine learning model in the data, store different models such as gpt-4o, De-berta, Llama, store the learnt models so that we can use it for our test data. 

Firstly, we will discuss about workspace in Azure ML. A workspace is a storage house for all the data, models, pkl files. If we want to use any of these data, we have to enter into the workspace and use the required data for whatever purpose we want to. A workspace has workspace name, subcription id and resource group attached to it. This makes the workspace identifiable according to the user who uses it, billing and subscriptions taken by the user. It is a centralized repository for the user or an organization with multiple users. 

A resource group is a container that holds multiple workspaces. Imagine a workspace that deals only with advanced nlp projects. Another workspace is one which only deals with forecasting. Another one is related only with operations. These workspaces will have different names for example NLP_Workspace, Forecasting_Workspace, Operations_Workspace respectively. Each of these workspaces will have datasets, models, tokenizers, pkl files corresponding to the projects within that workspace. For example, for Forecasting_workspace only models, datasets, pkl files of forecasting will be there. This makes the workspace complete entity of their own and users within that team can work independtly from other team and collaborate within their own team. 

A subscription id is corresponding identity which helps Azure to track the user account, their billing and credentials. 

A sample code for using workspace and resource group looks like:

from azureml.core import Workspace 

subscription_id=""
resource_group=""
workspace_name=""

workspace=Workspace(subscription_id,resource_group,workspace_name)

This allows you to access the particular Workspace(denoted by workspace name) in Azure. 







