
Here we can use this to deploy an entire infrastructure from a certain subscription.
Azure Blueprint artifacts are the building components that make up an Azure Blueprint definition. The main types of artifacts you can include:
- Policy assignments e.g. Apply default tag and value to all resources
- Role assignments e.g. Add a user or a group the contributor role assignment 
- ARM templates e.g. Create a vnet or a vnet-gateway
- Resource groups e.g. Create a resource group
	Here we can add artifacts within the resource group
	- Policy assignment
	- Role assignment
	- ARM template