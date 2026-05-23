#azure-developer-associate #cloud #azure 
Azure app service allows you to quickly build web apps and apis without relying on the underlying host.

## App service features
- Support for multiple languages.
- Web, REST API and mobile.
- CI/CD out of the box (Manual deployment like ftp or dropbox or automated like github actions or azure devops). 
- Deployment slots.
- Integrated, low code IAM.
- Multiple service plans for development and production.
- Built in autoscale.
- App service on linux expanding continually.

## Approach service plan as the "scale unit" 
### Service plan defines/controls for all apps 
- Region.
- Number and size of vms.
- Pricing tier.
- Run state and scale.
### When to isolate and app on a new plan
- Desire to scale app independently.
- App needs resources in a different region.
- App is resource intense.

## Service plans
- F1 Free and D1 Shared Tier
	- Share resources with other tenants.
	- Limit resources like cpu, disk space, apis and ram.
	- No SLAs.
	- Considered useful for test workloads.
	- Cannot run app service on linux on shared tiers.
- Basic B1, B2, B3 (dev/test), Standard (S1, S2, S3), Premium v2 (P1v2, P2v2, P3v2),  Premium v3 (P1v3, P2v3, P3v3) 
	- Dedicated tiers dedicated resources.
	- Production SLAs.
	- Additional security options and custom domain SSL.
	- Additional options such as built in load balancing across instances. (For premium tiers.)
	- 
- Isolated and Isolated v2
	- Isolation provides peace of mind.
	- All of the benefits found in the dedicated tiers.
	- Best of the best performance, security, scalability and availability.

## Enable diagnostic logging
- Go to app service logs option (this will enable to save application logs in the log stream). 

## Change tiers for the app service
- To scale down go to scale up option.
- To scale down go to scale down option.
- You can definine scaling rules when cpu or other thresholds based on metrics are reached.
## Deploy with deployment slots
Deployment slots or staging slots are live apps with their own hostnames. Deployment slots allow to have for example a production slot and a staging slot. When errors occur on production, a developer can test the changes on the staging slot and users traffic can be also temporarily be diverted there. When all is working well you can swap the production slot with the staging slot.  
- Identify the web app that you need to modify.
- Use a staging slot to test changes to the web app.
- Note that you need use a plan that supports deployment slots.
By default you will already have a production slot running after deploying to app service.

## Web app configuration
- General settings.
- Path mapping.
- Security certificates.
- App features.

## IAM Options
- Roll your own (user managing options inside app service configuration).
- Built in authentication.
- Workflow with SDK.
- Workflow without SDK.

## Deployment Options
- Manual.
- Automated.
- Deployment slots.