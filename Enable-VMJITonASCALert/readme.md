# Enable-VMJITonASCAlert
author: Nathan Swift

This Logic App will update a Azure VM to use JIT access for the OS management port when ASC Alerts fire. Ensure Worflow automation fires on alerts contains ”SSH Brute Force” or “Suspicious incoming RDP network” or “Suspicious incoming SSH network"

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSwiftSolves-MSFT%2FASC-Workflow-Automation%2Fmaster%2FEnable-VMJITonASCAlert%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSwiftSolves-MSFT%2FASC-Workflow-Automation%2Fmaster%2FEnable-VMJITonASCAlert%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

**Additional Post Install Notes:**

The Logic App creates and uses a Managed System Identity (MSI) to enable a Just In Time access policy to prevent management access on SSH or RDP on a Azure VM that was attacked.

Assign RBAC 'Virtual Machine Contributor' and 'Security Admin' role to the Logic App at the root Management Group level or on Azure Subscriptions.

To learn more about ASC Just In Time Access: https://docs.microsoft.com/en-us/azure/security-center/security-center-just-in-time