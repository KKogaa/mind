---
title: Authentication and Authorization
tags: [azure, azure-developer-associate, cloud, identity, security]
up: "[[azure]]"
---

# Authentication and Authorization

## OAuth2
How does OAuth2 work?
User opens web app -> redirect to azure AD (if successful it returns a token to the user) -> the token allows to validate the user.

- Resource owner: Requests service from app. Owns the data and assigns access to resources.
- Resource server: Resource or data resides here. Trusts authorization server to relay who has access to what and manages tokens.
- Authorization server: Also known as identity provier. Handles all aspects of user access, information, trusts. Azure AD B2C to enable users to use a preferred identity, such as Google or Apple.
## RBAC (Role based access control)
- On Azure there are predetermined roles, but you can also create custom ones.
- A role definition is made up of permissions, examples like read item, write item, execute query.
- Ones we have roles defined we make role assignments to user identities. 
- You can enable multi factor authentication, with conditional access policy.
### Sample built in roles that can be applied to a security principal
This example is for azure blob storage.
	- Storage Blob Data Owner -> Full access to blob storage containers and data including permissions for others.
	- Storage Blob Data Contributor -> Read, write, and delete access to Blob storage containers and blobs.
	- Storage Blob Reader -> Read and list Blob storage containers and blobs.
To create a role definition with command, first create a json file containing the name of the role, and the list of the permissions.	
az role definition create --role-definition <file.json>

## Implementing Secure Storage Solutions
### Surveying Shared Access Signatures (SAS)
Are keys that grant permissions to storage resources, you can share this keys in a string called the SAS Url. A SAS should follow the principle of least permission given to the user to get the job done. There are three types of levels where you can setup a SAS token.
- Account Level (Use very rarely): Delegates access to one or more resources using account key, with owner-like priviledges.
- Service Level (More common): Delegates access a specific resource using account key: blob, queue, table, files
- User Level (Preferred): Delegates access using Azure AD credentials to containers and blobs in Blob storage only.

## Related

- [[microsoft-entra-id]] — the authorization server in the OAuth2 flow above.
- [[azure-storage]] — the SAS section applies directly to blob storage.
- [[azure-resource-groups]] — the scope role assignments are made against.
- [[app-service]] — built-in authentication implements this flow for you.
- [[azure-blueprint]] — role assignments as a deployable artifact.
