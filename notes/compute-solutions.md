---
title: Compute Solutions
tags: [azure, azure-developer-associate, cloud, compute]
up: "[[azure]]"
---

# Compute Solutions

## Leaving behind virtual machines
### Shared Responsibility model
- On premises
	It is your own services you are expected to handle everything by yourself.
- IaaS  (Infrastructure as a service)
	Physical security and hardware is handled by azure, but you are partly responsible for maintaining the network and operating system, everything else it is up to you. This is a cloud server.
- PaaS  (Platform as a service )
	Scaling, security and infrastructure management is done by azure, like app services or functions.
- SaaS (Software as a service)
	Software or api services given by azure.
### Virtual machine deployment
You can deploy code two ways
- Imperative code
		Virtual infrastructure is deployed manually using azure cli or powershell with remote connection.
- Declarative code
	Virtual infrastructure is deployed using ARM or Bicep templates or terraform.
### Configuration Smorgasbord
For deploying on virtual machines there are many configurations.
- Many sizes for varying purposes
	- Small test-optimized workloads.
	- Something in between.
	- GPU bearing for machine learning.
- Customizabl.e from OS to images
	- Windows or Linux.
	- Purpose-built images.
	- Bring your own images.	
### Deploy with code
- Deploy using commands
	- For example using the command az vm create.
- Deploy using templates
	- Deploy using any type of template that connects to azure.

## Storing and sharing your containers

See [[azure-container-instance]] for running them, and [[azure-study-todo]] for the Container Registry recap still pending.

## Related

- [[app-service]] — the PaaS option.
- [[azure-functions]] — the serverless option.
- [[azure-container-instance]] — the container option.
- [[azure-blueprint]] — declarative deployment of whole environments.
- [[exam-questions]] — the IaaS/PaaS/SaaS placement question lives here.
