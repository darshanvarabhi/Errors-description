1. ### Disabling Encryption is not supported for the account.

      `azurerm_storage_account.<container_resource_name>: Error creating Azure Storage Account "<STORAGE_ACCOUNT_NAME>": storage.AccountsClient#Create: Failure responding to request: StatusCode=400 -- Original Error: autorest/azure: Service returned an error. Status=400 Code="FeatureNotSupportedForAccount" Message="Disabling Encryption is not supported for the account."`

    ### Resolution/Understanding:
    The <STORAGE_ACCOUNT_NAME> already existed in Azure, was created manually. Deleting the existing one or changing the name of the newly to-be-created storage account, will solve this issue.

    Other possible issues - https://github.com/terraform-providers/terraform-provider-azurerm/issues/1003
