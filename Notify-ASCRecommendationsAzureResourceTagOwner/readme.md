# Notify-ASCRecommendationsAzureResourceTagOwner
author: Nathan Swift

This Logic App for Workflow Automations will notify the Azure Resource Owner using the Azure Resource - Owner:someone@domain.com Tag for a ASC generated recommendations.

You will to be using a [policy enforcing a Tag Owner](https://github.com/swiftsolves-msft/Policy/blob/master/EnforceTagging.json) to exist on deployed Azure Resources to take advantage of this. This should increase transparency to people deploying onto Azure that their resource configurations are insecure. This will hopefully reduce the amount of effort that the Security Team tracks down individuals and explains the security score on a praticular Azure resource.

<a href="https://azuredeploy.net/?repository=https://github.com/swiftsolves-msft/ASC-Workflow-Automation/blob/master/Notify-ASCRecommendationsAzureResourceTagOwner" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FASC-Workflow-Automation%2Fmaster%2FNotify-ASCRecommendationsAzureResourceTagOwner%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>