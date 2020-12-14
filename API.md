
# Azure API Management Resources


## Referneces

- https://docs.microsoft.com/en-us/azure/api-management/
- https://docs.microsoft.com/en-us/azure/api-management/api-management-features


- How to deploy an Azure API Management service instance to multiple Azure regions
  + https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-deploy-multi-region


- https://docs.microsoft.com/en-us/azure/api-management/api-management-using-with-internal-vnet
- https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-integrate-internal-vnet-appgateway

- https://docs.microsoft.com/en-us/azure/api-management/api-management-using-with-vnet
- https://docs.microsoft.com/en-us/azure/api-management/api-management-using-with-vnet#-common-network-configuration-issues

- How to secure back-end services using client certificate authentication in Azure API Management
  + https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-mutual-certificates
    * "API Management allows you to secure access to the back-end service of an
      API using client certificates. This guide shows how to manage certificates
      in the Azure API Management service instance in the Azure portal. It also
      explains how to configure an API to use a certificate to access a back-end
      service."
  + https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-mutual-certificates#-configure-an-api-to-use-a-client-certificate-for-gateway-authentication

- Configure TLS mutual authentication for Azure App Service
  + https://docs.microsoft.com/en-us/azure/app-service/app-service-web-configure-tls-mutual-auth
    * "You can restrict access to your Azure App Service app by enabling
      different types of authentication for it. One way to do it is to request a
      client certificate when the client request is over TLS/SSL and validate
      the certificate. This mechanism is called TLS mutual authentication or
      client certificate authentication."


- How to add a custom CA certificate in Azure API Management
  + https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-ca-certificates

- Manage protocols and ciphers in Azure API Management
  + https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-manage-protocols-ciphers

- Import an OpenAPI specification
  + https://docs.microsoft.com/en-us/azure/api-management/import-api-from-oas
    * "An API can be composed of APIs exposed by different services, including
      the OpenAPI Specification, a SOAP API, the API Apps feature of Azure App
      Service, Azure Function App, Azure Logic Apps, and Azure Service Fabric."

- API import restrictions and known issues
  + htps://docs.microsoft.com/en-us/azure/api-management/api-management-api-import-restrictions
    * Required parameters across both path and query must have unique names.
    * ```\$ref``` pointers can't reference external files.
    * Custom extensions are ignored on import and aren't saved or preserved for export.
    * ```Recursion``` - API Management doesn't support definitions defined recursively (for example, schemas referring to themselves).
    * Source file URL (if available) is applied to relative server URLs.
    * Security definitions are ignored.
    * Inline schema definitions for API operations aren't supported. Schema definitions are defined in the API scope and can be referenced in API operations request or response scopes.
    * A defined URL parameter needs to be part of the URL template.
    * ```server``` object isn't supported on the API operation level.
    * ```Produces``` keyword, which describes MIME types returned by an API, isn't supported.
  + OAS v3
    * ```Examples``` isn't supported, but ```example``` is.


- Import an Azure Function App as an API in Azure API Management
  + https://docs.microsoft.com/en-us/azure/api-management/import-function-app-as-api




## Templates
- https://azure.microsoft.com/en-us/resources/templates/
  + https://github.com/Azure/azure-quickstart-templates

- Create a multi-region Premium tier API Management service
  + https://azure.microsoft.com/en-us/resources/templates/201-api-management-create-with-multiregion/
  + https://github.com/Azure/azure-quickstart-templates/tree/master/201-api-management-create-with-multiregion
  + This template demonstrates how to create API Management service with additional locations. 
  + This template creates API Management service in Premium tier.
  + The template deploys 3 units of Premium, consider the cost before deploying the template.


- Create an API Management service in Internal Virtual network
  + https://azure.microsoft.com/en-us/resources/templates/201-api-management-create-with-internal-vnet/
  + https://github.com/Azure/azure-quickstart-templates/tree/master/201-api-management-create-with-internal-vnet

- Create an API Management service in External Virtual Network
  + https://azure.microsoft.com/en-us/resources/templates/201-api-management-create-with-external-vnet/
  + https://github.com/Azure/azure-quickstart-templates/tree/master/201-api-management-create-with-external-vnet


- Create an API Management service with SSL from KeyVault
  + https://azure.microsoft.com/en-us/resources/templates/101-api-management-key-vault-create/
  + https://github.com/Azure/azure-quickstart-templates/tree/master/101-api-management-key-vault-create


