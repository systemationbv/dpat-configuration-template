# DPAT Configuration Template

<br/>

### Prerequisites

A Data Product should already exist in order to attach the new components to it.

<br/>

### Component Basic Information

This section includes the basic information that any Component of Witboost must have:

<br/>

#### DPAT Witboost Metadata 
Parameters for the DPAT Configuration template
      
- **name**: Required name used for display purposes (Required)
- **domain**: Domain of the Data Product this DPAT configuration artifact belongs to (Required)
  In our sandbox environment, you will find the following domains:
     * Finance
     * Marketing
     * Organization        
- **dataproduct**: Data Product this DPAT configuration artifact belongs to (Required)
  A group referring your company name and related to the accounts that we are providing to you should be already created inside the sandbox environment, so you can select it:
     * guest_admin
     * ...
     * ...
- **dataProductRepo**: DPAT Configuration artifact will be created into this repository (ReadOnly)
- **dataProductRootDirectory**: Root directory of the Data Product repository where the DPAT Configuration artifact will be created  (ReadOnly) 
- **identifier**: A unique identifier for the entity inside the domain. It will not be editable after creation and is expected to be a string that is sequences of [a-zA-Z] separated by any of [-_] (ReadOnly)
- **owner**: Automatically selected from the Data Product metadata. Data Product owner. (ReadOnly)
- **dependsOn**: Add a depencies risk (if needed) and give a short description of it/them.
   * Dependencies Risks

<br/>

_Example:_

| Field name                     | Example value                                          |
|:-------------------------------|:-------------------------------------------------------|
| **Name**                       | DPAT Configuration                                     |
| **Domain**                     | domain:engineering                                     |
| **Data Product**               | system:engineering.payments-interbank-credit-transfer.0|
| **Data Product Repository**    | rabo-wit-dp-engineering-paymentsinterbankcredittransfer|
| **Data Product Rootdirectory** | owner:guest_developer                                  |
| **_Identifier_**               | finance.rabobank-poc-dataproduct.0.dpat-configuration  |
| **Component Owner**            | user:rafael.correia.nascimento_rabobank.nl             |
| **Deponds on**                 | owner:guest_developer                                  |

<br/>

### Production variables:
Parameters for the DPAT Configuration template (All fields are Required)
      
- **resourceGroupName**: Name of the Azure Resource Group where the DPAT Data Product will be deployed
- **adlsStorageAccount**: Name of the ADLS Storage Account to be used in the DPAT Data Product configuration
- **adlsContainerName**: Name of the ADLS Container to be used in the DPAT Data Product configuration
- **databricksSecretKey**: Secret Key of the Databricks workspace to be used in the DPAT Data Product configuration
- **azureClientId**: Client ID of the Azure Service Principal to be used in the DPAT Data Product configuration
- **azureTenantId**: Tenant ID of the Azure Service Principal to be used in the DPAT Data Product configuration
- **azureScope**: Scope to be used for Azure authentication in the DPAT Data Product configuration
- **metadataAPI**: URL of the Metadata API to be used in the DPAT Data Product configuration
- **dataProducerName**: Name of the Data Producer to be used in the DPAT Data Product configuration
- **relativeUrl**: Relative URL to be used in the DPAT Data Product configuration

<br/>

_Example:_

| Field name                     | Example value                                             |
|:-------------------------------|:----------------------------------------------------------|
| **Resource Group Name**        | rg-edl-dpat-sandbox-westeu-prod-0001                      |
| **ADLS Storage Account**       | edldptsbxeuprod0001                                       |
| **ADLS Container Name**        | dpat-sandbox                                              |
| **ADLS Type**                  | abfss                                                     |
| **ADLS Endpoint URL**          | dfs.core.windows.net                                      |
| **ADLS Path**                  | data                                                      |
| **ADLS Format**                | delta                                                     |
| **Databricks Secret Key**      | edl-dpat-sandbox-prod-databricks                          |
| **Azure Client ID**            | 52ffdeb9-cc12-40ba-bc96-20e4cc206278                      |
| **Azure Tenant ID**            | 6e93a626-8aca-4dc1-9191-ce291b4b75a1                      |
| **Azure Scope**                | http://wapp-edl-cap-metadata-api-westeurope-prod/.default |
| **Metadata API URL**           | 2680ea35-1fa1-40e4-8a86-1665ab814978.az-eu.api.rabo.cloud |
| **Data Producer Name**         | Interbank Credit Transfer                                 |
| **Relative URL**               | https://portal.azure.com/#@raboweb.onmicrosoft.com/resource/subscriptions/ac36d871-d439-49b0-b4d0-ece8f4096050/resourceGroups/rg-edl-dpat-sandbox-westeu-prod-0001/overview |

<br/>

### QA variables:
Parameters for the DPAT Configuration template (All fields are Required)
      
- **resourceGroupName**: Name of the Azure Resource Group where the DPAT Data Product will be deployed
- **adlsStorageAccount**: Name of the ADLS Storage Account to be used in the DPAT Data Product configuration
- **adlsContainerName**: Name of the ADLS Container to be used in the DPAT Data Product configuration
- **databricksSecretKey**: Secret Key of the Databricks workspace to be used in the DPAT Data Product configuration
- **azureClientId**: Client ID of the Azure Service Principal to be used in the DPAT Data Product configuration
- **azureTenantId**: Tenant ID of the Azure Service Principal to be used in the DPAT Data Product configuration
- **azureScope**: Scope to be used for Azure authentication in the DPAT Data Product configuration
- **metadataAPI**: URL of the Metadata API to be used in the DPAT Data Product configuration
- **relativeUrl**: Relative URL to be used in the DPAT Data Product configuration
- **dataProducerName**: Name of the Data Producer to be used in the DPAT Data Product configuration

<br/>

_Example:_

| Field name                     | Example value                                             |
|:-------------------------------|:----------------------------------------------------------|
| **Resource Group Name**        | rg-edl-dpat-sandbox-westeu-test-0001                      |
| **ADLS Storage Account**       | edldptsbxeutest0001                                       |
| **ADLS Container Name**        | dpat-sandbox                                              |
| **ADLS Type**                  | abfss                                                     |
| **ADLS Endpoint URL**          | dfs.core.windows.net                                      |
| **ADLS Path**                  | data                                                      |
| **ADLS Format**                | delta                                                     |
| **Databricks Secret Key**      | edl-dpat-sandbox-test-databricks                          |
| **Azure Client ID**            | b5e4ed31-5641-48ec-aea7-fc60e5328234                      |
| **Azure Tenant ID**            | 6e93a626-8aca-4dc1-9191-ce291b4b75a1                      |
| **Azure Scope**                | http://wapp-edl-cap-metadata-api-westeurope-test/.default |
| **Metadata API URL**           | dde6cda3-863d-4ce2-8c0e-c89d0e563353-nonprd.t-az-eu.api.rabo.cloud |
| **Data Producer Name**         | Interbank Credit Transfer                                 |
| **Relative URL**               | https://portal.azure.com/#@raboweb.onmicrosoft.com/resource/subscriptions/ac36d871-d439-49b0-b4d0-ece8f4096050/resourceGroups/rg-edl-dpat-sandbox-westeu-test-0001/overview |

<br/>

### Development variables:
Parameters for the DPAT Configuration template (All fields are Required)
      
- **resourceGroupName**:  Name of the Azure Resource Group where the DPAT Data Product will be deployed
- **adlsStorageAccount**: Name of the ADLS Storage Account to be used in the DPAT Data Product configuration
- **adlsContainerName**: Name of the ADLS Container to be used in the DPAT Data Product configuration
- **databricksSecretKey**: Secret Key of the Databricks workspace to be used in the DPAT Data Product configuration
- **azureClientId**: Client ID of the Azure Service Principal to be used in the DPAT Data Product configuration
- **azureTenantId**: Tenant ID of the Azure Service Principal to be used in the DPAT Data Product configuration
- **azureScope**: Scope to be used for Azure authentication in the DPAT Data Product configuration
- **metadataAPI**: URL of the Metadata API to be used in the DPAT Data Product configuration
- **relativeUrl**: Relative URL to be used in the DPAT Data Product configuration
- **dataProducerName**: Name of the Data Producer to be used in the DPAT Data Product configuration

<br/>

_Example:_

| Field name                     | Example value                                             |
|:-------------------------------|:----------------------------------------------------------|
| **Resource Group Name**        | rg-edl-dpat-sandbox-westeu-dev-0001                       |
| **ADLS Storage Account**       | edldptsbxeudev0001                                        |
| **ADLS Container Name**        | dpat-sandbox                                              |
| **ADLS Type**                  | abfss                                                     |
| **ADLS Endpoint URL**          | dfs.core.windows.net                                      |
| **ADLS Path**                  | data                                                      |
| **ADLS Format**                | delta                                                     |
| **Databricks Secret Key**      | edl-dpat-sandbox-dev-databricks                           |
| **Azure Client ID**            | 52ffdeb9-cc12-40ba-bc96-20e4cc206278                      |
| **Azure Tenant ID**            | 6e93a626-8aca-4dc1-9191-ce291b4b75a1                      |
| **Azure Scope**                | http://wapp-edl-cap-metadata-api-westeurope-test/.default |
| **Metadata API URL**           | dde6cda3-863d-4ce2-8c0e-c89d0e563353-nonprd.t-az-eu.api.rabo.cloud |
| **Data Producer Name**         | Interbank Credit Transfer                                 |
| **Relative URL**               | https://portal.azure.com/#@raboweb.onmicrosoft.com/resource/subscriptions/ac36d871-d439-49b0-b4d0-ece8f4096050/resourceGroups/rg-edl-dpat-sandbox-westeu-dev-0001/overview |

<br/>

#### Review and Create
After the final step the system will show you the summary of the template, and you can go back and edit or go ahead and create the Component. With the examples values given here it should look something like this:

After this the system will show you the summary of the template, and you can go back and edit or go ahead and create the Component.

After clicking on "Create" the registering of the Component will start. If no errors occurred it will go through the 3 phases (Fetching, Publishing and Registering) and will give you the links to the newly created Repository and the component in the Catalog.

<br/>

#### Users guide
Click [here](https://raw.githubusercontent.com/systemationbv/dpat-configuration-template/main/docs/dpat-configuration-template.pdf) for the graphical users guide


<br/>

**Be careful not to delete the `catalog-info.yml` as well as keep the project structure as given.**