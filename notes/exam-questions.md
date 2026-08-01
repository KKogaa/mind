---
title: Exam Questions
tags: [azure, azure-developer-associate, certification, practice]
up: "[[azure]]"
---

# Exam Questions

- Which command can you use to deploy a new azure container app?
az containerapp create --resource-group myRg --name myContainerApp

- Which of the following approaches to hosting containers in Azure is most appropriate when you want a serverless experience for Kubernetes-style apps, which can span many microservices?
Azure Container Apps

- Where do Azure virtual machines fall on Azure shared responsibility model?
Infrastructure as a Service (IaaS)

-  You have a web app that is running in the S1 App Service tier. Your team has added some additional functionality and performance enhancements to the site, but your QA team needs to validate everything is functional prior to releasing the updates. What is the most efficient and cost-effective way to ensure they can validate your code without impacting your live site?
Create a new deployment slot in your web app, deploy your new code to that slot, and switch to your new slot as the production instance once QA has validated the changes.

- Which of the following options CANNOT be included as part of the function.json file for an Azure function?
Function time-out setting

- Which of the following options would be a valid Docker CLI command used to upload a Docker image from your local Docker instance to your container registry?
docker push or docker image push

- Which of the following is not required when creating a new Azure Container Registry Instance?
Size

- You need to run an Azure function that operates against message data in Azure Storage once a day. Which of the following triggers is most appropriate?
Timer

- In Azure App Service, what is the minimum App Service plan you can use to gain access to SSL certificate management and Production Azure SLAs?
S1

- Which of the following options are methods for deploying resources in Azure and are expressed in declarative language?
Azure Resource Manager (ARM) templates 

- Cosmos DB partitions are defined in which of the following two forms?
Logical and physical.

- Which of the following is a supported API in Cosmos DB?
Cassandra.

- In the context of Azure Blob Storage, what is the primary function of Azure Lifecycle Management Policies?
To transition data from hotter to cooler storage tiers based on the age of data, optimizing performance and cost.

- Which type of storage blob is best for random access files, a form of storage is required when setting up storage in a virtual machine?
Page.

- Which of the following is the least complex way to automatically transition your blobs between storage tiers based on metrics such as the last modified date?
Use lifecycle management.

- Which of the following represents the supported APIs in Cosmos DB?
Cassandra, NoSQL and Gremlin.

- Which storage tier would be best for storing reports that are updated once per quarter but accessed frequently by your leadership staff?
Hot. While the report is not updated frequently, it is still accessed regularly and should be readily available for those users.

- Which Cosmos DB consistency model offers the weakest consistency and no order guarantees for updates to distributed data?
Eventual Consistency.

- When you enable static website hosting in Azure Storage, a blob storage conainer is required to store all the files related to your site. What is the name of this container?
$web. You will need a file that acts as a homepage, which is often named index.html, but this is not the name of the container, it should be $web.

## Related

- [[app-service]], [[azure-functions]], [[azure-container-instance]], [[compute-solutions]] — compute answers.
- [[azure-storage]], [[azure-cosmos-db]] — data answers.
- [[azure-study-todo]] — gaps these questions exposed.
