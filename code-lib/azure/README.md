# Azure CLI codes

## Copy storage account data to another 
This code copy all data in storage account to another storage accout. SAS means Shared Access Signature. Can be obtain in Azure Storage explorer. (Be careful on permissions on SAS) 
```bash
azcopy cp "https://[sourceStorageAccountName].blob.core.windows.net/[SAS]" "https://[targetStorageAccountName].blob.core.windows.net/[SAS]" --recursive
```
Ref : https://devconnected.com/how-to-clean-up-git-branches/  
Install Azcopy : https://www.thomasmaurer.ch/2019/05/how-to-install-azcopy-for-azure-storage/

## Create Azure Credentials for Github
This code create worker credentials for github actions
```bash
az ad sp create-for-rbac --name "[workerName]" --role contributor \
                            --scopes /subscriptions/[SubcriptionId]/resourceGroups/[ResourceGroupName] \
                            --sdk-auth
```
