---
title: Azure Functions
tags: [azure, azure-developer-associate, cloud, serverless, compute]
up: "[[azure]]"
---

# Azure Functions

## Coding and deploying azure functions
Serverless isn't a one sized fit all for everything you need to do in a cloud. It is best for lightweight and flexible app or with inconsistent spikes. 
### Understanding serverless benefits
- No infrastructure management
	- Avoid administrative tasks and focus on core business logic. Simply deploy and run with high availability.
- Dynamic scalability
	- Scale apps dynamically to match the demands of independent workloads.
- Faster time to market 
	- Reduce operational dependencies, increasing agility and functionality in less time.
- Efficient use of resources
	- Reduce total cost of ownership freeing up staff to focus on tasks that drive innovation.

### Parts of a function
- Trigger
	- Based on schedules, rules or events, every function must have exactly one trigger.	
- Input
	- Inputs consist of data, such as a message in a queue, and are optional.
- Output
	- Outputs define the destination or handler for returned data and are optional.
## Consider Hosting options
Only the consumption and premium plan are truly serverless. The rest need more managing of the resources. 
The recommendation is to deploy apps on the consumption plan for development and testing, then you can switch to premium plan when the needs are met.
- Consumption plan
	- Designed for lightweight apps where you only pay for the resources that you use.
		- Pay only when functions are running.
		- Scale out automatically, even during periods of high load.
		- Times out after a configurable period of up to 10 minutes. 
		- idle function apps must "cold start" on next request.
		- Less complex architecture.
- Premium plan
	- Contains additional benefits that are not included in the consumption plan.
		- More predictable pricing.
		- Premium instance sizes of one, two, or four cores and faster scaling.
		- Unlimited execution duration, with 60 minutes guaranteed.
		- Continuously running instances to avoid any cold start.
		- VNet connectivity.
- Dedicated plan
- App service environment
- Kubernetes

## Related

- [[app-service]] — Functions run on App Service plans; the Dedicated plan is literally an App Service plan.
- [[compute-solutions]] — where serverless sits among the hosting options.
- [[azure-storage]] — the most common trigger and binding source.
- [[azure-cosmos-db]] — another common binding target.
- [[exam-questions]] — trigger types and `function.json` come up here.
- [[things-todo]] — "create azure function in python using sqlalchemy".
