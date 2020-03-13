# Notify-ASCAlertsAzureResource
author: Nathan Swift

This Logic App for Workflow Automations will notify ASC generated threat alerts to RBAC assigned Owners and Contributors both user and mail enabled security groups on the Azure Resource.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FASC-Workflow-Automation%2Fmaster%2FRemediation%2Fscripts%2FNotify%2FASC%2FAlerts%2Fto%2Fusers%2Fresponsible%2Ffor%2FAzure%2Fresource%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FASC-Workflow-Automation%2Fmaster%2FRemediation%2Fscripts%2FNotify%2FASC%2FAlerts%2Fto%2Fusers%2Fresponsible%2Ffor%2FAzure%2Fresource%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

**Additional Post Install Notes:**

The Logic App creates and uses a Managed System Identity (MSI) to authenticate and authorize against management.azure.com to obtain PrincipalIDs assigned to the Azure Resource. The MSI is also used to authenticate and authorize against graph.windows.net to obtains RBAC Objects by PrincipalIDs. 

Assign RBAC 'Reader' role to the Logic App at the Subscription level.
Assign AAD Directory Role 'Directory readers' role to the Logic App.
