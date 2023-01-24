# Cost Showback for VM group by size (s,m,l,xl) for   Operations 8.X, and Cloud
Use this [Aria Operations](https://www.vmware.com/products/vrealize-operations.html) dashboard to show the cost of VMs by size of VM (small, medium, large, x-large).

I modified the dashboard made by [Brock Peterson](https://developer.vmware.com/samples?id=7600#)

## Dashboard
![Dashboard](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/dashboard.png)

## Installation
1. Import the super metric at `Configure` / `Super Metrics` / `Import Super Metric` 
![Import Super Metric](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/supermetrics.png)
2. Click `Browse...` then select the file named [Supermetrics.json](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/supermetric.json)
3. Import Custom Groups at `Environment` / `Custom Groups` / `... ` / `Import`
![Import Custome Groups](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/customgroups.png)
4. Click `Browse...` then select the file named [CustomGroups.json](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/CustomGroups.json)
5. You can change groups membership and requiments. For the basic metrics it is set up as follow: 
`Small VM ` - CPU less then 1 RAM < 4GB
`Medium` - CPU = 2, RAM 8 GB
`Large` - CPU = 4, RAM 16 GB
`X-Large` - CPU >= 5 , RAM > 16 GB
6. Edit the Policy at `Configure` / `Policies`. The policy should be `vSphere Solution's Default Policy (DATE)` unless a new policy was explicitly created.
![Policy](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/policy.png)
7. Enable Super Metrics `AvarageWeeklyVMcost` , `AvarageDailyCost`, `AvarageMonthyCost` for `Container` / `Departments`
![Enable Policy](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/editPolicy.png)
8. Import the dashboard at `Environment` / `Dashboards` / `Manage` / `...` / `Import`
![Import Dashboard](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/dashboard1.png)
9. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/Dashboard.zip)
10 The dashboard should now be available in in the dashboard list
![Find your dashboard](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/dashboard2.png)

## IMPORTANT: The super metrics won't show cost until the next cost calculation run.  To manually run cost calculations to validate the super metrics, `Run` at `Administration` / `Cost Calculation`

![Run Cost Calculation](https://github.com/AngrySysOps/vrops_showback_cost_VM/blob/main/images/costcalculation.png)


NOTE: Additional objects can be added to the super metrics and to each widget and view in the dashboard.


IF you come a cross any issues, please open [ticket](https://github.com/AngrySysOps/vrops_showback_cost_VM/issues) 

Thank you! 

Please subscribe to my [Youtube channle](https://www.youtube.com/channel/UCRTcKGl0neismSRpDMK_M4A)

Please follow me on [Twitter](https://twitter.com/AngrySysOps)

Read my blog [angrysysops.com](https://angrysysops.com/)

