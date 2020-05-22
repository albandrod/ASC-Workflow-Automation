# Notify-ASCRecommendationsAzureScope
author: Nathan Swift

This Logic App for Workflow Automations will notify ASC generated recommendations to Owners and Contributors assigned RBAC on the Azure Resource and will send TO: scoped resource and CC: scoped MGs or Subs or RGs.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FASC-Workflow-Automation%2Fmaster%2FNotify-ASCRecommendationsAzureScope%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FASC-Workflow-Automation%2Fmaster%2FNotify-ASCRecommendationsAzureScope%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

**Additional Post Install Notes:**

The Logic App uses a Managed System Identity (MSI) to authenticate and authorize against management.azure.com to obtain PrincipalIDs assigned to the Azure Resource and determine scope. The MSI is also used to authenticate and authorize against graph.windows.net to obtains RBAC Objects by PrincipalIDs. Be sure to turn on the System Assigned Identity in the Logic App. 

Assign RBAC 'Reader' role to the Logic App at the Subscription level.
Assign AAD Directory Role 'Directory readers' role to the Logic App.