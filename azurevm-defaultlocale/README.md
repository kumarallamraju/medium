A quick ARM template that sets the default locale to German
This template was based off https://github.com/Azure/azure-quickstart-templates/tree/master/101-vm-simple-windows


###Steps to Deploy this ARM template.  


**1. Create a Resource Group.**. 

az group create --name nukeRG -l westus2

**2. Deploy the ARM template**. 

az deployment group create -g nukeRG --template-file azuredeploy.json --parameters azuredeploy.parameters.json --parameters adminUsername=azureuser --parameters adminPassword=YOURADMINPASSWORD --parameters dnsLabelPrefix=sp12282020
