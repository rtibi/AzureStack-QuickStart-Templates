# Deploy a VM Scale Set of Windows VMs

This template allows you to deploy a VM Scale Set of Windows VMs. It uses the latest patched version of several Windows versions. To connect from the load balancer to a VM in the scale set, you would go to the AzureStack Portal, find the load balancer of your scale set, examine the NAT rules, then connect using the NAT rule you want. For example, if there is a NAT rule on port 50000, you could RDP on port 50000 of the public IP to connect to that VM. Similarly if something is listening on port 80 we can connect to it using port 80.

PARAMETER RESTRICTIONS
======================

vmssName must be 3-10 characters in length. It should also be globally unique across all of AzureStack. If it isn't globally unique, it is possible that this template will still deploy properly, but we don't recommend relying on this pseudo-probabilistic behavior.
InstanceCount must be 20 or less. VM Scale Set supports upto 100 VMs and one should add more storage accounts to support this number.



<a href="https://portal.local.azurestack.external/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Frtibi%2FAzureStack-QuickStart-Templates%2Fmaster%2F101-vmss-windows-vm%2Fazuredeploy.json" target="_blank">
    <img src="https://github.com/rtibi/azs/blob/master/azsdeploybutton.png" width=161 height=34/> 
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Frtibi%2FAzureStack-QuickStart-Templates%2Fmaster%2F101-vmss-windows-vm%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/> 
</a>

