# Import-SecureScore
author: Nathan Swift

This Logic App will on a timer basis daily or weekly obtain your subscriptions Azure Security Ceneter Securee Scores and Reccomendations, then send the scores and recommendations to Azure Security Center Log Analytics Workspace - SecureScore_CL and SecureScoreControls_CL . You can now build workbooks and trend historical analysis of your Secure Scores and Recommendations overtime. You can also leverage SecureScore Email Reports with another Playbook using this data.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSwiftSolves-MSFT%2FASC-Workflow-Automation%2Fmaster%2FImport-SecureScore%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FSwiftSolves-MSFT%2FASC-Workflow-Automation%2Fmaster%2FImport-SecureScore%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>

**Additional Post Install Notes:**

Ensure to authorize the AzureLogAnalyticsDataCollector API by giving it the Azure Security Center LogAnalytics Workspace ID and Key
<img src="https://raw.githubusercontent.com/Azure-Sentinel/DataConnectors/master/Prisma/images/authorize.png"/>
</a>

To learn more about SecureScore: https://docs.microsoft.com/en-us/azure/security-center/secure-score-security-controls