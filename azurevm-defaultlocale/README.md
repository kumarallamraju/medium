A quick ARM template that sets the default locale to German
This template was based off https://github.com/Azure/azure-quickstart-templates/tree/master/101-vm-simple-windows


###Steps to Deploy this ARM template.  


**1. Create a Resource Group.**. 

az group create --name nukeRG -l westus2

**2. Deploy the ARM template**. 

az deployment group create -g nukeRG --template-file azuredeploy.json --parameters azuredeploy.parameters.json --parameters adminUsername=azureuser --parameters adminPassword=YOURADMINPASSWORD --parameters dnsLabelPrefix=sp12282020

e.g. 
az deployment group create -g nukeRG --name rollout0 --template-uri https://raw.githubusercontent.com/kumarallamraju/medium/master/azurevm-defaultlocale/azuredeploy.json --parameters https://raw.githubusercontent.com/kumarallamraju/medium/master/azurevm-defaultlocale/azuredeploy.parameters.json --parameters adminUsername=kumara --parameters adminPassword=Azure12345678# --parameters dnsLabelPrefix=sp12282020
