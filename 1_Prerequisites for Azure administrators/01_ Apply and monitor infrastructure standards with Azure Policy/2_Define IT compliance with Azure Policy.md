
# Define IT compliance with Azure Policy

Planning out a consistent cloud infrastructure starts with
### setting up policy. Your policies will enforce your rules for created resources, so 
 ## your infrastructure stays compliant with your corporate standards, 
  ## cost requirements,
  ## and any service-level agreements (SLAs) you have with your customers.
  
  ![alt text](https://docs.microsoft.com/en-us/learn/modules/intro-to-governance/media/2-azurepolicy.png)
  
## Azure Policy is an Azure service you use to create, assign and, manage policies.

* These policies enforce different rules and effects over your resources so that those resources stay compliant with your corporate standards and service level agreements. 
* Azure Policy meets this need by evaluating your resources for noncompliance with assigned policies.
## For example, you might have a policy that allows virtual machines of only a certain size in your environment. After this policy is implemented, new and existing resources are evaluated for compliance. With the right type of policy, existing resources can be brought into compliance.

Imagine we allow anyone in our organization to create virtual machines (VMs). We want to control costs, so the administrator of our Azure tenant defines a policy that prohibits the creation of any VM with more than 4 CPUs.
* Once the policy is implemented, Azure Policy will stop anyone from creating a new VM outside the list of allowed stock keeping units (SKUs). 
* Also, if you try to update an existing VM, it will be checked against policy. 
* Finally, Azure Policy will audit all the existing VMs in our organization to ensure our policy is enforced.
* It can audit non-compliant resources, alter the resource properties, or stop the resource from being created. 
* You can even integrate Azure Policy with Azure DevOps, by applying any continuous integration and delivery pipeline policies that affect the pre-deployment and post-deployment of your applications.

## How are Azure Policy and RBAC different?

`At first glance, it might seem like Azure Policy is a way to restrict access to specific resource types similar to role-based access control (RBAC).

However, they solve different problems.

RBAC focuses on user actions at different scopes.

You might be added to the contributor role for a resource group, allowing you to make changes to anything in that resource group.

Azure Policy focuses on resource properties during deployment and for already-existing resources. 

Azure Policy controls properties such as the types or locations of resources. 

Unlike RBAC, Azure Policy is a default-allow-and-explicit-deny system.
`
