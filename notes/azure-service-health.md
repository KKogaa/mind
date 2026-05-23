Azure Service Health is a suite of experiences that provides personalized guidance and support when issues with Azure services affect you.
## What is Azure Service Health?
Azure Service Health gives you a personalized view of the health of Azure services and regions you're using. It provides proactive notifications, guidance, and support when service issues occur, helping you understand how Azure service problems might impact your specific resources.
## Three Main Components
### Azure Status
This provides a global view of the health of all Azure services across all Azure regions. It shows service outages, planned maintenance, and other issues that might affect Azure services broadly.
Azure Service Health reports the status of an Azure resource as follows:
1. Available: no events have been detected that affects
2. Unavailable: an event has been detected on an ongoing platform or non-platform that affects the health of the resouce
3. Unknown: no information about the resource has been reported for more than 10 minutes.
4. Degraded: a loss in performance has been detected for the resource.
### Service Health
This gives you a personalized view that tracks the Azure services and regions you're actually using. It filters the global Azure status information to show only what's relevant to your subscriptions and resources.
Azure Service Health notifications are stored in the Azure Activity Log. This way, Azure Service Health integrates with Azure Monitor which sends alerts.
The various classes of service health notifications are as follows:
- Action required: something unusual has happened on your account
- Assisted recovery: an event has occurred and Azure engineers confirm you are experiencing
- Incident: an event that impacts service is currently affecting one or more of the resources under your subscription
- Maintenance: a planned maintenance activity that might impact one or more resources under your subscription
- Information: states possible optimizations that might help improve your resource use
- Security: urgent security related information regarding your solutions that run on Azure
### Resource Health
This provides information about the health of your individual resources, such as virtual machines or databases. It helps you determine if a resource issue is due to a problem on your side or an Azure platform issue.
## Key Features
### Proactive notifications
You can set up alerts to be notified via email, SMS, or webhook when service issues affect resources you're using.
### Historical Information
Service Health maintains a history of service issues, so you can review past incidents.
### Maintenance communications
You receive advance notice of planned maintenance that might affect your resources.
### Root Cause Analysis
After incidents are resolved, Microsoft often provides detailed root cause analysis reports explaining what happened and what steps are being taken to prevent similar issues.
