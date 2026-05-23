
When you delete a resource group, Resource Manager uses specific criteria to determine the order in which the resources are deleted:
1. All nested (child) resources are deleted first
2. All resources that manage other resources, as indicated by the managedBy property set on the managed resource, are deleted next
3. The remaining resources are deleted last, but not in chronological order from newest to oldest
Resource Manager continues to retry the DELETE call every 15 mintues when delete operation returns an error with 4XX or 5XX status.
A resource group deletion is final and not reversible.