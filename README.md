# Create A Resource Group And A Storage Account

## A Resource Group
A resource group is a container that holds related resources for an Azure solution. The resource group can include all the resources for the solution, or only those resources that you want to manage as a group. You decide how you want to allocate resources to resource groups based on what makes the most sense for your organization. Generally, add resources that share the same lifecycle to the same resource group so you can easily deploy, update, and delete them as a group.
The resource group stores metadata about the resources. Therefore, when you specify a location for the resource group, you are specifying where that metadata is stored. For compliance reasons, you may need to ensure that your data is stored in a particular region.
## Create Resource Groups
1. Sign in to the Azure portal.
2. Select Resource groups.
3. Select Create.
4. Enter the following values:
- Subscription: Select your Azure subscription.
- Resource group: Enter a new resource group name.
- Region: Select an Azure location, such as Central US.
5. Select Review + Create
6. Select Create. It takes a few seconds to create a resource group.
7. Select Refresh from the top menu to refresh the resource group list, and then select the newly created resource group to open it. Or select Notification(the bell icon) from the top, and then select Go to resource group to open the newly created resource group

## A Storage Account
An Azure storage account contains all of your Azure Storage data objects: blobs, files, queues, and tables. The storage account provides a unique namespace for your Azure Storage data that is accessible from anywhere in the world over HTTP or HTTPS.
## Create A Storage Account
A storage account is an Azure Resource Manager resource. Resource Manager is the deployment and management service for Azure.
Every Resource Manager resource, including an Azure storage account, must belong to an Azure resource group. A resource group is a logical container for grouping your Azure services. When you create a storage account, you have the option to either create a new resource group, or use an existing resource group. This how-to shows how to create a new resource group
To create an Azure storage account with the Azure portal, follow these steps:
1. From the left portal menu, select Storage accounts to display a list of your storage accounts. If the portal menu isn't visible, select the menu button to toggle it on.
2. On the Storage accounts page, select Create.
Options for your new storage account are organized into tabs in the Create a storage account page. You can either leave the options as default or select the options that bests describe what you want to do. The tabs are as follows; basic, advance, networking, data protection, encryption, tags, and review + create.

## Lets take this exercise; 
The IT department needs to prototype different storage scenarios and to train new personnel. The content isn’t important enough to back up and doesn’t need to be restored if the data is overwritten or removed. A simple configuration that can be easily changed is desired.
## Exercise Instructions
1. Create a resource group and a storage account.
- Create and deploy a resource group to hold all your project resources. Learn more about resource groups.
- In the Azure portal, search for and select Resource groups.
- Select + Create.
- Give your resource group a name. For example, storagerg.
- Select a region. Use this region throughout the project.
- Select Review and create to validate the resource group.
- Select Create to deploy the resource group.
2. Create and deploy a storage account to support testing and training. Learn more about the types of storage accounts.
- In the Azure portal, search for and select Storage accounts.
- Select + Create.
- On the Basics tab, select your Resource group.
- Provide a Storage account name. The storage account name must be unique in Azure.
- Set the Performance to Standard.
- Select Review, and then Create.
- Wait for the storage account to deploy and then Go to resource.
## Configure Simple Settings In The Storage Account.
1. The data in this storage account doesn’t require high availability or durability. A lowest cost storage solution is desired. 
- In your storage account, in the Data management section, select the Redundancy blade.
- Select Locally-redundant storage (LRS) in the Redundancy drop-down.
- Be sure to Save your changes.
- Refresh the page and notice the content only exists in the primary location.
2. The storage account should only accept requests from secure connections.
- In the Settings section, select the Configuration blade.
- Ensure Secure transfer required is Enabled.
3. Developers would like the storage account to use at least TLS version 1.2. 
- In the Settings section, select the Configuration blade.
- Ensure the Minimal TLS version is set to Version 1.2.
4, Until the storage is needed again, disable requests to the storage account. 
- In the Settings section, select the Configuration blade.
- Ensure Allow storage account key access is Disabled.
- Be sure to Save your changes.
5. Ensure the storage account allows public access from all networks.
- In the Security + networking section, select the Networking blade.
- Ensure Public network access is set to Enabled from all networks.
- Be sure to Save your changes
