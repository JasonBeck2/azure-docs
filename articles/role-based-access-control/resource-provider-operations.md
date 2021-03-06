---
title: Azure Resource Manager resource provider operations | Microsoft Docs
description: Lists the operations available for the Microsoft Azure Resource Manager resource providers
services: active-directory
documentationcenter:
author: rolyon
manager: mtillman


ms.service: role-based-access-control
ms.devlang: na
ms.topic: reference
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 10/19/2018
ms.author: rolyon
ms.reviewer: bagovind

---
# Azure Resource Manager resource provider operations

This article lists the operations available for each Azure Resource Manager resource provider. These operations can be used in [custom roles](custom-roles.md) to provide granular [role-based access control (RBAC)](overview.md) to resources in Azure. Operation strings have the following format: `{Company}.{ProviderName}/{resourceType}/{action}`

The resource provider operations are always evolving. To get the latest operations, use [Get-AzureRmProviderOperation](/powershell/module/azurerm.resources/get-azurermprovideroperation) or [az provider operation list](/cli/azure/provider/operation#az-provider-operation-list).

[!INCLUDE [GDPR-related guidance](../../includes/gdpr-intro-sentence.md)]

## Microsoft.AAD

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.AAD/domainServices/delete | Delete Domain Service |
> | Action | Microsoft.AAD/domainServices/oucontainer/delete | Delete Ou Container |
> | Action | Microsoft.AAD/domainServices/oucontainer/read | Read Ou Containers |
> | Action | Microsoft.AAD/domainServices/oucontainer/write | Write Ou Container |
> | Action | Microsoft.AAD/domainServices/read | Read Domain Services |
> | Action | Microsoft.AAD/domainServices/write | Write Domain Service |
> | Action | Microsoft.AAD/locations/operationresults/read |  |
> | Action | Microsoft.AAD/Operations/read |  |
> | Action | Microsoft.AAD/register/action | Register Domain Service |
> | Action | Microsoft.AAD/unregister/action | Unregister Domain Service |

## microsoft.aadiam

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | microsoft.aadiam/diagnosticsettings/delete | Deleting a diagnostic setting |
> | Action | microsoft.aadiam/diagnosticsettings/read | Reading a diagnostic setting |
> | Action | microsoft.aadiam/diagnosticsettings/write | Writing a diagnostic setting |
> | Action | microsoft.aadiam/diagnosticsettingscategories/read | Reading a diagnostic setting categories |
> | Action | microsoft.aadiam/tenants/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | microsoft.aadiam/tenants/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | microsoft.aadiam/tenants/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for tenants |

## Microsoft.Addons

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Addons/operations/read | Gets supported RP operations. |
> | Action | Microsoft.Addons/register/action | Register the specified subscription with Microsoft.Addons |
> | Action | Microsoft.Addons/supportProviders/listsupportplaninfo/action | Lists current support plan information for the specified subscription. |
> | Action | Microsoft.Addons/supportProviders/supportPlanTypes/delete | Removes the specified Canonical support plan |
> | Action | Microsoft.Addons/supportProviders/supportPlanTypes/read | Get the specified Canonical support plan state. |
> | Action | Microsoft.Addons/supportProviders/supportPlanTypes/write | Adds the Canonical support plan type specified. |

## Microsoft.ADHybridHealthService

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ADHybridHealthService/addsservices/action | Create a new forest for the tenant. |
> | Action | Microsoft.ADHybridHealthService/addsservices/addomainservicemembers/read | Gets all servers for the specified service name. |
> | Action | Microsoft.ADHybridHealthService/addsservices/alerts/read | Gets alerts details for the forest like alertid, alert raised date, alert last detected, alert description, last updated, alert level, alert state, alert troubleshooting links etc. . |
> | Action | Microsoft.ADHybridHealthService/addsservices/configuration/read | Gets Service Configuration for the forest. Example- Forest Name, Functional Level, Domain Naming master FSMO role, Schema master FSMO role etc. |
> | Action | Microsoft.ADHybridHealthService/addsservices/delete | Deletes a Service and it's servers along with Health data. |
> | Action | Microsoft.ADHybridHealthService/addsservices/dimensions/read | Gets the domains and sites details for the forest. Example- health status, active alerts, resolved alerts, properties like Domain Functional Level, Forest, Infrastructure Master, PDC, RID master etc.  |
> | Action | Microsoft.ADHybridHealthService/addsservices/features/userpreference/read | Gets the user preference setting for the forest.<br>Example- MetricCounterName like ldapsuccessfulbinds, ntlmauthentications, kerberosauthentications, addsinsightsagentprivatebytes, ldapsearches.<br>Settings for the UI Charts etc. |
> | Action | Microsoft.ADHybridHealthService/addsservices/forestsummary/read | Gets forest summary for the given forest like forest name, number of domains under this forest, number of sites and sites details etc. |
> | Action | Microsoft.ADHybridHealthService/addsservices/metricmetadata/read | Gets the list of supported metrics for a given service.<br>For example Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFS service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomainService.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for ADSync service. |
> | Action | Microsoft.ADHybridHealthService/addsservices/metrics/groups/read | Given a service, this API gets the metrics information.<br>For example, this API can be used to get information related to: Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFederation service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomain Service.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for Sync Service. |
> | Action | Microsoft.ADHybridHealthService/addsservices/premiumcheck/read | This API gets the list of all onboarded ADDomainServices for a premium tenant. |
> | Action | Microsoft.ADHybridHealthService/addsservices/read | Gets Service details for the specified service name. |
> | Action | Microsoft.ADHybridHealthService/addsservices/replicationdetails/read | Gets replication details for all the servers for the specified service name. |
> | Action | Microsoft.ADHybridHealthService/addsservices/replicationstatus/read | Gets the number of domain controllers and their replication errors if any. |
> | Action | Microsoft.ADHybridHealthService/addsservices/replicationsummary/read | Gets complete domain controller list along with replication details for the given forest. |
> | Action | Microsoft.ADHybridHealthService/addsservices/servicemembers/action | Add a server instance to the service. |
> | Action | Microsoft.ADHybridHealthService/addsservices/servicemembers/credentials/read | During server registration of ADDomainService, this api is called to get the credentials for onboarding new servers. |
> | Action | Microsoft.ADHybridHealthService/addsservices/servicemembers/delete | Deletes a server for a given service and tenant. |
> | Action | Microsoft.ADHybridHealthService/addsservices/write | Creates or Updates the ADDomainService instance for the tenant. |
> | Action | Microsoft.ADHybridHealthService/configuration/action | Updates Tenant Configuration. |
> | Action | Microsoft.ADHybridHealthService/configuration/read | Reads the Tenant Configuration. |
> | Action | Microsoft.ADHybridHealthService/configuration/write | Creates a Tenant Configuration. |
> | Action | Microsoft.ADHybridHealthService/logs/contents/read | Gets the content of agent installation and registration logs stored in blob. |
> | Action | Microsoft.ADHybridHealthService/logs/read | Gets agent installation and registration logs for the tenant. |
> | Action | Microsoft.ADHybridHealthService/operations/read | Gets list of operations supported by system. |
> | Action | Microsoft.ADHybridHealthService/register/action | Registers the ADHybrid Health Service Resource Provider and enables the creation of ADHybrid Health Service resource. |
> | Action | Microsoft.ADHybridHealthService/reports/availabledeployments/read | Gets list of available regions, used by DevOps to support customer incidents. |
> | Action | Microsoft.ADHybridHealthService/reports/badpassword/read | Gets the list of bad password attempts for all the users in Active Directory Federation Service. |
> | Action | Microsoft.ADHybridHealthService/reports/badpassworduseridipfrequency/read | Gets Blob SAS URI containing status and eventual result of newly enqueued report job for frequency of Bad Username/Password attempts per UserId per IPAddress per Day for a given Tenant. |
> | Action | Microsoft.ADHybridHealthService/reports/consentedtodevopstenants/read | Gets the list of DevOps consented tenants. Typically used for customer support. |
> | Action | Microsoft.ADHybridHealthService/reports/isdevops/read | Gets a value indicating whether the teannt is DevOps Consented or not. |
> | Action | Microsoft.ADHybridHealthService/reports/selectdevopstenant/read | Updates userid(objectid) for the selected dev ops tenant. |
> | Action | Microsoft.ADHybridHealthService/reports/selecteddeployment/read | Gets selected deployment for the given tenant. |
> | Action | Microsoft.ADHybridHealthService/reports/tenantassigneddeployment/read | Given a tenant id gets the tenant storage location. |
> | Action | Microsoft.ADHybridHealthService/reports/updateselecteddeployment/read | Gets the geo location from which data will be accessed. |
> | Action | Microsoft.ADHybridHealthService/services/action | Updates a service instance in the tenant. |
> | Action | Microsoft.ADHybridHealthService/services/alerts/read | Reads the alerts for a service. |
> | Action | Microsoft.ADHybridHealthService/services/alerts/read | Reads the alerts for a service. |
> | Action | Microsoft.ADHybridHealthService/services/checkservicefeatureavailibility/read | Given a feature name verifies if a service has everything required to use that feature. |
> | Action | Microsoft.ADHybridHealthService/services/delete | Deletes a service instance in the tenant. |
> | Action | Microsoft.ADHybridHealthService/services/exporterrors/read | Gets the export errors for a given sync service. |
> | Action | Microsoft.ADHybridHealthService/services/exportstatus/read | Gets the export status for a given service. |
> | Action | Microsoft.ADHybridHealthService/services/feedbacktype/feedback/read | Gets alerts feedback for a given service and server. |
> | Action | Microsoft.ADHybridHealthService/services/metricmetadata/read | Gets the list of supported metrics for a given service.<br>For example Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFS service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomainService.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for ADSync service. |
> | Action | Microsoft.ADHybridHealthService/services/metrics/groups/average/read | Given a service, this API gets the average for metrics for a given service.<br>For example, this API can be used to get information related to: Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFederation service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomain Service.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for Sync Service. |
> | Action | Microsoft.ADHybridHealthService/services/metrics/groups/read | Given a service, this API gets the metrics information.<br>For example, this API can be used to get information related to: Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFederation service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomain Service.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for Sync Service. |
> | Action | Microsoft.ADHybridHealthService/services/metrics/groups/sum/read | Given a service, this API gets the aggregated view for metrics for a given service.<br>For example, this API can be used to get information related to: Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFederation service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomain Service.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for Sync Service. |
> | Action | Microsoft.ADHybridHealthService/services/monitoringconfiguration/write | Add or updates monitoring configuration for a service. |
> | Action | Microsoft.ADHybridHealthService/services/monitoringconfigurations/read | Gets the monitoring configurations for a given service. |
> | Action | Microsoft.ADHybridHealthService/services/monitoringconfigurations/write | Add or updates monitoring configurations for a service. |
> | Action | Microsoft.ADHybridHealthService/services/premiumcheck/read | This API gets the list of all onboarded services for a premium tenant. |
> | Action | Microsoft.ADHybridHealthService/services/read | Reads the service instances in the tenant. |
> | Action | Microsoft.ADHybridHealthService/services/reports/details/read | Gets report of top 50 users with bad password errors from last 7 days |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/action | Creates a server instance in the service. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/alerts/read | Reads the alerts for a server. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/credentials/read | During server registration, this api is called to get the credentials for onboarding new servers. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/datafreshness/read | For a given server, this API gets a list of  datatypes that are being uploaded by the servers and the latest time for each upload. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/delete | Deletes a server instance in the service. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/exportstatus/read | Gets the Sync Export Error details for a given Sync Service. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/metrics/groups/read | Given a service, this API gets the metrics information.<br>For example, this API can be used to get information related to: Extranet Account Lockouts, Total Failed Requests, Outstanding Token Requests (Proxy), Token Requests /sec etc for ADFederation service.<br>NTLM Authentications/sec, LDAP Successful Binds/sec, LDAP Bind Time, LDAP Active Threads, Kerberos Authentications/sec, ATQ Threads Total etc for ADDomain Service.<br>Run Profile Latency, TCP Connections Established, Insights Agent Private Bytes,Export Statistics to Azure AD for Sync Service. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/read | Reads the server instance in the service. |
> | Action | Microsoft.ADHybridHealthService/services/servicemembers/serviceconfiguration/read | Gets service configuration for a given tenant. |
> | Action | Microsoft.ADHybridHealthService/services/tenantwhitelisting/read | Gets feature whitelisting status for a given tenant. |
> | Action | Microsoft.ADHybridHealthService/services/write | Creates a service instance in the tenant. |
> | Action | Microsoft.ADHybridHealthService/unregister/action | Unregisters the subscription for ADHybrid Health Service Resource Provider. |

## Microsoft.Advisor

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Advisor/configurations/read | Get configurations |
> | Action | Microsoft.Advisor/configurations/write | Creates/updates configuration |
> | Action | Microsoft.Advisor/generateRecommendations/action | Generates recommendations |
> | Action | Microsoft.Advisor/generateRecommendations/read | Gets generate recommendations status |
> | Action | Microsoft.Advisor/operations/read | Gets the operations for the Microsoft Advisor |
> | Action | Microsoft.Advisor/recommendations/available/action | New recommendation is available in Microsoft advisor |
> | Action | Microsoft.Advisor/recommendations/read | Reads recommendations |
> | Action | Microsoft.Advisor/recommendations/suppressions/delete | Deletes suppression |
> | Action | Microsoft.Advisor/recommendations/suppressions/read | Gets suppressions |
> | Action | Microsoft.Advisor/recommendations/suppressions/write | Creates/updates suppressions |
> | Action | Microsoft.Advisor/register/action | Registers the subscription for the Microsoft Advisor |
> | Action | Microsoft.Advisor/suppressions/delete | Deletes suppression |
> | Action | Microsoft.Advisor/suppressions/read | Gets suppressions |
> | Action | Microsoft.Advisor/suppressions/write | Creates/updates suppressions |
> | Action | Microsoft.Advisor/unregister/action | Unregisters the subscription for the Microsoft Advisor |

## Microsoft.AlertsManagement

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.AlertsManagement/alerts/changestate/action | Change the state of the alert. |
> | Action | Microsoft.AlertsManagement/alerts/read | Get all the alerts for the input filters. |
> | Action | Microsoft.AlertsManagement/alertsSummary/read | Get the summary of alerts |
> | Action | Microsoft.AlertsManagement/Operations/read | Reads the operations provided |
> | Action | Microsoft.AlertsManagement/smartGroups/changestate/action | Change the state of the smart group |
> | Action | Microsoft.AlertsManagement/smartGroups/read | Get all the smart groups for the input filters |

## Microsoft.AnalysisServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.AnalysisServices/locations/checkNameAvailability/action | Checks that given Analysis Server name is valid and not in use. |
> | Action | Microsoft.AnalysisServices/locations/operationresults/read | Retrieves the information of the specified operation result. |
> | Action | Microsoft.AnalysisServices/locations/operationstatuses/read | Retrieves the information of the specified operation status. |
> | Action | Microsoft.AnalysisServices/operations/read | Retrieves the information of operations |
> | Action | Microsoft.AnalysisServices/register/action | Registers Analysis Services resource provider. |
> | Action | Microsoft.AnalysisServices/servers/delete | Deletes the Analysis Server. |
> | Action | Microsoft.AnalysisServices/servers/listGatewayStatus/action | List the status of the gateway associated with the server. |
> | Action | Microsoft.AnalysisServices/servers/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for Analysis Server |
> | Action | Microsoft.AnalysisServices/servers/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for Analysis Server |
> | Action | Microsoft.AnalysisServices/servers/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for servers |
> | Action | Microsoft.AnalysisServices/servers/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Analysis Server |
> | Action | Microsoft.AnalysisServices/servers/read | Retrieves the information of the specified Analysis Server. |
> | Action | Microsoft.AnalysisServices/servers/resume/action | Resumes the Analysis Server. |
> | Action | Microsoft.AnalysisServices/servers/skus/read | Retrieve available SKU information for the server |
> | Action | Microsoft.AnalysisServices/servers/suspend/action | Suspends the Analysis Server. |
> | Action | Microsoft.AnalysisServices/servers/write | Creates or updates the specified Analysis Server. |
> | Action | Microsoft.AnalysisServices/skus/read | Retrieves the information of Skus |

## Microsoft.ApiManagement

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ApiManagement/checkNameAvailability/read | Checks if provided service name is available |
> | Action | Microsoft.ApiManagement/operations/read | Read all API operations available for Microsoft.ApiManagement resource |
> | Action | Microsoft.ApiManagement/register/action | Register subscription for Microsoft.ApiManagement resource provider |
> | Action | Microsoft.ApiManagement/reports/read | Get reports aggregated by time periods, geographical region, developers, products, APIs, operations, subscription and byRequest. |
> | Action | Microsoft.ApiManagement/service/apis/delete | Remove existing API |
> | Action | Microsoft.ApiManagement/service/apis/diagnostics/delete | Remove existing diagnostic |
> | Action | Microsoft.ApiManagement/service/apis/diagnostics/read | Get list of diagnostics or Get details of diagnostic |
> | Action | Microsoft.ApiManagement/service/apis/diagnostics/write | Add new diagnostic or Update existing diagnostic details |
> | Action | Microsoft.ApiManagement/service/apis/issues/attachments/delete | Removes existing attachment |
> | Action | Microsoft.ApiManagement/service/apis/issues/attachments/read | Get issue attachments or Gets API Management issue attachment details |
> | Action | Microsoft.ApiManagement/service/apis/issues/attachments/write | Add api issue attachment |
> | Action | Microsoft.ApiManagement/service/apis/issues/comments/delete | Removes existing comment |
> | Action | Microsoft.ApiManagement/service/apis/issues/comments/read | Gets issue comments or Gets API Management issue comment details |
> | Action | Microsoft.ApiManagement/service/apis/issues/comments/write | Add api issue comment |
> | Action | Microsoft.ApiManagement/service/apis/issues/delete | Removes existing issue |
> | Action | Microsoft.ApiManagement/service/apis/issues/read | Get Issues associated with API or Gets API Management issue details |
> | Action | Microsoft.ApiManagement/service/apis/issues/write | Add api issue or Update api issue |
> | Action | Microsoft.ApiManagement/service/apis/operations/delete | Remove existing API operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/policies/delete | Remove policy configuration from API Operation policies |
> | Action | Microsoft.ApiManagement/service/apis/operations/policies/read | Get policies for API Operation or Get policy configuration details for API Operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/policies/write | Set policy configuration details for API Operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/policy/delete | Remove policy configuration from operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/policy/read | Get policy configuration details for operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/policy/write | Set policy configuration details for operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/read | Get list of existing API operations or Get details of API operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/tags/delete | Delete association of existing Tag with existing Operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/tags/read | Get tags associated with the Operation or Get Tag details |
> | Action | Microsoft.ApiManagement/service/apis/operations/tags/write | Associate existing Tag with existing Operation |
> | Action | Microsoft.ApiManagement/service/apis/operations/write | Create new API operation or Update existing API operation |
> | Action | Microsoft.ApiManagement/service/apis/operationsByTags/read | Get list of Operation/Tag associations |
> | Action | Microsoft.ApiManagement/service/apis/policies/delete | Remove policy configuration from API policies |
> | Action | Microsoft.ApiManagement/service/apis/policies/read | Get policies for API or Get policy configuration details for API |
> | Action | Microsoft.ApiManagement/service/apis/policies/write | Set policy configuration details for API |
> | Action | Microsoft.ApiManagement/service/apis/policy/delete | Remove policy configuration from API |
> | Action | Microsoft.ApiManagement/service/apis/policy/read | Get policy configuration details for API |
> | Action | Microsoft.ApiManagement/service/apis/policy/write | Set policy configuration details for API |
> | Action | Microsoft.ApiManagement/service/apis/products/read | Get all products which the API is part of |
> | Action | Microsoft.ApiManagement/service/apis/read | Get list of all registered APIs or Get details of API |
> | Action | Microsoft.ApiManagement/service/apis/releases/delete | Removes all releases of the API or Remove API release |
> | Action | Microsoft.ApiManagement/service/apis/releases/read | Get releases for an API or Get details of API release |
> | Action | Microsoft.ApiManagement/service/apis/releases/write | Create new API release or Update existing API release |
> | Action | Microsoft.ApiManagement/service/apis/revisions/delete | Removes all revisions of an API |
> | Action | Microsoft.ApiManagement/service/apis/revisions/read | Get revisions belonging to an API |
> | Action | Microsoft.ApiManagement/service/apis/schemas/delete | Removes existing Schema |
> | Action | Microsoft.ApiManagement/service/apis/schemas/document/read | Get the document describing the Schema |
> | Action | Microsoft.ApiManagement/service/apis/schemas/document/write | Update the document describing the Schema |
> | Action | Microsoft.ApiManagement/service/apis/schemas/read | Gets all the schemas for a given API or Gets the Schemas used by the API |
> | Action | Microsoft.ApiManagement/service/apis/schemas/write | Sets the Schemas used by the API |
> | Action | Microsoft.ApiManagement/service/apis/tagDescriptions/delete | Remove Tag description from the API |
> | Action | Microsoft.ApiManagement/service/apis/tagDescriptions/read | Get Tags descriptions in scope of API or Get Tag description in scope of API |
> | Action | Microsoft.ApiManagement/service/apis/tagDescriptions/write | Create/Change Tag description in scope of API |
> | Action | Microsoft.ApiManagement/service/apis/tags/delete | Remove existing API/Tag association |
> | Action | Microsoft.ApiManagement/service/apis/tags/read | Get all API/Tag association for the API or Get details of API/Tag association |
> | Action | Microsoft.ApiManagement/service/apis/tags/write | Add new API/Tag association |
> | Action | Microsoft.ApiManagement/service/apis/write | Create new API or Update existing API details |
> | Action | Microsoft.ApiManagement/service/apisByTags/read | Get list of API/Tag associations |
> | Action | Microsoft.ApiManagement/service/api-version-sets/delete | Remove existing VersionSet |
> | Action | Microsoft.ApiManagement/service/api-version-sets/read | Get list of version group entities or Gets details of a VersionSet |
> | Action | Microsoft.ApiManagement/service/api-version-sets/versions/read | Get list of version entities |
> | Action | Microsoft.ApiManagement/service/api-version-sets/write | Create new VersionSet or Update existing VersionSet details |
> | Action | Microsoft.ApiManagement/service/applynetworkconfigurationupdates/action | Updates the Microsoft.ApiManagement resources running in Virtual Network to pick updated Network Settings. |
> | Action | Microsoft.ApiManagement/service/authorizationServers/delete | Remove existing authorization server |
> | Action | Microsoft.ApiManagement/service/authorizationServers/read | Get list of authorization servers or Get details of authorization server |
> | Action | Microsoft.ApiManagement/service/authorizationServers/write | Create a new authorization server or Update details of an existing authorization server |
> | Action | Microsoft.ApiManagement/service/backends/delete | Remove existing backend |
> | Action | Microsoft.ApiManagement/service/backends/read | Get list of backends or Get details of backend |
> | Action | Microsoft.ApiManagement/service/backends/reconnect/action | Create a Reconnect Request |
> | Action | Microsoft.ApiManagement/service/backends/write | Add a new backend or Update existing backend details |
> | Action | Microsoft.ApiManagement/service/backup/action | Backup API Management Service to the specified container in a user provided storage account |
> | Action | Microsoft.ApiManagement/service/certificates/delete | Remove existing certificate |
> | Action | Microsoft.ApiManagement/service/certificates/read | Get list of certificates or Get details of certificate |
> | Action | Microsoft.ApiManagement/service/certificates/write | Add new certificate |
> | Action | Microsoft.ApiManagement/service/delete | Delete API Management Service instance |
> | Action | Microsoft.ApiManagement/service/diagnostics/delete | Remove existing diagnostic |
> | Action | Microsoft.ApiManagement/service/diagnostics/read | Get list of diagnostics or Get details of diagnostic |
> | Action | Microsoft.ApiManagement/service/diagnostics/write | Add new diagnostic or Update existing diagnostic details |
> | Action | Microsoft.ApiManagement/service/getssotoken/action | Gets SSO token that can be used to login into API Management Service Legacy portal as an administrator |
> | Action | Microsoft.ApiManagement/service/groups/delete | Remove existing group |
> | Action | Microsoft.ApiManagement/service/groups/read | Get list of groups or Gets details of a group |
> | Action | Microsoft.ApiManagement/service/groups/users/delete | Remove existing user from existing group |
> | Action | Microsoft.ApiManagement/service/groups/users/read | Get list of group users |
> | Action | Microsoft.ApiManagement/service/groups/users/write | Add existing user to existing group |
> | Action | Microsoft.ApiManagement/service/groups/write | Create new group or Update existing group details |
> | Action | Microsoft.ApiManagement/service/identityProviders/delete | Remove existing Identity Provider |
> | Action | Microsoft.ApiManagement/service/identityProviders/read | Get list of Identity providers or Get details of Identity Provider |
> | Action | Microsoft.ApiManagement/service/identityProviders/write | Create a new Identity Provider or Update details of an existing Identity Provider |
> | Action | Microsoft.ApiManagement/service/locations/networkstatus/read | Gets the network access status of resources on which the service depends on in the location. |
> | Action | Microsoft.ApiManagement/service/loggers/delete | Remove existing logger |
> | Action | Microsoft.ApiManagement/service/loggers/read | Get list of loggers or Get details of logger |
> | Action | Microsoft.ApiManagement/service/loggers/write | Add new logger or Update existing logger details |
> | Action | Microsoft.ApiManagement/service/managedeployments/action | Change SKU/units, add/remove regional deployments of API Management Service |
> | Action | Microsoft.ApiManagement/service/networkstatus/read | Gets the network access status of resources on which the service depends on. |
> | Action | Microsoft.ApiManagement/service/notifications/action | Sends notification to a specified user |
> | Action | Microsoft.ApiManagement/service/notifications/read | Gets all API Management publisher notifications or Get API Management publisher notification details |
> | Action | Microsoft.ApiManagement/service/notifications/recipientEmails/delete | Removes existing Email associated with a Notification |
> | Action | Microsoft.ApiManagement/service/notifications/recipientEmails/read | Get Email Recipients associated with API Management Publisher Notification |
> | Action | Microsoft.ApiManagement/service/notifications/recipientEmails/write | Create new Email Recipient of the Notification |
> | Action | Microsoft.ApiManagement/service/notifications/recipientUsers/delete | Removes User associated to the Notification Recipients |
> | Action | Microsoft.ApiManagement/service/notifications/recipientUsers/read | Get Recipient Users associated with the Notification |
> | Action | Microsoft.ApiManagement/service/notifications/recipientUsers/write | Add User to the Notification Recipients |
> | Action | Microsoft.ApiManagement/service/notifications/write | Create or Update API Management publisher notification |
> | Action | Microsoft.ApiManagement/service/openidConnectProviders/delete | Remove existing OpenID Connect Provider |
> | Action | Microsoft.ApiManagement/service/openidConnectProviders/read | Get list of OpenID Connect providers or Get details of OpenID Connect Provider |
> | Action | Microsoft.ApiManagement/service/openidConnectProviders/write | Create a new OpenID Connect Provider or Update details of an existing OpenID Connect Provider |
> | Action | Microsoft.ApiManagement/service/operationresults/read | Gets current status of long running operation |
> | Action | Microsoft.ApiManagement/service/policies/delete | Remove policy configuration from Tenant policies |
> | Action | Microsoft.ApiManagement/service/policies/read | Get policies for Tenant or Get policy configuration details for Tenant |
> | Action | Microsoft.ApiManagement/service/policies/write | Set policy configuration details for Tenant |
> | Action | Microsoft.ApiManagement/service/policySnippets/read | Get all policy snippets |
> | Action | Microsoft.ApiManagement/service/portalsettings/read | Get Sign Up Settings for the Portal or Get Sign In Settings for the Portal or Get Delegation Settings for the Portal |
> | Action | Microsoft.ApiManagement/service/portalsettings/write | Update Sign Up settings or Update Sign Up settings or Update Sign In settings or Update Sign In settings or Update Delegation settings or Update Delegation settings |
> | Action | Microsoft.ApiManagement/service/products/apis/delete | Remove existing API from existing product |
> | Action | Microsoft.ApiManagement/service/products/apis/read | Get list of APIs added to existing product |
> | Action | Microsoft.ApiManagement/service/products/apis/write | Add existing API to existing product |
> | Action | Microsoft.ApiManagement/service/products/delete | Remove existing product |
> | Action | Microsoft.ApiManagement/service/products/groups/delete | Delete association of existing developer group with existing product |
> | Action | Microsoft.ApiManagement/service/products/groups/read | Get list of developer groups associated with product |
> | Action | Microsoft.ApiManagement/service/products/groups/write | Associate existing developer group with existing product |
> | Action | Microsoft.ApiManagement/service/products/policies/delete | Remove policy configuration from Product policies |
> | Action | Microsoft.ApiManagement/service/products/policies/read | Get policies for Product or Get policy configuration details for Product |
> | Action | Microsoft.ApiManagement/service/products/policies/write | Set policy configuration details for Product |
> | Action | Microsoft.ApiManagement/service/products/policy/delete | Remove policy configuration from existing product |
> | Action | Microsoft.ApiManagement/service/products/policy/read | Get policy configuration of existing product |
> | Action | Microsoft.ApiManagement/service/products/policy/write | Set policy configuration for existing product |
> | Action | Microsoft.ApiManagement/service/products/read | Get list of products or Get details of product |
> | Action | Microsoft.ApiManagement/service/products/subscriptions/read | Get list of product subscriptions |
> | Action | Microsoft.ApiManagement/service/products/tags/delete | Delete association of existing Tag with existing Product |
> | Action | Microsoft.ApiManagement/service/products/tags/read | Get tags associated with the Product or Get Tag details |
> | Action | Microsoft.ApiManagement/service/products/tags/write | Associate existing Tag with existing Product |
> | Action | Microsoft.ApiManagement/service/products/write | Create new product or Update existing product details |
> | Action | Microsoft.ApiManagement/service/productsByTags/read | Get list of Product/Tag associations |
> | Action | Microsoft.ApiManagement/service/properties/delete | Removes existing property |
> | Action | Microsoft.ApiManagement/service/properties/read | Gets list of all properties or Gets details of specified property |
> | Action | Microsoft.ApiManagement/service/properties/write | Creates a new property or Updates value for specified property |
> | Action | Microsoft.ApiManagement/service/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for API Management service |
> | Action | Microsoft.ApiManagement/service/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for API Management service |
> | Action | Microsoft.ApiManagement/service/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for API Management service |
> | Action | Microsoft.ApiManagement/service/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for API Management service |
> | Action | Microsoft.ApiManagement/service/quotas/periods/read | Get quota counter value for period |
> | Action | Microsoft.ApiManagement/service/quotas/periods/write | Set quota counter current value |
> | Action | Microsoft.ApiManagement/service/quotas/read | Get values for quota |
> | Action | Microsoft.ApiManagement/service/quotas/write | Set quota counter current value |
> | Action | Microsoft.ApiManagement/service/read | Read metadata for an API Management Service instance |
> | Action | Microsoft.ApiManagement/service/reports/read | Get report aggregated by time periods or Get report aggregated by geographical region or Get report aggregated by developers.<br>or Get report aggregated by products.<br>or Get report aggregated by APIs or Get report aggregated by operations or Get report aggregated by subscription.<br>or Get requests reporting data |
> | Action | Microsoft.ApiManagement/service/restore/action | Restore API Management Service from the specified container in a user provided storage account |
> | Action | Microsoft.ApiManagement/service/subscriptions/delete | Delete subscription. This operation can be used to delete subscription |
> | Action | Microsoft.ApiManagement/service/subscriptions/read | Get a list of product subscriptions or Get details of product subscription |
> | Action | Microsoft.ApiManagement/service/subscriptions/regeneratePrimaryKey/action | Regenerate subscription primary key |
> | Action | Microsoft.ApiManagement/service/subscriptions/regenerateSecondaryKey/action | Regenerate subscription secondary key |
> | Action | Microsoft.ApiManagement/service/subscriptions/write | Subscribe an existing user to an existing product or Update existing subscription details. This operation can be used to renew subscription |
> | Action | Microsoft.ApiManagement/service/tagResources/read | Get list of Tags with associated Resources |
> | Action | Microsoft.ApiManagement/service/tags/delete | Remove existing Tag |
> | Action | Microsoft.ApiManagement/service/tags/read | Get list of Tags or Get details of Tag |
> | Action | Microsoft.ApiManagement/service/tags/write | Add new Tag or Update existing Tag details |
> | Action | Microsoft.ApiManagement/service/templates/delete | Reset default API Management email template |
> | Action | Microsoft.ApiManagement/service/templates/read | Gets all email templates or Gets API Management email template details |
> | Action | Microsoft.ApiManagement/service/templates/write | Create or update API Management email template or Updates API Management email template |
> | Action | Microsoft.ApiManagement/service/tenant/delete | Remove policy configuration for the tenant |
> | Action | Microsoft.ApiManagement/service/tenant/deploy/action | Runs a deployment task to apply changes from the specified git branch to the configuration in database. |
> | Action | Microsoft.ApiManagement/service/tenant/operationResults/read | Get list of operation results or Get result of a specific operation |
> | Action | Microsoft.ApiManagement/service/tenant/read | Get policy configuration for the tenant or Get tenant access information details |
> | Action | Microsoft.ApiManagement/service/tenant/regeneratePrimaryKey/action | Regenerate primary access key |
> | Action | Microsoft.ApiManagement/service/tenant/regenerateSecondaryKey/action | Regenerate secondary access key |
> | Action | Microsoft.ApiManagement/service/tenant/save/action | Creates commit with configuration snapshot to the specified branch in the repository |
> | Action | Microsoft.ApiManagement/service/tenant/syncState/read | Get status of last git synchronization |
> | Action | Microsoft.ApiManagement/service/tenant/validate/action | Validates changes from the specified git branch |
> | Action | Microsoft.ApiManagement/service/tenant/write | Set policy configuration for the tenant or Update tenant access information details |
> | Action | Microsoft.ApiManagement/service/updatecertificate/action | Upload SSL certificate for an API Management Service |
> | Action | Microsoft.ApiManagement/service/updatehostname/action | Setup, update or remove custom domain names for an API Management Service |
> | Action | Microsoft.ApiManagement/service/users/action | Register a new user |
> | Action | Microsoft.ApiManagement/service/users/applications/attachments/delete | Removes an attachment |
> | Action | Microsoft.ApiManagement/service/users/applications/attachments/read | Gets application attachments or Gets attachment |
> | Action | Microsoft.ApiManagement/service/users/applications/attachments/write | Add Attachment to application |
> | Action | Microsoft.ApiManagement/service/users/applications/delete | Removes existing application |
> | Action | Microsoft.ApiManagement/service/users/applications/read | Get list of all user applications or Gets API Management application details |
> | Action | Microsoft.ApiManagement/service/users/applications/write | Registers an application to API Management or Updates application details |
> | Action | Microsoft.ApiManagement/service/users/delete | Remove user account |
> | Action | Microsoft.ApiManagement/service/users/generateSsoUrl/action | Generate SSO URL. The URL can be used to access admin portal |
> | Action | Microsoft.ApiManagement/service/users/groups/read | Get list of user groups |
> | Action | Microsoft.ApiManagement/service/users/keys/read | Get list of user keys |
> | Action | Microsoft.ApiManagement/service/users/read | Get a list of registered users or Get account details of a user |
> | Action | Microsoft.ApiManagement/service/users/subscriptions/read | Get list of user subscriptions |
> | Action | Microsoft.ApiManagement/service/users/token/action | Get token access token for a user |
> | Action | Microsoft.ApiManagement/service/users/write | Register a new user or Update account details of an existing user |
> | Action | Microsoft.ApiManagement/service/write | Create a new instance of API Management Service |
> | Action | Microsoft.ApiManagement/unregister/action | Un-register subscription for Microsoft.ApiManagement resource provider |

## Microsoft.Authorization

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Authorization/checkAccess/action | Checks if the caller is authorized to perform a particular action |
> | Action | Microsoft.Authorization/classicAdministrators/delete | Removes the administrator from the subscription. |
> | Action | Microsoft.Authorization/classicAdministrators/operationstatuses/read | Gets the administrator operation statuses of the subscription. |
> | Action | Microsoft.Authorization/classicAdministrators/read | Reads the administrators for the subscription. |
> | Action | Microsoft.Authorization/classicAdministrators/write | Add or modify administrator to a subscription. |
> | Action | Microsoft.Authorization/denyAssignments/delete | Delete a deny assignment at the specified scope. |
> | Action | Microsoft.Authorization/denyAssignments/read | Get information about a deny assignment. |
> | Action | Microsoft.Authorization/denyAssignments/write | Create a deny assignment at the specified scope. |
> | Action | Microsoft.Authorization/elevateAccess/action | Grants the caller User Access Administrator access at the tenant scope |
> | Action | Microsoft.Authorization/locks/delete | Delete locks at the specified scope. |
> | Action | Microsoft.Authorization/locks/read | Gets locks at the specified scope. |
> | Action | Microsoft.Authorization/locks/write | Add locks at the specified scope. |
> | Action | Microsoft.Authorization/operations/read | Gets the list of operations |
> | Action | Microsoft.Authorization/permissions/read | Lists all the permissions the caller has at a given scope. |
> | Action | Microsoft.Authorization/policyAssignments/delete | Delete a policy assignment at the specified scope. |
> | Action | Microsoft.Authorization/policyAssignments/read | Get information about a policy assignment. |
> | Action | Microsoft.Authorization/policyAssignments/write | Create a policy assignment at the specified scope. |
> | Action | Microsoft.Authorization/policyDefinitions/delete | Delete a policy definition. |
> | Action | Microsoft.Authorization/policyDefinitions/read | Get information about a policy definition. |
> | Action | Microsoft.Authorization/policyDefinitions/write | Create a custom policy definition. |
> | Action | Microsoft.Authorization/policySetDefinitions/delete | Delete a policy set definition. |
> | Action | Microsoft.Authorization/policySetDefinitions/read | Get information about a policy set definition. |
> | Action | Microsoft.Authorization/policySetDefinitions/write | Create a custom policy set definition. |
> | Action | Microsoft.Authorization/providerOperations/read | Get operations for all resource providers which can be used in role definitions. |
> | Action | Microsoft.Authorization/roleAssignments/delete | Delete a role assignment at the specified scope. |
> | Action | Microsoft.Authorization/roleAssignments/read | Get information about a role assignment. |
> | Action | Microsoft.Authorization/roleAssignments/write | Create a role assignment at the specified scope. |
> | Action | Microsoft.Authorization/roleDefinitions/delete | Delete the specified custom role definition. |
> | Action | Microsoft.Authorization/roleDefinitions/read | Get information about a role definition. |
> | Action | Microsoft.Authorization/roleDefinitions/write | Create or update a custom role definition with specified permissions and assignable scopes. |

## Microsoft.Automation

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Automation/automationAccounts/agentRegistrationInformation/read | Read an Azure Automation DSC's registration information |
> | Action | Microsoft.Automation/automationAccounts/agentRegistrationInformation/regenerateKey/action | Writes a request to regenerate Azure Automation DSC keys |
> | Action | Microsoft.Automation/automationAccounts/certificates/delete | Deletes an Azure Automation certificate asset |
> | Action | Microsoft.Automation/automationAccounts/certificates/getCount/action | Reads the count of certificates |
> | Action | Microsoft.Automation/automationAccounts/certificates/read | Gets an Azure Automation certificate asset |
> | Action | Microsoft.Automation/automationAccounts/certificates/write | Creates or updates an Azure Automation certificate asset |
> | Action | Microsoft.Automation/automationAccounts/compilationjobs/read | Reads an Azure Automation DSC's Compilation |
> | Action | Microsoft.Automation/automationAccounts/compilationjobs/read | Reads an Azure Automation DSC's Compilation |
> | Action | Microsoft.Automation/automationAccounts/compilationjobs/write | Writes an Azure Automation DSC's Compilation |
> | Action | Microsoft.Automation/automationAccounts/compilationjobs/write | Writes an Azure Automation DSC's Compilation |
> | Action | Microsoft.Automation/automationAccounts/configurations/content/read | Reads the configuration media content |
> | Action | Microsoft.Automation/automationAccounts/configurations/delete | Deletes an Azure Automation DSC's content |
> | Action | Microsoft.Automation/automationAccounts/configurations/getCount/action | Reads the count of an Azure Automation DSC's content |
> | Action | Microsoft.Automation/automationAccounts/configurations/read | Gets an Azure Automation DSC's content |
> | Action | Microsoft.Automation/automationAccounts/configurations/write | Writes an Azure Automation DSC's content |
> | Action | Microsoft.Automation/automationAccounts/connections/delete | Deletes an Azure Automation connection asset |
> | Action | Microsoft.Automation/automationAccounts/connections/getCount/action | Reads the count of connections |
> | Action | Microsoft.Automation/automationAccounts/connections/read | Gets an Azure Automation connection asset |
> | Action | Microsoft.Automation/automationAccounts/connections/write | Creates or updates an Azure Automation connection asset |
> | Action | Microsoft.Automation/automationAccounts/connectionTypes/delete | Deletes an Azure Automation connection type asset |
> | Action | Microsoft.Automation/automationAccounts/connectionTypes/read | Gets an Azure Automation connection type asset |
> | Action | Microsoft.Automation/automationAccounts/connectionTypes/write | Creates an Azure Automation connection type asset |
> | Action | Microsoft.Automation/automationAccounts/credentials/delete | Deletes an Azure Automation credential asset |
> | Action | Microsoft.Automation/automationAccounts/credentials/getCount/action | Reads the count of credentials |
> | Action | Microsoft.Automation/automationAccounts/credentials/read | Gets an Azure Automation credential asset |
> | Action | Microsoft.Automation/automationAccounts/credentials/write | Creates or updates an Azure Automation credential asset |
> | Action | Microsoft.Automation/automationAccounts/delete | Deletes an Azure Automation account |
> | Action | Microsoft.Automation/automationAccounts/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Automation/automationAccounts/diagnosticSettings/write | Sets the diagnostic setting for the resource |
> | Action | Microsoft.Automation/automationAccounts/hybridRunbookWorkerGroups/delete | Deletes Hybrid Runbook Worker Resources |
> | Action | Microsoft.Automation/automationAccounts/hybridRunbookWorkerGroups/read | Reads Hybrid Runbook Worker Resources |
> | Action | Microsoft.Automation/automationAccounts/jobs/output/read | Gets the output of a job |
> | Action | Microsoft.Automation/automationAccounts/jobs/read | Gets an Azure Automation job |
> | Action | Microsoft.Automation/automationAccounts/jobs/resume/action | Resumes an Azure Automation job |
> | Action | Microsoft.Automation/automationAccounts/jobs/runbookContent/action | Gets the content of the Azure Automation runbook at the time of the job execution |
> | Action | Microsoft.Automation/automationAccounts/jobs/stop/action | Stops an Azure Automation job |
> | Action | Microsoft.Automation/automationAccounts/jobs/streams/read | Gets an Azure Automation job stream |
> | Action | Microsoft.Automation/automationAccounts/jobs/streams/read | Gets an Azure Automation job stream |
> | Action | Microsoft.Automation/automationAccounts/jobs/suspend/action | Suspends an Azure Automation job |
> | Action | Microsoft.Automation/automationAccounts/jobs/write | Creates an Azure Automation job |
> | Action | Microsoft.Automation/automationAccounts/jobSchedules/delete | Deletes an Azure Automation job schedule |
> | Action | Microsoft.Automation/automationAccounts/jobSchedules/read | Gets an Azure Automation job schedule |
> | Action | Microsoft.Automation/automationAccounts/jobSchedules/write | Creates an Azure Automation job schedule |
> | Action | Microsoft.Automation/automationAccounts/linkedWorkspace/read | Gets the workspace linked to the automation account |
> | Action | Microsoft.Automation/automationAccounts/listKeys/action | Reads the Keys for the automation account |
> | Action | Microsoft.Automation/automationAccounts/logDefinitions/read | Gets the available logs for the automation account |
> | Action | Microsoft.Automation/automationAccounts/modules/activities/read | Gets Azure Automation Activities |
> | Action | Microsoft.Automation/automationAccounts/modules/delete | Deletes an Azure Automation Powershell module |
> | Action | Microsoft.Automation/automationAccounts/modules/getCount/action | Gets the count of Powershell modules within the Automation Account |
> | Action | Microsoft.Automation/automationAccounts/modules/read | Gets an Azure Automation Powershell module |
> | Action | Microsoft.Automation/automationAccounts/modules/write | Creates or updates an Azure Automation Powershell module |
> | Action | Microsoft.Automation/automationAccounts/nodeConfigurations/delete | Deletes an Azure Automation DSC's node configuration |
> | Action | Microsoft.Automation/automationAccounts/nodeConfigurations/rawContent/action | Reads an Azure Automation DSC's node configuration content |
> | Action | Microsoft.Automation/automationAccounts/nodeConfigurations/read | Reads an Azure Automation DSC's node configuration |
> | Action | Microsoft.Automation/automationAccounts/nodeConfigurations/write | Writes an Azure Automation DSC's node configuration |
> | Action | Microsoft.Automation/automationAccounts/nodecounts/read | Reads node count summary for the specified type |
> | Action | Microsoft.Automation/automationAccounts/nodes/delete | Deletes Azure Automation DSC nodes |
> | Action | Microsoft.Automation/automationAccounts/nodes/read | Reads Azure Automation DSC nodes |
> | Action | Microsoft.Automation/automationAccounts/nodes/reports/content/read | Reads Azure Automation DSC report contents |
> | Action | Microsoft.Automation/automationAccounts/nodes/reports/read | Reads Azure Automation DSC reports |
> | Action | Microsoft.Automation/automationAccounts/nodes/write | Creates or updates Azure Automation DSC nodes |
> | Action | Microsoft.Automation/automationAccounts/objectDataTypes/fields/read | Gets Azure Automation TypeFields |
> | Action | Microsoft.Automation/automationAccounts/providers/Microsoft.Insights/metricDefinitions/read | Gets Automation Metric Definitions |
> | Action | Microsoft.Automation/automationAccounts/python2Packages/delete | Deletes an Azure Automation Python 2 package |
> | Action | Microsoft.Automation/automationAccounts/python2Packages/read | Gets an Azure Automation Python 2 package |
> | Action | Microsoft.Automation/automationAccounts/python2Packages/write | Creates or updates an Azure Automation Python 2 package |
> | Action | Microsoft.Automation/automationAccounts/python3Packages/delete | Deletes an Azure Automation Python 3 package |
> | Action | Microsoft.Automation/automationAccounts/python3Packages/read | Gets an Azure Automation Python 3 package |
> | Action | Microsoft.Automation/automationAccounts/python3Packages/write | Creates or updates an Azure Automation Python 3 package |
> | Action | Microsoft.Automation/automationAccounts/read | Gets an Azure Automation account |
> | Action | Microsoft.Automation/automationAccounts/runbooks/content/read | Gets the content of an Azure Automation runbook |
> | Action | Microsoft.Automation/automationAccounts/runbooks/delete | Deletes an Azure Automation runbook |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/content/write | Creates the content of an Azure Automation runbook draft |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/operationResults/read | Gets Azure Automation runbook draft operation results |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/read | Gets an Azure Automation runbook draft |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/testJob/read | Gets an Azure Automation runbook draft test job |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/testJob/resume/action | Resumes an Azure Automation runbook draft test job |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/testJob/stop/action | Stops an Azure Automation runbook draft test job |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/testJob/suspend/action | Suspends an Azure Automation runbook draft test job |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/testJob/write | Creates an Azure Automation runbook draft test job |
> | Action | Microsoft.Automation/automationAccounts/runbooks/draft/undoEdit/action | Undo edits to an Azure Automation runbook draft |
> | Action | Microsoft.Automation/automationAccounts/runbooks/getCount/action | Gets the count of Azure Automation runbooks |
> | Action | Microsoft.Automation/automationAccounts/runbooks/publish/action | Publishes an Azure Automation runbook draft |
> | Action | Microsoft.Automation/automationAccounts/runbooks/read | Gets an Azure Automation runbook |
> | Action | Microsoft.Automation/automationAccounts/runbooks/write | Creates or updates an Azure Automation runbook |
> | Action | Microsoft.Automation/automationAccounts/schedules/delete | Deletes an Azure Automation schedule asset |
> | Action | Microsoft.Automation/automationAccounts/schedules/getCount/action | Gets the count of Azure Automation schedules |
> | Action | Microsoft.Automation/automationAccounts/schedules/read | Gets an Azure Automation schedule asset |
> | Action | Microsoft.Automation/automationAccounts/schedules/write | Creates or updates an Azure Automation schedule asset |
> | Action | Microsoft.Automation/automationAccounts/softwareUpdateConfigurations/delete | Deletes an Azure Automation Software Update Configuration |
> | Action | Microsoft.Automation/automationAccounts/softwareUpdateConfigurations/read | Gets an Azure Automation Software Update Configuration |
> | Action | Microsoft.Automation/automationAccounts/softwareUpdateConfigurations/write | Creates or updates Azure Automation Software Update Configuration |
> | Action | Microsoft.Automation/automationAccounts/statistics/read | Gets Azure Automation Statistics |
> | Action | Microsoft.Automation/automationAccounts/updateDeploymentMachineRuns/read | Get an Azure Automation update deployment machine |
> | Action | Microsoft.Automation/automationAccounts/updateManagementPatchJob/read | Gets an Azure Automation update management patch job |
> | Action | Microsoft.Automation/automationAccounts/usages/read | Gets Azure Automation Usage |
> | Action | Microsoft.Automation/automationAccounts/variables/delete | Deletes an Azure Automation variable asset |
> | Action | Microsoft.Automation/automationAccounts/variables/read | Reads an Azure Automation variable asset |
> | Action | Microsoft.Automation/automationAccounts/variables/write | Creates or updates an Azure Automation variable asset |
> | Action | Microsoft.Automation/automationAccounts/watchers/delete | Delete an Azure Automation watcher job |
> | Action | Microsoft.Automation/automationAccounts/watchers/read | Gets an Azure Automation watcher job |
> | Action | Microsoft.Automation/automationAccounts/watchers/start/action | Start an Azure Automation watcher job |
> | Action | Microsoft.Automation/automationAccounts/watchers/stop/action | Stop an Azure Automation watcher job |
> | Action | Microsoft.Automation/automationAccounts/watchers/streams/read | Gets an Azure Automation watcher job stream |
> | Action | Microsoft.Automation/automationAccounts/watchers/watcherActions/delete | Delete an Azure Automation watcher job actions |
> | Action | Microsoft.Automation/automationAccounts/watchers/watcherActions/read | Gets an Azure Automation watcher job actions |
> | Action | Microsoft.Automation/automationAccounts/watchers/watcherActions/write | Create an Azure Automation watcher job actions |
> | Action | Microsoft.Automation/automationAccounts/watchers/write | Creates an Azure Automation watcher job |
> | Action | Microsoft.Automation/automationAccounts/webhooks/action | Generates a URI for an Azure Automation webhook |
> | Action | Microsoft.Automation/automationAccounts/webhooks/delete | Deletes an Azure Automation webhook  |
> | Action | Microsoft.Automation/automationAccounts/webhooks/read | Reads an Azure Automation webhook |
> | Action | Microsoft.Automation/automationAccounts/webhooks/write | Creates or updates an Azure Automation webhook |
> | Action | Microsoft.Automation/automationAccounts/write | Creates or updates an Azure Automation account |
> | Action | Microsoft.Automation/operations/read | Gets Available Operations for Azure Automation resources |
> | Action | Microsoft.Automation/register/action | Registers the subscription to Azure Automation |

## Microsoft.AzureActiveDirectory

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.AzureActiveDirectory/b2cDirectories/delete | Delete B2C Directory resource |
> | Action | Microsoft.AzureActiveDirectory/b2cDirectories/read | View B2C Directory resource |
> | Action | Microsoft.AzureActiveDirectory/b2cDirectories/write | Create or update B2C Directory resource |
> | Action | Microsoft.AzureActiveDirectory/operations/read | Read all API operations available for Microsoft.AzureActiveDirectory resource provider |
> | Action | Microsoft.AzureActiveDirectory/register/action | Register subscription for Microsoft.AzureActiveDirectory resource provider |

## Microsoft.AzureStack

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.AzureStack/Operations/read | Gets the properties of a resource provider operation |
> | Action | Microsoft.AzureStack/register/action | Registers Subscription with Microsoft.AzureStack resource provider |
> | Action | Microsoft.AzureStack/registrations/customerSubscriptions/delete | Deletes an Azure Stack Customer Subscription |
> | Action | Microsoft.AzureStack/registrations/customerSubscriptions/read | Gets the properties of an Azure Stack Customer Subscription |
> | Action | Microsoft.AzureStack/registrations/customerSubscriptions/write | Creates or updates an Azure Stack Customer Subscription |
> | Action | Microsoft.AzureStack/registrations/delete | Deletes an Azure Stack registration |
> | Action | Microsoft.AzureStack/registrations/getActivationKey/action | Gets the latest Azure Stack activation key |
> | Action | Microsoft.AzureStack/registrations/products/listDetails/action | Retrieves extended details for an Azure Stack Marketplace product |
> | Action | Microsoft.AzureStack/registrations/products/read | Gets the properties of an Azure Stack Marketplace product |
> | Action | Microsoft.AzureStack/registrations/read | Gets the properties of an Azure Stack registration |
> | Action | Microsoft.AzureStack/registrations/write | Creates or updates an Azure Stack registration |

## Microsoft.Batch

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Batch/batchAccounts/applications/delete | Deletes an application |
> | Action | Microsoft.Batch/batchAccounts/applications/read | Lists applications or gets the properties of an application |
> | Action | Microsoft.Batch/batchAccounts/applications/versions/activate/action | Activates an application package |
> | Action | Microsoft.Batch/batchAccounts/applications/versions/delete | Deletes an application package |
> | Action | Microsoft.Batch/batchAccounts/applications/versions/read | Gets the properties of an application package |
> | Action | Microsoft.Batch/batchAccounts/applications/versions/write | Creates a new application package or updates an existing application package |
> | Action | Microsoft.Batch/batchAccounts/applications/write | Creates a new application or updates an existing application |
> | Action | Microsoft.Batch/batchAccounts/certificateOperationResults/read | Gets the results of a long running certificate operation on a Batch account |
> | Action | Microsoft.Batch/batchAccounts/certificates/cancelDelete/action | Cancels the failed deletion of a certificate on a Batch account |
> | Action | Microsoft.Batch/batchAccounts/certificates/delete | Deletes a certificate from a Batch account |
> | Action | Microsoft.Batch/batchAccounts/certificates/read | Lists certificates on a Batch account or gets the properties of a certificate |
> | Action | Microsoft.Batch/batchAccounts/certificates/write | Creates a new certificate on a Batch account or updates an existing certificate |
> | Action | Microsoft.Batch/batchAccounts/delete | Deletes a Batch account |
> | Action | Microsoft.Batch/batchAccounts/listkeys/action | Lists access keys for a Batch account |
> | Action | Microsoft.Batch/batchAccounts/operationResults/read | Gets the results of a long running Batch account operation |
> | Action | Microsoft.Batch/batchAccounts/poolOperationResults/read | Gets the results of a long running pool operation on a Batch account |
> | Action | Microsoft.Batch/batchAccounts/pools/delete | Deletes a pool from a Batch account |
> | Action | Microsoft.Batch/batchAccounts/pools/disableAutoscale/action | Disables automatic scaling for a Batch account pool |
> | Action | Microsoft.Batch/batchAccounts/pools/read | Lists pools on a Batch account or gets the properties of a pool |
> | Action | Microsoft.Batch/batchAccounts/pools/stopResize/action | Stops an ongoing resize operation on a Batch account pool |
> | Action | Microsoft.Batch/batchAccounts/pools/upgradeOs/action | Upgrades the operating system of a Batch account pool |
> | Action | Microsoft.Batch/batchAccounts/pools/write | Creates a new pool on a Batch account or updates an existing pool |
> | Action | Microsoft.Batch/batchAccounts/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Batch/batchAccounts/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Batch/batchAccounts/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for the Batch service |
> | Action | Microsoft.Batch/batchAccounts/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for the Batch service |
> | Action | Microsoft.Batch/batchAccounts/read | Lists Batch accounts or gets the properties of a Batch account |
> | Action | Microsoft.Batch/batchAccounts/regeneratekeys/action | Regenerates access keys for a Batch account |
> | Action | Microsoft.Batch/batchAccounts/syncAutoStorageKeys/action | Synchronizes access keys for the auto storage account configured for a Batch account |
> | Action | Microsoft.Batch/batchAccounts/write | Creates a new Batch account or updates an existing Batch account |
> | Action | Microsoft.Batch/locations/checkNameAvailability/action | Checks that the account name is valid and not in use. |
> | Action | Microsoft.Batch/locations/quotas/read | Gets Batch quotas of the specified subscription at the specified Azure region |
> | Action | Microsoft.Batch/operations/read | Lists operations available on Microsoft.Batch resource provider |
> | Action | Microsoft.Batch/register/action | Registers the subscription for the Batch Resource Provider and enables the creation of Batch accounts |
> | Action | Microsoft.Batch/unregister/action | Unregisters the subscription for the Batch Resource Provider preventing the creation of Batch accounts |

## Microsoft.BatchAI

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.BatchAI/clusters/read | Lists Batch AI clusters or gets the properties of a Batch AI cluster |
> | Action | Microsoft.BatchAI/fileservers/read | Lists Batch AI fileservers or gets the properties of a Batch AI fileserver |
> | Action | Microsoft.BatchAI/locations/operationresults/read | Gets Batch AI async operation result at the specified Azure region |
> | Action | Microsoft.BatchAI/locations/operationstatuses/read | Gets Batch AI async operation status at the specified Azure region |
> | Action | Microsoft.BatchAI/locations/usages/read | Gets Batch AI usages of the specified subscription at the specified Azure region |
> | Action | Microsoft.BatchAI/register/action | Registers the subscription for the Batch AI Resource Provider and enables the creation of Batch AI resources |
> | Action | Microsoft.BatchAI/unregister/action | Unregisters the subscription for the Batch AI Resource Provider preventing the creation of Batch AI resources |
> | Action | Microsoft.BatchAI/workspaces/clusters/delete | Deletes a Batch AI cluster |
> | Action | Microsoft.BatchAI/workspaces/clusters/read | Lists Batch AI clusters or gets the properties of a Batch AI cluster |
> | Action | Microsoft.BatchAI/workspaces/clusters/remoteLoginInformation/action | Lists remote-login information for a Batch AI cluster |
> | Action | Microsoft.BatchAI/workspaces/clusters/write | Creates a new Batch AI cluster or updates an existing Batch AI cluster |
> | Action | Microsoft.BatchAI/workspaces/delete | Deletes a Batch AI workspace |
> | Action | Microsoft.BatchAI/workspaces/experiments/delete | Deletes a Batch AI experiment |
> | Action | Microsoft.BatchAI/workspaces/experiments/jobs/delete | Deletes a Batch AI job |
> | Action | Microsoft.BatchAI/workspaces/experiments/jobs/listoutputfiles/action | Lists output files for a Batch AI job |
> | Action | Microsoft.BatchAI/workspaces/experiments/jobs/read | Lists Batch AI jobs or gets the properties of a Batch AI job |
> | Action | Microsoft.BatchAI/workspaces/experiments/jobs/remoteLoginInformation/action | Lists remote-login information for a Batch AI job |
> | Action | Microsoft.BatchAI/workspaces/experiments/jobs/terminate/action | Terminates a Batch AI job |
> | Action | Microsoft.BatchAI/workspaces/experiments/jobs/write | Creates a new Batch AI job or updates an existing Batch AI job |
> | Action | Microsoft.BatchAI/workspaces/experiments/read | Lists Batch AI experiments or gets the properties of a Batch AI experiment |
> | Action | Microsoft.BatchAI/workspaces/experiments/write | Creates a new Batch AI experiment or updates an existing Batch AI experiment |
> | Action | Microsoft.BatchAI/workspaces/fileservers/delete | Deletes a Batch AI fileserver |
> | Action | Microsoft.BatchAI/workspaces/fileservers/read | Lists Batch AI fileservers or gets the properties of a Batch AI fileserver |
> | Action | Microsoft.BatchAI/workspaces/fileservers/write | Creates a new Batch AI fileserver or updates an existing Batch AI fileserver |
> | Action | Microsoft.BatchAI/workspaces/read | Lists Batch AI workspaces or gets the properties of a Batch AI workspace |
> | Action | Microsoft.BatchAI/workspaces/write | Creates a new Batch AI workspace or updates an existing Batch AI workspace |

## Microsoft.Billing

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Billing/billingPeriods/read | Lists available billing periods |
> | Action | Microsoft.Billing/invoices/read | Lists available invoices |

## Microsoft.BingMaps

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.BingMaps/mapApis/Delete | Delete Operation |
> | Action | Microsoft.BingMaps/mapApis/listSecrets/action | List the Secrets |
> | Action | Microsoft.BingMaps/mapApis/listSingleSignOnToken/action | Read Single Sign On Authorization Token For The Resource |
> | Action | Microsoft.BingMaps/mapApis/Read | Read Operation |
> | Action | Microsoft.BingMaps/mapApis/regenerateKey/action | Regenerates the Key |
> | Action | Microsoft.BingMaps/mapApis/Write | Write Operation |
> | Action | Microsoft.BingMaps/Operations/read | Description of the operation. |

## Microsoft.Blueprint

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Blueprint/blueprintAssignments/delete | Delete any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprintAssignments/read | Read any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprintAssignments/write | Create or Update any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprints/artifacts/delete | Delete any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprints/artifacts/read | Read any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprints/artifacts/write | Create or Update any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprints/delete | Delete any Blueprints |
> | Action | Microsoft.Blueprint/blueprints/read | Read any Blueprints |
> | Action | Microsoft.Blueprint/blueprints/versions/artifacts/read | Read any Blueprint Artifacts |
> | Action | Microsoft.Blueprint/blueprints/versions/delete | Delete any Blueprints |
> | Action | Microsoft.Blueprint/blueprints/versions/read | Read any Blueprints |
> | Action | Microsoft.Blueprint/blueprints/versions/write | Create or Update any Blueprints |
> | Action | Microsoft.Blueprint/blueprints/write | Create or Update any Blueprints |
> | Action | Microsoft.Blueprint/register/action | Registers the Blueprint Resource Provider |

## Microsoft.BotService

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.BotService/botServices/channels/delete | Delete a Bot Service |
> | Action | Microsoft.BotService/botServices/channels/read | Read a Bot Service |
> | Action | Microsoft.BotService/botServices/channels/write | Write a Bot Service |
> | Action | Microsoft.BotService/botServices/connections/delete | Delete a Bot Service |
> | Action | Microsoft.BotService/botServices/connections/read | Read a Bot Service |
> | Action | Microsoft.BotService/botServices/connections/write | Write a Bot Service |
> | Action | Microsoft.BotService/botServices/delete | Delete a Bot Service |
> | Action | Microsoft.BotService/botServices/read | Read a Bot Service |
> | Action | Microsoft.BotService/botServices/write | Write a Bot Service |
> | Action | Microsoft.BotService/locations/operationresults/read | Read the status of an asynchronous operation |
> | Action | Microsoft.BotService/Operations/read | Read the operations for all resource types |

## Microsoft.Cache

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Cache/checknameavailability/action | Checks if a name is available for use with a new Redis Cache |
> | Action | Microsoft.Cache/locations/operationresults/read | Gets the result of a long running operation for which the 'Location' header was previously returned to the client |
> | Action | Microsoft.Cache/operations/read | Lists the operations that 'Microsoft.Cache' provider supports. |
> | Action | Microsoft.Cache/redis/delete | Delete the entire Redis Cache |
> | Action | Microsoft.Cache/redis/export/action | Export Redis data to prefixed storage blobs in specified format |
> | Action | Microsoft.Cache/redis/firewallRules/delete | Delete IP firewall rules of a Redis Cache |
> | Action | Microsoft.Cache/redis/firewallRules/read | Get the IP firewall rules of a Redis Cache |
> | Action | Microsoft.Cache/redis/firewallRules/write | Edit the IP firewall rules of a Redis Cache |
> | Action | Microsoft.Cache/redis/forceReboot/action | Force reboot a cache instance, potentially with data loss. |
> | Action | Microsoft.Cache/redis/import/action | Import data of a specified format from multiple blobs into Redis |
> | Action | Microsoft.Cache/redis/linkedservers/delete | Delete Linked Server from a Redis Cache |
> | Action | Microsoft.Cache/redis/linkedservers/read | Get Linked Servers associated with a redis cache. |
> | Action | Microsoft.Cache/redis/linkedservers/write | Add Linked Server to a Redis Cache |
> | Action | Microsoft.Cache/redis/listKeys/action | View the value of Redis Cache access keys in the management portal |
> | Action | Microsoft.Cache/redis/listUpgradeNotifications/read | List the latest Upgrade Notifications for the cache tenant. |
> | Action | Microsoft.Cache/redis/metricDefinitions/read | Gets the available metrics for a Redis Cache |
> | Action | Microsoft.Cache/redis/patchSchedules/delete | Delete the patch schedule of a Redis Cache |
> | Action | Microsoft.Cache/redis/patchSchedules/read | Gets the patching schedule of a Redis Cache |
> | Action | Microsoft.Cache/redis/patchSchedules/write | Modify the patching schedule of a Redis Cache |
> | Action | Microsoft.Cache/redis/read | View the Redis Cache's settings and configuration in the management portal |
> | Action | Microsoft.Cache/redis/recommendations/read | Read Azure Redis Cache Recommendations |
> | Action | Microsoft.Cache/redis/regenerateKey/action | Change the value of Redis Cache access keys in the management portal |
> | Action | Microsoft.Cache/redis/start/action | Start a cache instance. |
> | Action | Microsoft.Cache/redis/start/action | Start a cache instance. |
> | Action | Microsoft.Cache/redis/stop/action | Stop a cache instance. |
> | Action | Microsoft.Cache/redis/write | Modify the Redis Cache's settings and configuration in the management portal |
> | Action | Microsoft.Cache/register/action | Registers the 'Microsoft.Cache' resource provider with a subscription |
> | Action | Microsoft.Cache/unregister/action | Unregisters the 'Microsoft.Cache' resource provider with a subscription |

## Microsoft.Capacity

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Capacity/register/action | Registers the Capacity resource provider and enables the creation of Capacity resources. |
> | Action | Microsoft.Capacity/reservationorders/action | Update any Reservation |
> | Action | Microsoft.Capacity/reservationorders/delete | Delete any Reservation |
> | Action | Microsoft.Capacity/reservationorders/read | Read All Reservations |
> | Action | Microsoft.Capacity/reservationorders/reservations/action | Update any Reservation |
> | Action | Microsoft.Capacity/reservationorders/reservations/delete | Delete any Reservation |
> | Action | Microsoft.Capacity/reservationorders/reservations/read | Read All Reservations |
> | Action | Microsoft.Capacity/reservationorders/reservations/revisions/read | Read All Reservations |
> | Action | Microsoft.Capacity/reservationorders/reservations/write | Create any Reservation |
> | Action | Microsoft.Capacity/reservationorders/write | Create any Reservation |

## Microsoft.Cdn

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Cdn/CheckNameAvailability/action |  |
> | Action | Microsoft.Cdn/CheckResourceUsage/action |  |
> | Action | Microsoft.Cdn/edgenodes/delete |  |
> | Action | Microsoft.Cdn/edgenodes/read |  |
> | Action | Microsoft.Cdn/edgenodes/write |  |
> | Action | Microsoft.Cdn/operationresults/delete |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/CheckResourceUsage/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/delete |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/CheckResourceUsage/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/customdomainresults/delete |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/customdomainresults/DisableCustomHttps/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/customdomainresults/EnableCustomHttps/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/customdomainresults/read |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/customdomainresults/write |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/delete |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/Load/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/originresults/delete |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/originresults/read |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/originresults/write |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/Purge/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/read |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/Start/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/Stop/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/ValidateCustomDomain/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/endpointresults/write |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/GenerateSsoUri/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/GetSupportedOptimizationTypes/action |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/read |  |
> | Action | Microsoft.Cdn/operationresults/profileresults/write |  |
> | Action | Microsoft.Cdn/operationresults/read |  |
> | Action | Microsoft.Cdn/operationresults/write |  |
> | Action | Microsoft.Cdn/operations/read |  |
> | Action | Microsoft.Cdn/profiles/CheckResourceUsage/action |  |
> | Action | Microsoft.Cdn/profiles/delete |  |
> | Action | Microsoft.Cdn/profiles/endpoints/CheckResourceUsage/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/customdomains/delete |  |
> | Action | Microsoft.Cdn/profiles/endpoints/customdomains/DisableCustomHttps/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/customdomains/EnableCustomHttps/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/customdomains/read |  |
> | Action | Microsoft.Cdn/profiles/endpoints/customdomains/write |  |
> | Action | Microsoft.Cdn/profiles/endpoints/delete |  |
> | Action | Microsoft.Cdn/profiles/endpoints/Load/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/origins/delete |  |
> | Action | Microsoft.Cdn/profiles/endpoints/origins/read |  |
> | Action | Microsoft.Cdn/profiles/endpoints/origins/write |  |
> | Action | Microsoft.Cdn/profiles/endpoints/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic settings for the resource |
> | Action | Microsoft.Cdn/profiles/endpoints/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic settings for the resource |
> | Action | Microsoft.Cdn/profiles/endpoints/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Microsoft.Cdn |
> | Action | Microsoft.Cdn/profiles/endpoints/Purge/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/read |  |
> | Action | Microsoft.Cdn/profiles/endpoints/Start/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/Stop/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/ValidateCustomDomain/action |  |
> | Action | Microsoft.Cdn/profiles/endpoints/write |  |
> | Action | Microsoft.Cdn/profiles/GenerateSsoUri/action |  |
> | Action | Microsoft.Cdn/profiles/GetSupportedOptimizationTypes/action |  |
> | Action | Microsoft.Cdn/profiles/read |  |
> | Action | Microsoft.Cdn/profiles/write |  |
> | Action | Microsoft.Cdn/register/action | Registers the subscription for the CDN resource provider and enables the creation of CDN profiles. |
> | Action | Microsoft.Cdn/ValidateProbe/action |  |

## Microsoft.CertificateRegistration

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.CertificateRegistration/certificateOrders/certificates/Delete | Delete an existing certificate |
> | Action | Microsoft.CertificateRegistration/certificateOrders/certificates/Read | Get the list of certificates |
> | Action | Microsoft.CertificateRegistration/certificateOrders/certificates/Write | Add a new certificate or update an existing one |
> | Action | Microsoft.CertificateRegistration/certificateOrders/Delete | Delete an existing AppServiceCertificate |
> | Action | Microsoft.CertificateRegistration/certificateOrders/Read | Get the list of CertificateOrders |
> | Action | Microsoft.CertificateRegistration/certificateOrders/reissue/Action | Reissue an existing certificateorder |
> | Action | Microsoft.CertificateRegistration/certificateOrders/renew/Action | Renew an existing certificateorder |
> | Action | Microsoft.CertificateRegistration/certificateOrders/resendEmail/Action | Resend certificate email |
> | Action | Microsoft.CertificateRegistration/certificateOrders/resendRequestEmails/Action | Resend request emails to another email address |
> | Action | Microsoft.CertificateRegistration/certificateOrders/resendRequestEmails/Action | Retrieve site seal for an issued App Service Certificate |
> | Action | Microsoft.CertificateRegistration/certificateOrders/retrieveCertificateActions/Action | Retrieve the list of certificate actions |
> | Action | Microsoft.CertificateRegistration/certificateOrders/retrieveEmailHistory/Action | Retrieve certificate email history |
> | Action | Microsoft.CertificateRegistration/certificateOrders/verifyDomainOwnership/Action | Verify domain ownership |
> | Action | Microsoft.CertificateRegistration/certificateOrders/Write | Add a new certificateOrder or update an existing one |
> | Action | Microsoft.CertificateRegistration/operations/Read | List all operations from app service certificate registration |
> | Action | Microsoft.CertificateRegistration/provisionGlobalAppServicePrincipalInUserTenant/Action | Provision service principal for service app principal |
> | Action | Microsoft.CertificateRegistration/register/action | Register the Microsoft Certificates resource provider for the subscription |
> | Action | Microsoft.CertificateRegistration/validateCertificateRegistrationInformation/Action | Validate certificate purchase object without submitting it |

## Microsoft.ClassicCompute

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ClassicCompute/capabilities/read | Shows the capabilities |
> | Action | Microsoft.ClassicCompute/checkDomainNameAvailability/action | Checks the availability of a given domain name. |
> | Action | Microsoft.ClassicCompute/checkDomainNameAvailability/read | Gets the availability of a given domain name. |
> | Action | Microsoft.ClassicCompute/domainNames/active/write | Sets the active domain name. |
> | Action | Microsoft.ClassicCompute/domainNames/availabilitySets/read | Show the availability set for the resource. |
> | Action | Microsoft.ClassicCompute/domainNames/capabilities/read | Shows the domain name capabilities |
> | Action | Microsoft.ClassicCompute/domainNames/delete | Remove the domain names for resources. |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/read | Shows the deployment slots. |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/roles/read | Get role on deployment slot of domain name |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/roles/roleinstances/read | Get role instance for role on deployment slot of domain name |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/state/read | Get the deployment slot state. |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/state/write | Add the deployment slot state. |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/upgradedomain/read | Get upgrade domain for deployment slot on domain name |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/upgradedomain/write | Update upgrade domain for deployment slot on domain name |
> | Action | Microsoft.ClassicCompute/domainNames/deploymentslots/write | Creates or update the deployment. |
> | Action | Microsoft.ClassicCompute/domainNames/extensions/delete | Remove the domain name extensions. |
> | Action | Microsoft.ClassicCompute/domainNames/extensions/operationStatuses/read | Reads the operation status for the domain names extensions. |
> | Action | Microsoft.ClassicCompute/domainNames/extensions/read | Returns the domain name extensions. |
> | Action | Microsoft.ClassicCompute/domainNames/extensions/write | Add the domain name extensions. |
> | Action | Microsoft.ClassicCompute/domainNames/internalLoadBalancers/delete | Remove a new internal load balance. |
> | Action | Microsoft.ClassicCompute/domainNames/internalLoadBalancers/operationStatuses/read | Reads the operation status for the domain names internal load balancers. |
> | Action | Microsoft.ClassicCompute/domainNames/internalLoadBalancers/read | Gets the internal load balancers. |
> | Action | Microsoft.ClassicCompute/domainNames/internalLoadBalancers/write | Creates a new internal load balance. |
> | Action | Microsoft.ClassicCompute/domainNames/loadBalancedEndpointSets/operationStatuses/read | Reads the operation status for the domain names load balanced endpoint sets. |
> | Action | Microsoft.ClassicCompute/domainNames/loadBalancedEndpointSets/read | Get the load balanced endpoint sets. |
> | Action | Microsoft.ClassicCompute/domainNames/loadBalancedEndpointSets/write | Add the load balanced endpoint set. |
> | Action | Microsoft.ClassicCompute/domainNames/operationstatuses/read | Get operation status of the domain name. |
> | Action | Microsoft.ClassicCompute/domainNames/operationStatuses/read | Reads the operation status for the domain names extensions. |
> | Action | Microsoft.ClassicCompute/domainNames/read | Return the domain names for resources. |
> | Action | Microsoft.ClassicCompute/domainNames/serviceCertificates/delete | Delete the service certificates used. |
> | Action | Microsoft.ClassicCompute/domainNames/serviceCertificates/operationStatuses/read | Reads the operation status for the domain names service certificates. |
> | Action | Microsoft.ClassicCompute/domainNames/serviceCertificates/read | Returns the service certificates used. |
> | Action | Microsoft.ClassicCompute/domainNames/serviceCertificates/write | Add or modify the service certificates used. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/abortMigration/action | Aborts migration of a deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/commitMigration/action | Commits migration of a deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/delete | Deletes a given deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/operationStatuses/read | Reads the operation status for the domain names slots. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/prepareMigration/action | Prepares migration of a deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/read | Shows the deployment slots. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/extensionReferences/delete | Remove the extension reference for the deployment slot role. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/extensionReferences/operationStatuses/read | Reads the operation status for the domain names slots roles extension references. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/extensionReferences/read | Returns the extension reference for the deployment slot role. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/extensionReferences/write | Add or modify the extension reference for the deployment slot role. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/metricdefinitions/read | Get the role metric definition for the domain name. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/metrics/read | Get role metric for the domain name. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/operationstatuses/read | Get the operation status for the domain names slot role. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostics settings. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/providers/Microsoft.Insights/diagnosticSettings/write | Add or modify diagnostics settings. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/providers/Microsoft.Insights/metricDefinitions/read | Gets the metrics definitions. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/read | Get the role for the deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/roleInstances/downloadremotedesktopconnectionfile/action | Downloads remote desktop connection file for the role instance on the domain name slot role. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/roleInstances/operationStatuses/read | Gets the operation status for the role instance on domain names slot role. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/roleInstances/read | Get the role instance. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/roleInstances/rebuild/action | Rebuilds the role instance. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/roleInstances/reimage/action | Reimages the role instance. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/roleInstances/restart/action | Restarts role instances. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/skus/read | Get role sku for the deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/roles/write | Add role for the deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/start/action | Starts a deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/state/start/write | Changes the deployment slot state to stopped. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/state/stop/write | Changes the deployment slot state to started. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/stop/action | Suspends the deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/upgradeDomain/write | Walk upgrade the domain. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/validateMigration/action | Validates migration of a deployment slot. |
> | Action | Microsoft.ClassicCompute/domainNames/slots/write | Creates or update the deployment. |
> | Action | Microsoft.ClassicCompute/domainNames/swap/action | Swaps the staging slot to the production slot. |
> | Action | Microsoft.ClassicCompute/domainNames/write | Add or modify the domain names for resources. |
> | Action | Microsoft.ClassicCompute/moveSubscriptionResources/action | Move all classic resources to a different subscription. |
> | Action | Microsoft.ClassicCompute/operatingSystemFamilies/read | Lists the guest operating system families available in Microsoft Azure, and also lists the operating system versions available for each family. |
> | Action | Microsoft.ClassicCompute/operatingSystems/read | Lists the versions of the guest operating system that are currently available in Microsoft Azure. |
> | Action | Microsoft.ClassicCompute/operations/read | Gets the list of operations. |
> | Action | Microsoft.ClassicCompute/operationStatuses/read | Reads the operation status for the resource. |
> | Action | Microsoft.ClassicCompute/quotas/read | Get the quota for the subscription. |
> | Action | Microsoft.ClassicCompute/register/action | Register to Classic Compute |
> | Action | Microsoft.ClassicCompute/resourceTypes/skus/read | Gets the Sku list for supported resource types. |
> | Action | Microsoft.ClassicCompute/validateSubscriptionMoveAvailability/action | Validate the subscription's availability for classic move operation. |
> | Action | Microsoft.ClassicCompute/virtualMachines/associatedNetworkSecurityGroups/delete | Deletes the network security group associated with the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/associatedNetworkSecurityGroups/operationStatuses/read | Reads the operation status for the virtual machines associated network security groups. |
> | Action | Microsoft.ClassicCompute/virtualMachines/associatedNetworkSecurityGroups/read | Gets the network security group associated with the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/associatedNetworkSecurityGroups/write | Adds a network security group associated with the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/asyncOperations/read | Gets the possible async operations |
> | Action | Microsoft.ClassicCompute/virtualMachines/attachDisk/action | Attaches a data disk to a virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/capture/action | Capture a virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/delete | Removes virtual machines. |
> | Action | Microsoft.ClassicCompute/virtualMachines/detachDisk/action | Detaches a data disk from virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/diagnosticsettings/read | Get virtual machine diagnostics settings. |
> | Action | Microsoft.ClassicCompute/virtualMachines/disks/read | Retrives list of data disks |
> | Action | Microsoft.ClassicCompute/virtualMachines/downloadRemoteDesktopConnectionFile/action | Downloads the RDP file for virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/extensions/operationStatuses/read | Reads the operation status for the virtual machines extensions. |
> | Action | Microsoft.ClassicCompute/virtualMachines/extensions/read | Gets the virtual machine extension. |
> | Action | Microsoft.ClassicCompute/virtualMachines/extensions/write | Puts the virtual machine extension. |
> | Action | Microsoft.ClassicCompute/virtualMachines/metricdefinitions/read | Get the virtual machine metric definition. |
> | Action | Microsoft.ClassicCompute/virtualMachines/metrics/read | Gets the metrics. |
> | Action | Microsoft.ClassicCompute/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/delete | Deletes the network security group associated with the network interface. |
> | Action | Microsoft.ClassicCompute/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/operationStatuses/read | Reads the operation status for the virtual machines associated network security groups. |
> | Action | Microsoft.ClassicCompute/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/read | Gets the network security group associated with the network interface. |
> | Action | Microsoft.ClassicCompute/virtualMachines/networkInterfaces/associatedNetworkSecurityGroups/write | Adds a network security group associated with the network interface. |
> | Action | Microsoft.ClassicCompute/virtualMachines/operationStatuses/read | Reads the operation status for the virtual machines. |
> | Action | Microsoft.ClassicCompute/virtualMachines/performMaintenance/action | Performs maintenance on the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostics settings. |
> | Action | Microsoft.ClassicCompute/virtualMachines/providers/Microsoft.Insights/diagnosticSettings/write | Add or modify diagnostics settings. |
> | Action | Microsoft.ClassicCompute/virtualMachines/providers/Microsoft.Insights/metricDefinitions/read | Gets the metrics definitions. |
> | Action | Microsoft.ClassicCompute/virtualMachines/read | Retrieves list of virtual machines. |
> | Action | Microsoft.ClassicCompute/virtualMachines/redeploy/action | Redeploys the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/restart/action | Restarts virtual machines. |
> | Action | Microsoft.ClassicCompute/virtualMachines/shutdown/action | Shutdown the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/start/action | Start the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/stop/action | Stops the virtual machine. |
> | Action | Microsoft.ClassicCompute/virtualMachines/write | Add or modify virtual machines. |

## Microsoft.ClassicNetwork

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/operationstatuses/read | Get an express route cross connection operation status. |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/peerings/delete | Delete express route cross connection peering. |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/peerings/operationstatuses/read | Get an express route cross connection peering operation status. |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/peerings/read | Get express route cross connection peering. |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/peerings/write | Add express route cross connection peering. |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/read | Get express route cross connections. |
> | Action | Microsoft.ClassicNetwork/expressroutecrossconnections/write | Add express route cross connections. |
> | Action | Microsoft.ClassicNetwork/gatewaySupportedDevices/read | Retrieves the list of supported devices. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/delete | Deletes the network security group. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/operationStatuses/read | Reads the operation status for the network security group. |
> | Action | Microsoft.ClassicNetwork/networksecuritygroups/providers/Microsoft.Insights/diagnosticSettings/read | Gets the Network Security Groups Diagnostic Settings |
> | Action | Microsoft.ClassicNetwork/networksecuritygroups/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the Network Security Groups diagnostic settings, this operation is supplemented by insghts resource provider. | 
> | Action | Microsoft.ClassicNetwork/networksecuritygroups/providers/Microsoft.Insights/logDefinitions/read | Gets the events for network security group |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/read | Gets the network security group. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/securityRules/delete | Deletes the security rule. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/securityRules/operationStatuses/read | Reads the operation status for the network security group security rules. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/securityRules/read | Gets the security rule. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/securityRules/write | Adds or update a security rule. |
> | Action | Microsoft.ClassicNetwork/networkSecurityGroups/write | Adds a new network security group. |
> | Action | Microsoft.ClassicNetwork/operations/read | Get classic network operations. |
> | Action | Microsoft.ClassicNetwork/quotas/read | Get the quota for the subscription. |
> | Action | Microsoft.ClassicNetwork/register/action | Register to Classic Network |
> | Action | Microsoft.ClassicNetwork/reservedIps/delete | Delete a reserved Ip. |
> | Action | Microsoft.ClassicNetwork/reservedIps/join/action | Join a reserved Ip |
> | Action | Microsoft.ClassicNetwork/reservedIps/link/action | Link a reserved Ip |
> | Action | Microsoft.ClassicNetwork/reservedIps/operationStatuses/read | Reads the operation status for the reserved ips. |
> | Action | Microsoft.ClassicNetwork/reservedIps/read | Gets the reserved Ips |
> | Action | Microsoft.ClassicNetwork/reservedIps/write | Add a new reserved Ip |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/abortMigration/action | Aborts the migration of a Virtual Network |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/capabilities/read | Shows the capabilities |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/checkIPAddressAvailability/action | Checks the availability of a given IP address in a virtual network. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/commitMigration/action | Commits the migration of a Virtual Network |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/delete | Deletes the virtual network. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRevokedCertificates/delete | Unrevokes a client certificate. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRevokedCertificates/read | Read the revoked client certificates. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRevokedCertificates/write | Revokes a client certificate. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRootCertificates/delete | Deletes the virtual network gateway client certificate. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRootCertificates/download/action | Downloads certificate by thumbprint. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRootCertificates/listPackage/action | Lists the virtual network gateway certificate package. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRootCertificates/read | Find the client root certificates. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/clientRootCertificates/write | Uploads a new client root certificate. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/connections/connect/action | Connects a site to site gateway connection. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/connections/disconnect/action | Disconnects a site to site gateway connection. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/connections/read | Retrieves the list of connections. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/connections/test/action | Tests a site to site gateway connection. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/delete | Deletes the virtual network gateway. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/downloadDeviceConfigurationScript/action | Downloads the device configuration script. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/downloadDiagnostics/action | Downloads the gateway diagnostics. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/listCircuitServiceKey/action | Retrieves the circuit service key. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/listPackage/action | Lists the virtual network gateway package. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/operationStatuses/read | Reads the operation status for the virtual networks gateways. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/packages/read | Gets the virtual network gateway package. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/read | Gets the virtual network gateways. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/startDiagnostics/action | Starts diagnositic for the virtual network gateway. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/stopDiagnostics/action | Stops the diagnositic for the virtual network gateway. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/gateways/write | Adds a virtual network gateway. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/join/action | Joins the virtual network. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/operationStatuses/read | Reads the operation status for the virtual networks. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/peer/action | Peers a virtual network with another virtual network. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/prepareMigration/action | Prepares the migration of a Virtual Network |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/read | Get the virtual network. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/remoteVirtualNetworkPeeringProxies/delete | Deletes the remote virtual network peering proxy. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/remoteVirtualNetworkPeeringProxies/read | Gets the remote virtual network peering proxy. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/remoteVirtualNetworkPeeringProxies/write | Adds or updates the remote virtual network peering proxy. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/subnets/associatedNetworkSecurityGroups/delete | Deletes the network security group associated with the subnet. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/subnets/associatedNetworkSecurityGroups/operationStatuses/read | Reads the operation status for the virtual network subnet associated network security group. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/subnets/associatedNetworkSecurityGroups/read | Gets the network security group associated with the subnet. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/subnets/associatedNetworkSecurityGroups/write | Adds a network security group associated with the subnet. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/validateMigration/action | Validates the migration of a Virtual Network |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/virtualNetworkPeerings/read | Gets the virtual network peering. |
> | Action | Microsoft.ClassicNetwork/virtualNetworks/write | Add a new virtual network. |

## Microsoft.ClassicStorage

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ClassicStorage/capabilities/read | Shows the capabilities |
> | Action | Microsoft.ClassicStorage/checkStorageAccountAvailability/action | Checks for the availability of a storage account. |
> | Action | Microsoft.ClassicStorage/checkStorageAccountAvailability/read | Get the availability of a storage account. |
> | Action | Microsoft.ClassicStorage/disks/read | Returns the storage account disk. |
> | Action | Microsoft.ClassicStorage/images/operationstatuses/read | Gets Image Operation Status. |
> | Action | Microsoft.ClassicStorage/images/read | Returns the image. |
> | Action | Microsoft.ClassicStorage/operations/read | Gets classic storage operations |
> | Action | Microsoft.ClassicStorage/osImages/read | Returns the operating system image. |
> | Action | Microsoft.ClassicStorage/osPlatformImages/read | Gets the operating system platform image. |
> | Action | Microsoft.ClassicStorage/publicImages/read | Gets the public virtual machine image. |
> | Action | Microsoft.ClassicStorage/quotas/read | Get the quota for the subscription. |
> | Action | Microsoft.ClassicStorage/register/action | Register to Classic Storage |
> | Action | Microsoft.ClassicStorage/storageAccounts/abortMigration/action | Aborts migration of a storage account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/commitMigration/action | Commits migration of a storage account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/delete | Delete the storage account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/disks/delete | Deletes a given storage account  disk. |
> | Action | Microsoft.ClassicStorage/storageAccounts/disks/operationStatuses/read | Reads the operation status for the resource. |
> | Action | Microsoft.ClassicStorage/storageAccounts/disks/read | Returns the storage account disk. |
> | Action | Microsoft.ClassicStorage/storageAccounts/disks/write | Adds a storage account disk. |
> | Action | Microsoft.ClassicStorage/storageAccounts/images/delete | Deletes a given storage account image. (Deprecated. Use 'Microsoft.ClassicStorage/storageAccounts/vmImages') |
> | Action | Microsoft.ClassicStorage/storageAccounts/images/operationstatuses/read | Returns the storage account image operation status. |
> | Action | Microsoft.ClassicStorage/storageAccounts/images/read | Returns the storage account image. (Deprecated. Use 'Microsoft.ClassicStorage/storageAccounts/vmImages') |
> | Action | Microsoft.ClassicStorage/storageAccounts/listKeys/action | Lists the access keys for the storage accounts. |
> | Action | Microsoft.ClassicStorage/storageAccounts/operationStatuses/read | Reads the operation status for the resource. |
> | Action | Microsoft.ClassicStorage/storageAccounts/osImages/delete | Deletes a given storage account operating system image. |
> | Action | Microsoft.ClassicStorage/storageAccounts/osImages/read | Returns the storage account operating system image. |
> | Action | Microsoft.ClassicStorage/storageAccounts/osImages/write | Adds a given storage account operating system image. |
> | Action | Microsoft.ClassicStorage/storageAccounts/prepareMigration/action | Prepares migration of a storage account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/read | Return the storage account with the given account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/regenerateKey/action | Regenerates the existing access keys for the storage account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/services/diagnosticSettings/read | Get the diagnostics settings. |
> | Action | Microsoft.ClassicStorage/storageAccounts/services/diagnosticSettings/write | Add or modify diagnostics settings. |
> | Action | Microsoft.ClassicStorage/storageAccounts/services/metricDefinitions/read | Gets the metrics definitions. |
> | Action | Microsoft.ClassicStorage/storageAccounts/services/metrics/read | Gets the metrics. |
> | Action | Microsoft.ClassicStorage/storageAccounts/services/read | Get the available services. |
> | Action | Microsoft.ClassicStorage/storageAccounts/validateMigration/action | Validates migration of a storage account. |
> | Action | Microsoft.ClassicStorage/storageAccounts/vmImages/delete | Deletes a given virtual machine image. |
> | Action | Microsoft.ClassicStorage/storageAccounts/vmImages/operationstatuses/read | Gets a given virtual machine image operation status. |
> | Action | Microsoft.ClassicStorage/storageAccounts/vmImages/read | Returns the virtual machine image. |
> | Action | Microsoft.ClassicStorage/storageAccounts/vmImages/write | Adds a given virtual machine image. |
> | Action | Microsoft.ClassicStorage/storageAccounts/write | Adds a new storage account. |
> | Action | Microsoft.ClassicStorage/vmImages/read | Lists virtual machine images. |

## Microsoft.CognitiveServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.CognitiveServices/accounts/delete | Deletes API accounts |
> | Action | Microsoft.CognitiveServices/accounts/listKeys/action | List Keys |
> | Action | Microsoft.CognitiveServices/accounts/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.CognitiveServices/accounts/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.CognitiveServices/accounts/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Cognitive Services account |
> | Action | Microsoft.CognitiveServices/accounts/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Cognitive Services. |
> | Action | Microsoft.CognitiveServices/accounts/read | Reads API accounts. |
> | Action | Microsoft.CognitiveServices/accounts/regenerateKey/action | Regenerate Key |
> | Action | Microsoft.CognitiveServices/accounts/skus/read | Reads available SKUs for an existing resource. |
> | Action | Microsoft.CognitiveServices/accounts/usages/read | Get the quota usage for an existing resource. |
> | Action | Microsoft.CognitiveServices/accounts/write | Writes API Accounts. |
> | Action | Microsoft.CognitiveServices/locations/checkSkuAvailability/action | Reads available SKUs for an subscription. |
> | Action | Microsoft.CognitiveServices/Operations/read | List all available operations |
> | Action | Microsoft.CognitiveServices/register/action | Registers Subscription for Cognitive Services |
> | Action | Microsoft.CognitiveServices/skus/read | Reads available SKUs for Cognitive Services. |

## Microsoft.Commerce

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Commerce/RateCard/read | Returns offer data, resource/meter metadata and rates for the given subscription. |
> | Action | Microsoft.Commerce/UsageAggregates/read | Retrieves Microsoft Azure’s consumption  by a subscription. The result contains aggregates usage data, subscription and resource related information, on a particular time range. |

## Microsoft.Compute

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Compute/availabilitySets/delete | Deletes the availability set |
> | Action | Microsoft.Compute/availabilitySets/read | Get the properties of an availability set |
> | Action | Microsoft.Compute/availabilitySets/vmSizes/read | List available sizes for creating or updating a virtual machine in the availability set |
> | Action | Microsoft.Compute/availabilitySets/write | Creates a new availability set or updates an existing one |
> | Action | Microsoft.Compute/disks/beginGetAccess/action | Get the SAS URI of the Disk for blob access |
> | Action | Microsoft.Compute/disks/delete | Deletes the Disk |
> | Action | Microsoft.Compute/disks/endGetAccess/action | Revoke the SAS URI of the Disk |
> | Action | Microsoft.Compute/disks/read | Get the properties of a Disk |
> | Action | Microsoft.Compute/disks/write | Creates a new Disk or updates an existing one |
> | Action | Microsoft.Compute/galleries/delete | Deletes the Gallery |
> | Action | Microsoft.Compute/galleries/images/delete | Deletes the Gallery Image |
> | Action | Microsoft.Compute/galleries/images/read | Gets the properties of Gallery Image |
> | Action | Microsoft.Compute/galleries/images/versions/delete | Deletes the Gallery Image Version |
> | Action | Microsoft.Compute/galleries/images/versions/read | Gets the properties of Gallery Image Version |
> | Action | Microsoft.Compute/galleries/images/versions/write | Creates a new Gallery Image Version or updates an existing one |
> | Action | Microsoft.Compute/galleries/images/write | Creates a new Gallery Image or updates an existing one |
> | Action | Microsoft.Compute/galleries/read | Gets the properties of Gallery |
> | Action | Microsoft.Compute/galleries/write | Creates a new Gallery or updates an existing one |
> | Action | Microsoft.Compute/images/delete | Deletes the image |
> | Action | Microsoft.Compute/images/read | Get the properties of the Image |
> | Action | Microsoft.Compute/images/write | Creates a new Image or updates an existing one |
> | Action | Microsoft.Compute/locations/capsOperations/read | Gets the status of an asynchronous Caps operation |
> | Action | Microsoft.Compute/locations/diskOperations/read | Gets the status of an asynchronous Disk operation |
> | Action | Microsoft.Compute/locations/logAnalytics/getRequestRateByInterval/action | Create logs to show total requests by time interval to aid throttling diagnostics. |
> | Action | Microsoft.Compute/locations/logAnalytics/getThrottledRequests/action | Create logs to show aggregates of throttled requests grouped by ResourceName, OperationName, or the applied Throttle Policy. |
> | Action | Microsoft.Compute/locations/operations/read | Gets the status of an asynchronous operation |
> | Action | Microsoft.Compute/locations/publishers/artifacttypes/offers/read | Get the properties of a Platform Image Offer |
> | Action | Microsoft.Compute/locations/publishers/artifacttypes/offers/skus/read | Get the properties of a Platform Image Sku |
> | Action | Microsoft.Compute/locations/publishers/artifacttypes/offers/skus/versions/read | Get the properties of a Platform Image Version |
> | Action | Microsoft.Compute/locations/publishers/artifacttypes/types/read | Get the properties of a VMExtension Type |
> | Action | Microsoft.Compute/locations/publishers/artifacttypes/types/versions/read | Get the properties of a VMExtension Version |
> | Action | Microsoft.Compute/locations/publishers/read | Get the properties of a Publisher |
> | Action | Microsoft.Compute/locations/runCommands/read | Lists available run commands in location |
> | Action | Microsoft.Compute/locations/usages/read | Gets service limits and current usage quantities for the subscription's compute resources in a location |
> | Action | Microsoft.Compute/locations/vmSizes/read | Lists available virtual machine sizes in a location |
> | Action | Microsoft.Compute/operations/read | Lists operations available on Microsoft.Compute resource provider |
> | Action | Microsoft.Compute/register/action | Registers Subscription with Microsoft.Compute resource provider |
> | Action | Microsoft.Compute/restorePointCollections/delete | Deletes the restore point collection and contained restore points |
> | Action | Microsoft.Compute/restorePointCollections/read | Get the properties of a restore point collection |
> | Action | Microsoft.Compute/restorePointCollections/restorePoints/delete | Deletes the restore point |
> | Action | Microsoft.Compute/restorePointCollections/restorePoints/read | Get the properties of a restore point |
> | Action | Microsoft.Compute/restorePointCollections/restorePoints/retrieveSasUris/action | Get the properties of a restore point along with blob SAS URIs |
> | Action | Microsoft.Compute/restorePointCollections/restorePoints/write | Creates a new restore point |
> | Action | Microsoft.Compute/restorePointCollections/write | Creates a new restore point collection or updates an existing one |
> | Action | Microsoft.Compute/sharedVMImages/delete | Deletes the SharedVMImage |
> | Action | Microsoft.Compute/sharedVMImages/read | Get the properties of a SharedVMImage |
> | Action | Microsoft.Compute/sharedVMImages/versions/delete | Delete a SharedVMImageVersion |
> | Action | Microsoft.Compute/sharedVMImages/versions/read | Get the properties of a SharedVMImageVersion |
> | Action | Microsoft.Compute/sharedVMImages/versions/replicate/action | Replicate a SharedVMImageVersion to target regions |
> | Action | Microsoft.Compute/sharedVMImages/versions/write | Create a new SharedVMImageVersion or update an existing one |
> | Action | Microsoft.Compute/sharedVMImages/write | Creates a new SharedVMImage or updates an existing one |
> | Action | Microsoft.Compute/skus/read | Gets the list of Microsoft.Compute SKUs available for your Subscription |
> | Action | Microsoft.Compute/snapshots/beginGetAccess/action | Get the SAS URI of the Snapshot for blob access |
> | Action | Microsoft.Compute/snapshots/delete | Delete a Snapshot |
> | Action | Microsoft.Compute/snapshots/endGetAccess/action | Revoke the SAS URI of the Snapshot |
> | Action | Microsoft.Compute/snapshots/read | Get the properties of a Snapshot |
> | Action | Microsoft.Compute/snapshots/write | Create a new Snapshot or update an existing one |
> | Action | Microsoft.Compute/virtualMachines/capture/action | Captures the virtual machine by copying virtual hard disks and generates a template that can be used to create similar virtual machines |
> | Action | Microsoft.Compute/virtualMachines/convertToManagedDisks/action | Converts the blob based disks of the virtual machine to managed disks |
> | Action | Microsoft.Compute/virtualMachines/deallocate/action | Powers off the virtual machine and releases the compute resources |
> | Action | Microsoft.Compute/virtualMachines/delete | Deletes the virtual machine |
> | Action | Microsoft.Compute/virtualMachines/extensions/delete | Deletes the virtual machine extension |
> | Action | Microsoft.Compute/virtualMachines/extensions/read | Get the properties of a virtual machine extension |
> | Action | Microsoft.Compute/virtualMachines/extensions/write | Creates a new virtual machine extension or updates an existing one |
> | Action | Microsoft.Compute/virtualMachines/generalize/action | Sets the virtual machine state to Generalized and prepares the virtual machine for capture |
> | Action | Microsoft.Compute/virtualMachines/instanceView/read | Gets the detailed runtime status of the virtual machine and its resources |
> | DataAction | Microsoft.Compute/virtualMachines/login/action | Log in to a virtual machine as a regular user |
> | DataAction | Microsoft.Compute/virtualMachines/loginAsAdmin/action | Log in to a virtual machine with Windows administrator or Linux root user privileges |
> | Action | Microsoft.Compute/virtualMachines/performMaintenance/action | Performs Maintenance Operation on the VM. |
> | Action | Microsoft.Compute/virtualMachines/powerOff/action | Powers off the virtual machine. Note that the virtual machine will continue to be billed. |
> | Action | Microsoft.Compute/virtualMachines/providers/Microsoft.Insights/metricDefinitions/read | Reads Virtual Machine Metric Definitions |
> | Action | Microsoft.Compute/virtualMachines/read | Get the properties of a virtual machine |
> | Action | Microsoft.Compute/virtualMachines/redeploy/action | Redeploys virtual machine |
> | Action | Microsoft.Compute/virtualMachines/reimage/action | Reimages virtual machine which is using differencing disk. |
> | Action | Microsoft.Compute/virtualMachines/restart/action | Restarts the virtual machine |
> | Action | Microsoft.Compute/virtualMachines/runCommand/action | Executes a predefined script on the virtual machine |
> | Action | Microsoft.Compute/virtualMachines/start/action | Starts the virtual machine |
> | Action | Microsoft.Compute/virtualMachines/vmSizes/read | Lists available sizes the virtual machine can be updated to |
> | Action | Microsoft.Compute/virtualMachines/write | Creates a new virtual machine or updates an existing virtual machine |
> | Action | Microsoft.Compute/virtualMachineScaleSets/deallocate/action | Powers off and releases the compute resources for the instances of the Virtual Machine Scale Set  |
> | Action | Microsoft.Compute/virtualMachineScaleSets/delete | Deletes the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/delete/action | Deletes the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/extensions/delete | Deletes the Virtual Machine Scale Set Extension |
> | Action | Microsoft.Compute/virtualMachineScaleSets/extensions/read | Gets the properties of a Virtual Machine Scale Set Extension |
> | Action | Microsoft.Compute/virtualMachineScaleSets/extensions/write | Creates a new Virtual Machine Scale Set Extension or updates an existing one |
> | Action | Microsoft.Compute/virtualMachineScaleSets/forceRecoveryServiceFabricPlatformUpdateDomainWalk/action | Manually walk the platform update domains of a service fabric Virtual Machine Scale Set to finish a pending update that is stuck |
> | Action | Microsoft.Compute/virtualMachineScaleSets/instanceView/read | Gets the instance view of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/manualUpgrade/action | Manually updates instances to latest model of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/networkInterfaces/read | Get properties of all network interfaces of a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/osRollingUpgrade/action | Starts a rolling upgrade to move all Virtual Machine Scale Set instances to the latest available Platform Image OS version. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/osUpgradeHistory/read | Gets the history of OS upgrades for a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/performMaintenance/action | Performs planned maintenance on the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/powerOff/action | Powers off the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the Virtual Machine Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the Virtual Machine Scale set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Virtual Machine Scale Sets. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/providers/Microsoft.Insights/metricDefinitions/read | Reads Virtual Machine Scalet Set Metric Definitions |
> | Action | Microsoft.Compute/virtualMachineScaleSets/publicIPAddresses/read | Get properties of all public IP addresses of a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/read | Get the properties of a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/redeploy/action | Redeploy the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/reimage/action | Reimages the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/reimageAll/action | Reimages all disks (OS Disk and Data Disks) for the instances of a Virtual Machine Scale Set  |
> | Action | Microsoft.Compute/virtualMachineScaleSets/restart/action | Restarts the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/rollingUpgrades/cancel/action | Cancels the rolling upgrade of a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/rollingUpgrades/read | Get latest Rolling Upgrade status for a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/scale/action | Verify if an existing Virtual Machine Scale Set can Scale In/Scale Out to specified instance count |
> | Action | Microsoft.Compute/virtualMachineScaleSets/skus/read | Lists the valid SKUs for an existing Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/start/action | Starts the instances of the Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/deallocate/action | Powers off and releases the compute resources for a Virtual Machine in a VM Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/delete | Delete a specific Virtual Machine in a VM Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/instanceView/read | Retrieves the instance view of a Virtual Machine in a VM Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/networkInterfaces/ipConfigurations/publicIPAddresses/read | Get properties of public IP address created using Virtual Machine Scale Set. Virtual Machine Scale Set can create at most one public IP per ipconfiguration (private IP) |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/networkInterfaces/ipConfigurations/read | Get properties of one or all IP configurations of a network interface created using Virtual Machine Scale Set. IP configurations represent private IPs |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/networkInterfaces/read | Get properties of one or all network interfaces of a virtual machine created using Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/performMaintenance/action | Performs planned maintenance on a Virtual Machine instance in a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/powerOff/action | Powers Off a Virtual Machine instance in a VM Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/providers/Microsoft.Insights/metricDefinitions/read | Reads Virtual Machine in Scale Set Metric Definitions |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/read | Retrieves the properties of a Virtual Machine in a VM Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/redeploy/action | Redeploys a Virtual Machine instance in a Virtual Machine Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/reimage/action | Reimages a Virtual Machine instance in a Virtual Machine Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/reimageAll/action | Reimages all disks (OS Disk and Data Disks) for Virtual Machine instance in a Virtual Machine Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/restart/action | Restarts a Virtual Machine instance in a VM Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/runCommand/action | Executes a predefined script on a Virtual Machine instance in a Virtual Machine Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/start/action | Starts a Virtual Machine instance in a VM Scale Set. |
> | Action | Microsoft.Compute/virtualMachineScaleSets/virtualMachines/write | Updates the properties of a Virtual Machine in a VM Scale Set |
> | Action | Microsoft.Compute/virtualMachineScaleSets/write | Creates a new Virtual Machine Scale Set or updates an existing one |

## Microsoft.Consumption

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Consumption/balances/read | List the utilization summary for a billing period for a management group. |
> | Action | Microsoft.Consumption/budgets/read | List the budgets by a subscription or a management group. |
> | Action | Microsoft.Consumption/budgets/write | Creates, update and delete the budgets by a subscription or a management group. |
> | Action | Microsoft.Consumption/marketplaces/read | List the marketplace resource usage details for a scope for EA and WebDirect subscriptions. |
> | Action | Microsoft.Consumption/operations/read | List all supported operations by Microsoft.Consumption resource provider. |
> | Action | Microsoft.Consumption/pricesheets/read | List the Pricesheets data for a subscription or a management group. |
> | Action | Microsoft.Consumption/reservationDetails/read | List the utilization details for reserved instances by reservation order or managment groups. The details data is per instance per day level. |
> | Action | Microsoft.Consumption/reservationRecommendations/read | List single or shared recommendations for Reserved instances for a subscription. |
> | Action | Microsoft.Consumption/reservationSummaries/read | List the utilization summary for reserved instances by reservation order or managment groups. The summary data is either at monthly or daily level. |
> | Action | Microsoft.Consumption/reservationTransactions/read | List the transaction history for reserved instances by management groups. |
> | Action | Microsoft.Consumption/tenants/register/action | Register action for scope of Microsoft.Consumption by a tenant. |
> | Action | Microsoft.Consumption/terms/read | List the terms for a subscription or a management group. |
> | Action | Microsoft.Consumption/usageDetails/read | List the usage details for a scope for EA and WebDirect subscriptions. |

## Microsoft.ContainerInstance

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ContainerInstance/containerGroups/containers/logs/read | Get logs for a specific container. |
> | Action | Microsoft.ContainerInstance/containerGroups/delete | Delete the specific container group. |
> | Action | Microsoft.ContainerInstance/containerGroups/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the container group. |
> | Action | Microsoft.ContainerInstance/containerGroups/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the container group. |
> | Action | Microsoft.ContainerInstance/containerGroups/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for container group. |
> | Action | Microsoft.ContainerInstance/containerGroups/read | Get all container goups. |
> | Action | Microsoft.ContainerInstance/containerGroups/restart/action | Restarts a specific container group. |
> | Action | Microsoft.ContainerInstance/containerGroups/stop/action | Stops a specific container group. Compute resources will be deallocated and billing will stop. |
> | Action | Microsoft.ContainerInstance/containerGroups/write | Create or update a specific container group. |
> | Action | Microsoft.ContainerInstance/register/action | Registers the subscription for the container instance resource provider and enables the creation of container groups. |

## Microsoft.ContainerRegistry

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ContainerRegistry/checkNameAvailability/read | Checks whether the container registry name is available for use. |
> | Action | Microsoft.ContainerRegistry/locations/deleteVirtualNetworkOrSubnets/action | Notifies Microsoft.ContainerRegistry that virtual network or subnet is being deleted |
> | Action | Microsoft.ContainerRegistry/locations/operationResults/read | Gets an async operation result |
> | Action | Microsoft.ContainerRegistry/operations/read | Lists all of the available Azure Container Registry REST API operations |
> | Action | Microsoft.ContainerRegistry/register/action | Registers the subscription for the container registry resource provider and enables the creation of container registries. |
> | Action | Microsoft.ContainerRegistry/registries/builds/cancel/action | Cancels an existing build. |
> | Action | Microsoft.ContainerRegistry/registries/builds/getLogLink/action | Gets a link to download the build logs. |
> | Action | Microsoft.ContainerRegistry/registries/builds/read | Gets the properties of the specified build or lists all the builds for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/builds/write | Updates a build for a container registry with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/delete | Deletes a build task from a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/listSourceRepositoryProperties/action | Lists the source control properties for a build task. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/read | Gets the properties of the specified build task or lists all the build tasks for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/steps/delete | Deletes a build step from a build task. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/steps/listBuildArguments/action | Lists the build arguments for a build step including the secret arguments. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/steps/read | Gets the properties of the specified build step or lists all the build steps for the specified build task. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/steps/write | Creates or updates a build step for a build task with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/buildTasks/write | Creates or updates a build task for a container registry with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/delete | Deletes a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/eventGridFilters/delete | Deletes an event grid filter from a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/eventGridFilters/read | Gets the properties of the specified event grid filter or lists all the event grid filters for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/eventGridFilters/write | Creates or updates an event grid filter for a container registry with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/getBuildSourceUploadUrl/action | Gets the upload location for the user to be able to upload the source. |
> | Action | Microsoft.ContainerRegistry/registries/importImage/action | Import Image to container registry with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/listCredentials/action | Lists the login credentials for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/listPolicies/read | Lists the policies for the specified container registry |
> | Action | Microsoft.ContainerRegistry/registries/listUsages/read | Lists the quota usages for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/operationStatuses/read | Gets a registry async operation status |
> | Action | Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.ContainerRegistry/registries/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Microsoft ContainerRegistry |
> | Action | Microsoft.ContainerRegistry/registries/pull/read | Pull or Get images from a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/push/write | Push or Write images to a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/quarantineRead/read | Pull or Get quarantined images from container registry |
> | Action | Microsoft.ContainerRegistry/registries/quarantineWrite/write | Write/Modify quarantine state of quarantined images |
> | Action | Microsoft.ContainerRegistry/registries/queueBuild/action | Creates a new build based on the request parameters and add it to the build queue. |
> | Action | Microsoft.ContainerRegistry/registries/read | Gets the properties of the specified container registry or lists all the container registries under the specified resource group or subscription. |
> | Action | Microsoft.ContainerRegistry/registries/regenerateCredential/action | Regenerates one of the login credentials for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/replications/delete | Deletes a replication from a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/replications/operationStatuses/read | Gets a replication async operation status |
> | Action | Microsoft.ContainerRegistry/registries/replications/read | Gets the properties of the specified replication or lists all the replications for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/replications/write | Creates or updates a replication for a container registry with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/sign/write | Push/Pull content trust metadata for a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/updatePolicies/write | Updates the policies for the specified container registry |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/delete | Deletes a webhook from a container registry. |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/getCallbackConfig/action | Gets the configuration of service URI and custom headers for the webhook. |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/listEvents/action | Lists recent events for the specified webhook. |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/operationStatuses/read | Gets a webhook async operation status |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/ping/action | Triggers a ping event to be sent to the webhook. |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/read | Gets the properties of the specified webhook or lists all the webhooks for the specified container registry. |
> | Action | Microsoft.ContainerRegistry/registries/webhooks/write | Creates or updates a webhook for a container registry with the specified parameters. |
> | Action | Microsoft.ContainerRegistry/registries/write | Creates or updates a container registry with the specified parameters. |

## Microsoft.ContainerService

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ContainerService/containerServices/delete | Deletes a container service |
> | Action | Microsoft.ContainerService/containerServices/read | Get a container service |
> | Action | Microsoft.ContainerService/containerServices/write | Creates a new container service or updates an existing one |
> | Action | Microsoft.ContainerService/locations/operationresults/read | Gets the status of an asynchronous operation result |
> | Action | Microsoft.ContainerService/locations/operations/read | Gets the status of an asynchronous operation |
> | Action | Microsoft.ContainerService/locations/orchestrators/read | Lists the supported orchestrators |
> | Action | Microsoft.ContainerService/managedClusters/accessProfiles/listCredential/action | Get a managed cluster access profile by role name using list credential |
> | Action | Microsoft.ContainerService/managedClusters/accessProfiles/read | Get a managed cluster access profile by role name |
> | Action | Microsoft.ContainerService/managedClusters/delete | Deletes a managed cluster |
> | Action | Microsoft.ContainerService/managedClusters/listClusterAdminCredential/action | List the clusterAdmin credential of a managed cluster |
> | Action | Microsoft.ContainerService/managedClusters/listClusterUserCredential/action | List the clusterUser credential of a managed cluster |
> | Action | Microsoft.ContainerService/managedClusters/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic setting for a managed cluster resource |
> | Action | Microsoft.ContainerService/managedClusters/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for a managed cluster resource |
> | Action | Microsoft.ContainerService/managedClusters/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Managed Cluster |
> | Action | Microsoft.ContainerService/managedClusters/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Managed Cluster |
> | Action | Microsoft.ContainerService/managedClusters/read | Get a managed cluster |
> | Action | Microsoft.ContainerService/managedClusters/upgradeprofiles/read | Gets the upgrade profile of the cluster |
> | Action | Microsoft.ContainerService/managedClusters/write | Creates a new managed cluster or updates an existing one |
> | Action | Microsoft.ContainerService/operations/read | Lists operations available on Microsoft.ContainerService resource provider |
> | Action | Microsoft.ContainerService/register/action | Registers Subscription with Microsoft.ContainerService resource provider |
> | Action | Microsoft.ContainerService/unregister/action | Unregisters Subscription with Microsoft.ContainerService resource provider |

## Microsoft.ContentModerator

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ContentModerator/applications/delete | Delete Operation |
> | Action | Microsoft.ContentModerator/applications/listSecrets/action | List Secrets |
> | Action | Microsoft.ContentModerator/applications/listSingleSignOnToken/action | Read Single Sign On Tokens |
> | Action | Microsoft.ContentModerator/applications/read | Read Operation |
> | Action | Microsoft.ContentModerator/applications/write | Write Operation |
> | Action | Microsoft.ContentModerator/applications/write | Write Operation |
> | Action | Microsoft.ContentModerator/listCommunicationPreference/action | List communication preference |
> | Action | Microsoft.ContentModerator/operations/read | read operations |
> | Action | Microsoft.ContentModerator/updateCommunicationPreference/action | Update communication preference |

## Microsoft.CostManagement

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.CostManagement/dimensions/read | List all supported dimensions by a scope. |
> | Action | Microsoft.CostManagement/query/action | Query usage data by a scope. |
> | Action | Microsoft.CostManagement/query/read | Query usage data by a scope. |
> | Action | Microsoft.CostManagement/reports/action | Schedule reports on usage data by a scope. |
> | Action | Microsoft.CostManagement/reports/read | Schedule reports on usage data by a scope. |

## Microsoft.CustomerInsights

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.CustomerInsights/hubs/adobemetadata/action | Create or Update any Azure Customer Insights Adobe Metadata |
> | Action | Microsoft.CustomerInsights/hubs/adobemetadata/read | Read any Azure Customer Insights Adobe Metadata |
> | Action | Microsoft.CustomerInsights/hubs/authorizationPolicies/delete | Delete any Azure Customer Insights Shared Access Signature Policy |
> | Action | Microsoft.CustomerInsights/hubs/authorizationPolicies/read | Read any Azure Customer Insights Shared Access Signature Policy |
> | Action | Microsoft.CustomerInsights/hubs/authorizationPolicies/regeneratePrimaryKey/action | Regenerate Azure Customer Insights Shared Access Signature Policy primary key |
> | Action | Microsoft.CustomerInsights/hubs/authorizationPolicies/regenerateSecondaryKey/action | Regenerate Azure Customer Insights Shared Access Signature Policy secondary key |
> | Action | Microsoft.CustomerInsights/hubs/authorizationPolicies/write | Create or Update any Azure Customer Insights Shared Access Signature Policy |
> | Action | Microsoft.CustomerInsights/hubs/connectors/activate/action | Activate any Azure Customer Insights Connector |
> | Action | Microsoft.CustomerInsights/hubs/connectors/activate/action | Activate any Azure Customer Insights Connector |
> | Action | Microsoft.CustomerInsights/hubs/connectors/delete | Delete any Azure Customer Insights Connector |
> | Action | Microsoft.CustomerInsights/hubs/connectors/getruntimestatus/action | Get any Azure Customer Insights Connector runtime status |
> | Action | Microsoft.CustomerInsights/hubs/connectors/mappings/activate/action | Activate any Azure Customer Insights Connector Mapping |
> | Action | Microsoft.CustomerInsights/hubs/connectors/mappings/delete | Delete any Azure Customer Insights Connector Mapping |
> | Action | Microsoft.CustomerInsights/hubs/connectors/mappings/operations/read | Read any Azure Customer Insights Connector Mapping operation result |
> | Action | Microsoft.CustomerInsights/hubs/connectors/mappings/read | Read any Azure Customer Insights Connector Mapping |
> | Action | Microsoft.CustomerInsights/hubs/connectors/mappings/write | Create or Update any Azure Customer Insights Connector Mapping |
> | Action | Microsoft.CustomerInsights/hubs/connectors/operations/read | Read any Azure Customer Insights Connector operation result |
> | Action | Microsoft.CustomerInsights/hubs/connectors/read | Read any Azure Customer Insights Connector |
> | Action | Microsoft.CustomerInsights/hubs/connectors/saveauthinfo/action | Create or Update any Azure Customer Insights Connector Authentication Infomation |
> | Action | Microsoft.CustomerInsights/hubs/connectors/update/action | Update any Azure Customer Insights Connector |
> | Action | Microsoft.CustomerInsights/hubs/connectors/write | Create or Update any Azure Customer Insights Connector |
> | Action | Microsoft.CustomerInsights/hubs/crmmetadata/action | Create or Update any Azure Customer Insights Crm Metadata |
> | Action | Microsoft.CustomerInsights/hubs/crmmetadata/read | Read any Azure Customer Insights Crm Metadata |
> | Action | Microsoft.CustomerInsights/hubs/delete | Delete any Azure Customer Insights Hub |
> | Action | Microsoft.CustomerInsights/hubs/gdpr/delete | Delete any Azure Customer Insights Gdpr |
> | Action | Microsoft.CustomerInsights/hubs/gdpr/read | Read any Azure Customer Insights Gdpr |
> | Action | Microsoft.CustomerInsights/hubs/gdpr/write | Create or Update any Azure Customer Insights Gdpr |
> | Action | Microsoft.CustomerInsights/hubs/getbillingcredits/read | Get Azure Customer Insights Hub Billing Credits |
> | Action | Microsoft.CustomerInsights/hubs/getbillinghistory/read | Get Azure Customer Insights Hub Billing History |
> | Action | Microsoft.CustomerInsights/hubs/images/delete | Delete any Azure Customer Insights Image |
> | Action | Microsoft.CustomerInsights/hubs/images/read | Read any Azure Customer Insights Image |
> | Action | Microsoft.CustomerInsights/hubs/images/write | Create or Update any Azure Customer Insights Image |
> | Action | Microsoft.CustomerInsights/hubs/interactions/delete | Delete any azure Customer Insights Interactions |
> | Action | Microsoft.CustomerInsights/hubs/interactions/operations/read | Read any Azure Customer Insights Interaction operation result |
> | Action | Microsoft.CustomerInsights/hubs/interactions/read | Read any Azure Customer Insights Interaction |
> | Action | Microsoft.CustomerInsights/hubs/interactions/suggestrelationshiplinks/action | Suggest RelationShip Links for any Azure Customer Insights Interactions |
> | Action | Microsoft.CustomerInsights/hubs/interactions/write | Create or Update any Azure Customer Insights Interaction |
> | Action | Microsoft.CustomerInsights/hubs/kpi/delete | Delete any Azure Customer Insights Key Performance Indicator |
> | Action | Microsoft.CustomerInsights/hubs/kpi/operations/read | Read any Azure Customer Insights Key Performance Indicators operation result |
> | Action | Microsoft.CustomerInsights/hubs/kpi/read | Read any Azure Customer Insights Key Performance Indicator |
> | Action | Microsoft.CustomerInsights/hubs/kpi/reprocess/action | Reprocess any Azure Customer Insights Key Performance Indicators |
> | Action | Microsoft.CustomerInsights/hubs/kpi/write | Create or Update any Azure Customer Insights Key Performance Indicator |
> | Action | Microsoft.CustomerInsights/hubs/links/delete | Delete any Azure Customer Insights Links |
> | Action | Microsoft.CustomerInsights/hubs/links/operations/read | Read any Azure Customer Insights Links operation result |
> | Action | Microsoft.CustomerInsights/hubs/links/read | Read any Azure Customer Insights Links |
> | Action | Microsoft.CustomerInsights/hubs/links/write | Create or Update any Azure Customer Links |
> | Action | Microsoft.CustomerInsights/hubs/msemetadata/action | Create or Update any Azure Customer Insights Mse Metadata |
> | Action | Microsoft.CustomerInsights/hubs/msemetadata/read | Read any Azure Customer Insights Mse Metadata |
> | Action | Microsoft.CustomerInsights/hubs/operationresults/read | Get Azure Customer Insights Hub Operation Results |
> | Action | Microsoft.CustomerInsights/hubs/predictions/delete | Delete any Azure Customer Insights Predictions |
> | Action | Microsoft.CustomerInsights/hubs/predictions/operations/read | Read any Azure Customer Insights Predictions operation result |
> | Action | Microsoft.CustomerInsights/hubs/predictions/read | Read any Azure Customer Insights Predictions |
> | Action | Microsoft.CustomerInsights/hubs/predictions/write | Create or Update any Azure Customer Predictions |
> | Action | Microsoft.CustomerInsights/hubs/predictivematchpolicies/delete | Delete any Azure Customer Insights Predictive Match Policies |
> | Action | Microsoft.CustomerInsights/hubs/predictivematchpolicies/operations/read | Read any Azure Customer Insights Predictive Match Policies operation result |
> | Action | Microsoft.CustomerInsights/hubs/predictivematchpolicies/read | Read any Azure Customer Insights Predictive Match Policies |
> | Action | Microsoft.CustomerInsights/hubs/predictivematchpolicies/write | Create or Update any Azure Customer Insights Predictive Match Policies |
> | Action | Microsoft.CustomerInsights/hubs/profiles/delete | Delete any Azure Customer Insights Profile |
> | Action | Microsoft.CustomerInsights/hubs/profiles/operations/read | Read any Azure Customer Insights Profile operation result |
> | Action | Microsoft.CustomerInsights/hubs/profiles/read | Read any Azure Customer Insights Profile |
> | Action | Microsoft.CustomerInsights/hubs/profiles/write | Write any Azure Customer Insights Profile |
> | Action | Microsoft.CustomerInsights/hubs/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.CustomerInsights/hubs/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.CustomerInsights/hubs/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for resource |
> | Action | Microsoft.CustomerInsights/hubs/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for resource |
> | Action | Microsoft.CustomerInsights/hubs/read | Read any Azure Customer Insights Hub |
> | Action | Microsoft.CustomerInsights/hubs/relationshiplinks/delete | Delete any Azure Customer Insights Relationship Links |
> | Action | Microsoft.CustomerInsights/hubs/relationshiplinks/operations/read | Read any Azure Customer Insights Relationship Links operation result |
> | Action | Microsoft.CustomerInsights/hubs/relationshiplinks/read | Read any Azure Customer Insights Relationship Links |
> | Action | Microsoft.CustomerInsights/hubs/relationshiplinks/write | Create or Update any Azure Customer Insights Relationship Links |
> | Action | Microsoft.CustomerInsights/hubs/relationships/delete | Delete any Azure Customer Insights Relationships |
> | Action | Microsoft.CustomerInsights/hubs/relationships/operations/read | Read any Azure Customer Insights Relationships operation result |
> | Action | Microsoft.CustomerInsights/hubs/relationships/read | Read any Azure Customer Insights Relationships |
> | Action | Microsoft.CustomerInsights/hubs/relationships/write | Create or Update any Azure Customer Insights Relationships |
> | Action | Microsoft.CustomerInsights/hubs/roleAssignments/delete | Delete any Azure Customer Insights Rbac Assignment |
> | Action | Microsoft.CustomerInsights/hubs/roleAssignments/operations/read | Read any Azure Customer Insights Rbac Assignment operation result |
> | Action | Microsoft.CustomerInsights/hubs/roleAssignments/read | Read any Azure Customer Insights Rbac Assignment |
> | Action | Microsoft.CustomerInsights/hubs/roleAssignments/write | Create or Update any Azure Customer Insights Rbac Assignment |
> | Action | Microsoft.CustomerInsights/hubs/roles/read | Read any Azure Customer Insights Rbac Roles |
> | Action | Microsoft.CustomerInsights/hubs/salesforcemetadata/action | Create or Update any Azure Customer Insights SalesForce Metadata |
> | Action | Microsoft.CustomerInsights/hubs/salesforcemetadata/read | Read any Azure Customer Insights SalesForce Metadata |
> | Action | Microsoft.CustomerInsights/hubs/segments/delete | Delete any Azure Customer Insights Segments |
> | Action | Microsoft.CustomerInsights/hubs/segments/dynamic/action | Management any Azure Customer Insight Dynamic Segments |
> | Action | Microsoft.CustomerInsights/hubs/segments/read | Read any Azure Customer Insights Segments |
> | Action | Microsoft.CustomerInsights/hubs/segments/static/action | Management any Azure Customer Insight Static Segments |
> | Action | Microsoft.CustomerInsights/hubs/segments/write | Create or Update any Azure Customer Insights Segments |
> | Action | Microsoft.CustomerInsights/hubs/sqlconnectionstrings/delete | Delete any Azure Customer Insights SqlConnectionStrings |
> | Action | Microsoft.CustomerInsights/hubs/sqlconnectionstrings/read | Read any Azure Customer Insights SqlConnectionStrings |
> | Action | Microsoft.CustomerInsights/hubs/sqlconnectionstrings/write | Create or Update any Azure Customer Insights SqlConnectionStrings |
> | Action | Microsoft.CustomerInsights/hubs/suggesttypeschema/action | Generate Suggest Type Schema from sample data |
> | Action | Microsoft.CustomerInsights/hubs/tenantmanagement/read | Manage any Azure Customer Insights hub settings |
> | Action | Microsoft.CustomerInsights/hubs/views/delete | Delete any Azure Customer Insights App View |
> | Action | Microsoft.CustomerInsights/hubs/views/read | Read any Azure Customer Insights App View |
> | Action | Microsoft.CustomerInsights/hubs/views/write | Create or Update any Azure Customer Insights App View |
> | Action | Microsoft.CustomerInsights/hubs/widgettypes/read | Read any Azure Customer Insights App Widget Types |
> | Action | Microsoft.CustomerInsights/hubs/write | Create or Update any Azure Customer Insights Hub |
> | Action | Microsoft.CustomerInsights/operations/read | Read Azure Customer Insights Api Metadatas |
> | Action | Microsoft.CustomerInsights/register/action | Registers the subscription for the Customer Insights resource provider and enables the creation of Customer Insights resources |
> | Action | Microsoft.CustomerInsights/unregister/action | Unregisters the subscription for the Customer Insights resource provider |

## Microsoft.DataBox

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataBox/jobs/bookShipmentPickUp/action | Allows to book a pick up for return shipments. |
> | Action | Microsoft.DataBox/jobs/cancel/action | Cancels an order in progress. |
> | Action | Microsoft.DataBox/jobs/delete | Delete the Orders |
> | Action | Microsoft.DataBox/jobs/listCredentials/action | Lists the unencrypted credentials related to the order. |
> | Action | Microsoft.DataBox/jobs/read | List or get the Orders |
> | Action | Microsoft.DataBox/jobs/write | Create or update the Orders |
> | Action | Microsoft.DataBox/locations/availableSkus/action | This method returns the list of available skus. |
> | Action | Microsoft.DataBox/locations/validateAddress/action | Validates the shipping address and provides alternate addresses if any. |

## Microsoft.DataBoxEdge

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/alerts/read | Lists or gets the alerts |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/alerts/read | Lists or gets the alerts |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/bandwidthSchedules/delete | Deletes the bandwidth schedules |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/bandwidthSchedules/read | Lists or gets the bandwidth schedules |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/bandwidthSchedules/read | Lists or gets the bandwidth schedules |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/bandwidthSchedules/write | Creates or updates the bandwidth schedules |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/delete | Deletes the Data Box Edge devices |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/downloadUpdates/action | Download Updates in device |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/extendedInformation/action | Retrieves resource extended information |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/extendedInformation/write | Creates or updates the resource extended information |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/installUpdates/action | Install Updates on device |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/jobs/read | Lists or gets the jobs |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/networkSettings/read | Lists or gets the Device network settings |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostics setting for the resource |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/providers/Microsoft.Insights/metricDefinitions/read | Gets the available Data Box Edge device level metrics |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/read | Lists or gets the Data Box Edge devices |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/read | Lists or gets the Data Box Edge devices |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/read | Lists or gets the Data Box Edge devices |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/roles/delete | Deletes the ArmApiRes_roles |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/roles/read | Lists or gets the ArmApiRes_roles |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/roles/read | Lists or gets the ArmApiRes_roles |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/roles/write | Creates or updates the ArmApiRes_roles |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/scanForUpdates/action | Scan for updates |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/securitySettings/update/action | Update security settings |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/shares/delete | Deletes the shares |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/shares/read | Lists or gets the shares |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/shares/read | Lists or gets the shares |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/shares/refresh/action | ArmApiDesc_action_refresh_shares |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/shares/write | Creates or updates the shares |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/storageAccountCredentials/delete | Deletes the storage account credentials |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/storageAccountCredentials/read | Lists or gets the storage account credentials |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/storageAccountCredentials/read | Lists or gets the storage account credentials |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/storageAccountCredentials/write | Creates or updates the storage account credentials |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/updateSummary/read | Lists or gets the update summary |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/uploadCertificate/action | Upload certificate for device registration |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/users/delete | Deletes the share users |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/users/read | Lists or gets the share users |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/users/read | Lists or gets the share users |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/users/write | Creates or updates the share users |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/write | Creates or updates the Data Box Edge devices |
> | Action | Microsoft.DataBoxEdge/dataBoxEdgeDevices/write | Creates or updates the Data Box Edge devices |

## Microsoft.Databricks

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Databricks/workspaces/delete | Removes an workspace. |
> | Action | Microsoft.Databricks/workspaces/read | Retrieves a list of workspaces. |
> | Action | Microsoft.Databricks/workspaces/write | Creates an workspace. |

## Microsoft.DataCatalog

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataCatalog/catalogs/delete | Deletes the catalog. |
> | Action | Microsoft.DataCatalog/catalogs/read | Get properties for catalog or catalogs under subscription or resource group. |
> | Action | Microsoft.DataCatalog/catalogs/write | Creates catalog or updates the tags and properties for the catalog. |
> | Action | Microsoft.DataCatalog/checkNameAvailability/action | Checks catalog name availability for tenant. |
> | Action | Microsoft.DataCatalog/operations/read | Lists operations available on Microsoft.DataCatalog resource provider. |
> | Action | Microsoft.DataCatalog/register/action | Registers subscription with Microsoft.DataCatalog resource provider. |
> | Action | Microsoft.DataCatalog/unregister/action | Unregisters subscription from Microsoft.DataCatalog resource provider. |

## Microsoft.DataFactory

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataFactory/datafactories/activitywindows/read | Reads Activity Windows in the Data Factory with specified parameters. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/activities/activitywindows/read | Reads Activity Windows for the Pipeline Activity with specified parameters. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/activitywindows/read | Reads Activity Windows for the Pipeline with specified parameters. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/delete | Deletes any Pipeline. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/pause/action | Pauses any Pipeline. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/read | Reads any Pipeline. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/resume/action | Resumes any Pipeline. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/update/action | Updates any Pipeline. |
> | Action | Microsoft.DataFactory/datafactories/datapipelines/write | Creates or Updates any Pipeline. |
> | Action | Microsoft.DataFactory/datafactories/datasets/activitywindows/read | Reads Activity Windows for the Dataset with specified parameters. |
> | Action | Microsoft.DataFactory/datafactories/datasets/delete | Deletes any Dataset. |
> | Action | Microsoft.DataFactory/datafactories/datasets/read | Reads any Dataset. |
> | Action | Microsoft.DataFactory/datafactories/datasets/sliceruns/read | Reads the Data Slice Run for the given dataset with the given start time. |
> | Action | Microsoft.DataFactory/datafactories/datasets/slices/read | Gets the Data Slices in the given period. |
> | Action | Microsoft.DataFactory/datafactories/datasets/slices/write | Update the Status of the Data Slice. |
> | Action | Microsoft.DataFactory/datafactories/datasets/write | Creates or Updates any Dataset. |
> | Action | Microsoft.DataFactory/datafactories/delete | Deletes the Data Factory. |
> | Action | Microsoft.DataFactory/datafactories/gateways/connectioninfo/action | Reads the Connection Info for any Gateway. |
> | Action | Microsoft.DataFactory/datafactories/gateways/delete | Deletes any Gateway. |
> | Action | Microsoft.DataFactory/datafactories/gateways/listauthkeys/action | Lists the Authentication Keys for any Gateway. |
> | Action | Microsoft.DataFactory/datafactories/gateways/read | Reads any Gateway. |
> | Action | Microsoft.DataFactory/datafactories/gateways/regenerateauthkey/action | Regenerates the Authentication Keys for any Gateway. |
> | Action | Microsoft.DataFactory/datafactories/gateways/write | Creates or Updates any Gateway. |
> | Action | Microsoft.DataFactory/datafactories/linkedServices/delete | Deletes any Linked Service. |
> | Action | Microsoft.DataFactory/datafactories/linkedServices/read | Reads any Linked Service. |
> | Action | Microsoft.DataFactory/datafactories/linkedServices/write | Creates or Updates any Linked Service. |
> | Action | Microsoft.DataFactory/datafactories/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.DataFactory/datafactories/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.DataFactory/datafactories/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for datafactories |
> | Action | Microsoft.DataFactory/datafactories/read | Reads the Data Factory. |
> | Action | Microsoft.DataFactory/datafactories/runs/loginfo/read | Reads a SAS URI to a blob container containing the logs. |
> | Action | Microsoft.DataFactory/datafactories/tables/delete | Deletes any Dataset. |
> | Action | Microsoft.DataFactory/datafactories/tables/read | Reads any Dataset. |
> | Action | Microsoft.DataFactory/datafactories/tables/write | Creates or Updates any Dataset. |
> | Action | Microsoft.DataFactory/datafactories/write | Creates or Updates the Data Factory. |
> | Action | Microsoft.DataFactory/factories/cancelpipelinerun/action | Cancels the pipeline run specified by the run ID. |
> | Action | Microsoft.DataFactory/factories/datasets/delete | Deletes any Dataset. |
> | Action | Microsoft.DataFactory/factories/datasets/read | Reads any Dataset. |
> | Action | Microsoft.DataFactory/factories/datasets/write | Creates or Updates any Dataset. |
> | Action | Microsoft.DataFactory/factories/delete | Deletes Data Factory. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/delete | Deletes any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/getconnectioninfo/read | Reads Integration Runtime Connection Info. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/getstatus/read | Reads Integration Runtime Status. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/listauthkeys/read | Lists the Authentication Keys for any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/monitoringdata/read | Gets the Monitoring Data for any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/nodes/delete | Deletes the Node for the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/nodes/ipAddress/action | Returns the IP Address for the specified node of the Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/nodes/read | Reads the Node for the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/nodes/write | Updates a self-hosted Integration Runtime Node. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/queryactivityruns/action | Queries Activity Runs for the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/read | Reads any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/regenerateauthkey/action | Regenerates the Authentication Keys for the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/removelinks/action | Removes Linked Integration Runtime References from the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/start/action | Starts any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/stop/action | Stops any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/synccredentials/action | Syncs the Credentials for the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/upgrade/action | Upgrades the specified Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/integrationruntimes/write | Creates or Updates any Integration Runtime. |
> | Action | Microsoft.DataFactory/factories/linkedServices/delete | Deletes Linked Service. |
> | Action | Microsoft.DataFactory/factories/linkedServices/read | Reads Linked Service. |
> | Action | Microsoft.DataFactory/factories/linkedServices/write | Create or Update Linked Service |
> | Action | Microsoft.DataFactory/factories/pipelineruns/activityruns/read | Reads the activity runs for the specified pipeline run ID. |
> | Action | Microsoft.DataFactory/factories/pipelineruns/cancel/action | Cancels the pipeline run specified by the run ID. |
> | Action | Microsoft.DataFactory/factories/pipelineruns/queryactivityruns/action | Queries the activity runs for the specified pipeline run ID. |
> | Action | Microsoft.DataFactory/factories/pipelineruns/queryactivityruns/read | Reads the result of query activity runs for the specified pipeline run ID. |
> | Action | Microsoft.DataFactory/factories/pipelineruns/read | Reads the Pipeline Runs. |
> | Action | Microsoft.DataFactory/factories/pipelines/createrun/action | Creates a run for the Pipeline. |
> | Action | Microsoft.DataFactory/factories/pipelines/delete | Deletes Pipeline. |
> | Action | Microsoft.DataFactory/factories/pipelines/pipelineruns/activityruns/progress/read | Gets the Progress of Activity Runs. |
> | Action | Microsoft.DataFactory/factories/pipelines/pipelineruns/read | Reads the Pipeline Run. |
> | Action | Microsoft.DataFactory/factories/pipelines/read | Reads Pipeline. |
> | Action | Microsoft.DataFactory/factories/pipelines/write | Create or Update Pipeline |
> | Action | Microsoft.DataFactory/factories/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.DataFactory/factories/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.DataFactory/factories/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for factories |
> | Action | Microsoft.DataFactory/factories/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for factories |
> | Action | Microsoft.DataFactory/factories/querypipelineruns/action | Queries the Pipeline Runs. |
> | Action | Microsoft.DataFactory/factories/querypipelineruns/read | Reads the Result of Query Pipeline Runs. |
> | Action | Microsoft.DataFactory/factories/querytriggerruns/action | Queries the Trigger Runs. |
> | Action | Microsoft.DataFactory/factories/querytriggerruns/read | Reads the Result of Trigger Runs. |
> | Action | Microsoft.DataFactory/factories/read | Reads Data Factory. |
> | Action | Microsoft.DataFactory/factories/triggerruns/read | Reads the Trigger Runs. |
> | Action | Microsoft.DataFactory/factories/triggers/delete | Deletes any Trigger. |
> | Action | Microsoft.DataFactory/factories/triggers/read | Reads any Trigger. |
> | Action | Microsoft.DataFactory/factories/triggers/start/action | Starts any Trigger. |
> | Action | Microsoft.DataFactory/factories/triggers/stop/action | Stops any Trigger. |
> | Action | Microsoft.DataFactory/factories/triggers/triggerruns/read | Reads the Trigger Runs. |
> | Action | Microsoft.DataFactory/factories/triggers/write | Creates or Updates any Trigger. |
> | Action | Microsoft.DataFactory/factories/write | Create or Update Data Factory |
> | Action | Microsoft.DataFactory/locations/configureFactoryRepo/action | Configures the repository for the factory. |
> | Action | Microsoft.DataFactory/operations/read | Reads all Operations in Microsoft Data Factory Provider. |
> | Action | Microsoft.DataFactory/register/action | Registers the subscription for the Data Factory Resource Provider. |
> | Action | Microsoft.DataFactory/unregister/action | Unregisters the subscription for the Data Factory Resource Provider. |

## Microsoft.DataLakeAnalytics

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataLakeAnalytics/accounts/computePolicies/delete | Delete a compute policy. |
> | Action | Microsoft.DataLakeAnalytics/accounts/computePolicies/read | Get information about a compute policy. |
> | Action | Microsoft.DataLakeAnalytics/accounts/computePolicies/write | Create or update a compute policy. |
> | Action | Microsoft.DataLakeAnalytics/accounts/dataLakeStoreAccounts/delete | Unlink a DataLakeStore account from a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/dataLakeStoreAccounts/read | Get information about a linked DataLakeStore account of a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/dataLakeStoreAccounts/write | Create or update a linked DataLakeStore account of a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/delete | Delete a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/firewallRules/delete | Delete a firewall rule. |
> | Action | Microsoft.DataLakeAnalytics/accounts/firewallRules/read | Get information about a firewall rule. |
> | Action | Microsoft.DataLakeAnalytics/accounts/firewallRules/write | Create or update a firewall rule. |
> | Action | Microsoft.DataLakeAnalytics/accounts/operationResults/read | Get result of a DataLakeAnalytics account operation. |
> | Action | Microsoft.DataLakeAnalytics/accounts/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic settings for the DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/providers/Microsoft.Insights/diagnosticSettings/write | Create or update the diagnostic settings for the DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/providers/Microsoft.Insights/logDefinitions/read | Get the available logs for the DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/providers/Microsoft.Insights/metricDefinitions/read | Get the available metrics for the DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/read | Get information about an existing DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/storageAccounts/Containers/listSasTokens/action | List SAS tokens for storage containers of a linked Storage account of a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/storageAccounts/Containers/read | Get containers of a linked Storage account of a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/storageAccounts/delete | Unlink a Storage account from a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/storageAccounts/read | Get information about a linked Storage account of a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/storageAccounts/write | Create or update a linked Storage account of a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/accounts/TakeOwnership/action | Grant permissions to cancel jobs submitted by other users. |
> | Action | Microsoft.DataLakeAnalytics/accounts/write | Create or update a DataLakeAnalytics account. |
> | Action | Microsoft.DataLakeAnalytics/locations/capability/read | Get capability information of a subscription regarding using DataLakeAnalytics. |
> | Action | Microsoft.DataLakeAnalytics/locations/checkNameAvailability/action | Check availability of a DataLakeAnalytics account name. |
> | Action | Microsoft.DataLakeAnalytics/locations/operationResults/read | Get result of a DataLakeAnalytics account operation. |
> | Action | Microsoft.DataLakeAnalytics/operations/read | Get available operations of DataLakeAnalytics. |
> | Action | Microsoft.DataLakeAnalytics/register/action | Register subscription to DataLakeAnalytics. |

## Microsoft.DataLakeStore

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataLakeStore/accounts/delete | Delete a DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/enableKeyVault/action | Enable KeyVault for a DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/eventGridFilters/delete | Delete an EventGrid Filter. |
> | Action | Microsoft.DataLakeStore/accounts/eventGridFilters/read | Get an EventGrid Filter. |
> | Action | Microsoft.DataLakeStore/accounts/eventGridFilters/write | Create or update an EventGrid Filter. |
> | Action | Microsoft.DataLakeStore/accounts/firewallRules/delete | Delete a firewall rule. |
> | Action | Microsoft.DataLakeStore/accounts/firewallRules/read | Get information about a firewall rule. |
> | Action | Microsoft.DataLakeStore/accounts/firewallRules/write | Create or update a firewall rule. |
> | Action | Microsoft.DataLakeStore/accounts/operationResults/read | Get result of a DataLakeStore account operation. |
> | Action | Microsoft.DataLakeStore/accounts/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic settings for the DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/providers/Microsoft.Insights/diagnosticSettings/write | Create or update the diagnostic settings for the DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/providers/Microsoft.Insights/logDefinitions/read | Get the available logs for the DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/providers/Microsoft.Insights/metricDefinitions/read | Get the available metrics for the DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/read | Get information about an existing DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/accounts/Superuser/action | Grant Superuser on Data Lake Store when granted with Microsoft.Authorization/roleAssignments/write. |
> | Action | Microsoft.DataLakeStore/accounts/trustedIdProviders/delete | Delete a trusted identity provider. |
> | Action | Microsoft.DataLakeStore/accounts/trustedIdProviders/read | Get information about a trusted identity provider. |
> | Action | Microsoft.DataLakeStore/accounts/trustedIdProviders/write | Create or update a trusted identity provider. |
> | Action | Microsoft.DataLakeStore/accounts/write | Create or update a DataLakeStore account. |
> | Action | Microsoft.DataLakeStore/locations/capability/read | Get capability information of a subscription regarding using DataLakeStore. |
> | Action | Microsoft.DataLakeStore/locations/checkNameAvailability/action | Check availability of a DataLakeStore account name. |
> | Action | Microsoft.DataLakeStore/locations/operationResults/read | Get result of a DataLakeStore account operation. |
> | Action | Microsoft.DataLakeStore/operations/read | Get available operations of DataLakeStore. |
> | Action | Microsoft.DataLakeStore/register/action | Register subscription to DataLakeStore. |

## Microsoft.DataMigration

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DataMigration/locations/operationResults/read | Get the status of a long-running operation related to a 202 Accepted response |
> | Action | Microsoft.DataMigration/locations/operationStatuses/read | Get the status of a long-running operation related to a 202 Accepted response |
> | Action | Microsoft.DataMigration/register/action | Registers the subscription with the Azure Database Migration Service provider |
> | Action | Microsoft.DataMigration/services/checkStatus/action | Check whether the service is deployed and running |
> | Action | Microsoft.DataMigration/services/delete | Deletes a resource and all of its children |
> | Action | Microsoft.DataMigration/services/projects/accessArtifacts/action | Generate a URL that can be used to GET or PUT project artifacts |
> | Action | Microsoft.DataMigration/services/projects/delete | Deletes a resource and all of its children |
> | Action | Microsoft.DataMigration/services/projects/files/delete | Deletes a resource and all of its children |
> | Action | Microsoft.DataMigration/services/projects/files/read | Read information about resources |
> | Action | Microsoft.DataMigration/services/projects/files/read/action | Obtain a URL that can be used to read the content of the file |
> | Action | Microsoft.DataMigration/services/projects/files/readWrite/action | Obtain a URL that can be used to read or write the content of the file |
> | Action | Microsoft.DataMigration/services/projects/files/write | Create or update resources and their properties |
> | Action | Microsoft.DataMigration/services/projects/read | Read information about resources |
> | Action | Microsoft.DataMigration/services/projects/tasks/cancel/action | Cancel the task if it's currently running |
> | Action | Microsoft.DataMigration/services/projects/tasks/delete | Deletes a resource and all of its children |
> | Action | Microsoft.DataMigration/services/projects/tasks/read | Read information about resources |
> | Action | Microsoft.DataMigration/services/projects/tasks/write | Run tasks Azure Database Migration Service tasks |
> | Action | Microsoft.DataMigration/services/projects/write | Run tasks Azure Database Migration Service tasks |
> | Action | Microsoft.DataMigration/services/read | Read information about resources |
> | Action | Microsoft.DataMigration/services/slots/delete | Deletes a resource and all of its children |
> | Action | Microsoft.DataMigration/services/slots/read | Read information about resources |
> | Action | Microsoft.DataMigration/services/slots/write | Create or update resources and their properties |
> | Action | Microsoft.DataMigration/services/start/action | Start the DMS service to allow it to process migrations again |
> | Action | Microsoft.DataMigration/services/stop/action | Stop the DMS service to minimize its cost |
> | Action | Microsoft.DataMigration/services/write | Create or update resources and their properties |
> | Action | Microsoft.DataMigration/skus/read | Get a list of SKUs supported by DMS resources. |

## Microsoft.DBforMariaDB

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DBforMariaDB/locations/performanceTiers/read | Returns the list of Performance Tiers available. |
> | Action | Microsoft.DBforMariaDB/performanceTiers/read | Returns the list of Performance Tiers available. |
> | Action | Microsoft.DBforMariaDB/servers/configurations/read | Return the list of configurations for a server or gets the properties for the specified configuration. |
> | Action | Microsoft.DBforMariaDB/servers/configurations/write | Update the value for the specified configuration |
> | Action | Microsoft.DBforMariaDB/servers/delete | Deletes an existing server. |
> | Action | Microsoft.DBforMariaDB/servers/firewallRules/delete | Deletes an existing firewall rule. |
> | Action | Microsoft.DBforMariaDB/servers/firewallRules/read | Return the list of firewall rules for a server or gets the properties for the specified firewall rule. |
> | Action | Microsoft.DBforMariaDB/servers/firewallRules/write | Creates a firewall rule with the specified parameters or update an existing rule. |
> | Action | Microsoft.DBforMariaDB/servers/providers/Microsoft.Insights/diagnosticSettings/read | Gets the disagnostic setting for the resource |
> | Action | Microsoft.DBforMariaDB/servers/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.DBforMariaDB/servers/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for databases |
> | Action | Microsoft.DBforMariaDB/servers/read | Return the list of servers or gets the properties for the specified server. |
> | Action | Microsoft.DBforMariaDB/servers/recoverableServers/read | Return the recoverable MariaDB Server info |
> | Action | Microsoft.DBforMariaDB/servers/updateConfigurations/action | Update configurations for the specified server |
> | Action | Microsoft.DBforMariaDB/servers/virtualNetworkRules/delete | Deletes an existing Virtual Network Rule |
> | Action | Microsoft.DBforMariaDB/servers/virtualNetworkRules/read | Return the list of virtual network rules or gets the properties for the specified virtual network rule. |
> | Action | Microsoft.DBforMariaDB/servers/virtualNetworkRules/write | Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule. |
> | Action | Microsoft.DBforMariaDB/servers/write | Creates a server with the specified parameters or update the properties or tags for the specified server. |

## Microsoft.DBforMySQL

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DBforMySQL/locations/performanceTiers/read | Returns the list of Performance Tiers available. |
> | Action | Microsoft.DBforMySQL/performanceTiers/read | Returns the list of Performance Tiers available. |
> | Action | Microsoft.DBforMySQL/servers/configurations/read | Return the list of configurations for a server or gets the properties for the specified configuration. |
> | Action | Microsoft.DBforMySQL/servers/configurations/write | Update the value for the specified configuration |
> | Action | Microsoft.DBforMySQL/servers/delete | Deletes an existing server. |
> | Action | Microsoft.DBforMySQL/servers/firewallRules/delete | Deletes an existing firewall rule. |
> | Action | Microsoft.DBforMySQL/servers/firewallRules/read | Return the list of firewall rules for a server or gets the properties for the specified firewall rule. |
> | Action | Microsoft.DBforMySQL/servers/firewallRules/write | Creates a firewall rule with the specified parameters or update an existing rule. |
> | Action | Microsoft.DBforMySQL/servers/providers/Microsoft.Insights/diagnosticSettings/read | Gets the disagnostic setting for the resource |
> | Action | Microsoft.DBforMySQL/servers/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.DBforMySQL/servers/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for MySQL servers |
> | Action | Microsoft.DBforMySQL/servers/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for databases |
> | Action | Microsoft.DBforMySQL/servers/read | Return the list of servers or gets the properties for the specified server. |
> | Action | Microsoft.DBforMySQL/servers/recoverableServers/read | Return the recoverable MySQL Server info |
> | Action | Microsoft.DBforMySQL/servers/securityAlertPolicies/read | Retrieve details of the server threat detection policy configured on a given server |
> | Action | Microsoft.DBforMySQL/servers/securityAlertPolicies/write | Change the server threat detection policy for a given server |
> | Action | Microsoft.DBforMySQL/servers/updateConfigurations/action | Update configurations for the specified server |
> | Action | Microsoft.DBforMySQL/servers/virtualNetworkRules/delete | Deletes an existing Virtual Network Rule |
> | Action | Microsoft.DBforMySQL/servers/virtualNetworkRules/read | Return the list of virtual network rules or gets the properties for the specified virtual network rule. |
> | Action | Microsoft.DBforMySQL/servers/virtualNetworkRules/write | Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule. |
> | Action | Microsoft.DBforMySQL/servers/write | Creates a server with the specified parameters or update the properties or tags for the specified server. |

## Microsoft.DBforPostgreSQL

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DBforPostgreSQL/locations/performanceTiers/read | Returns the list of Performance Tiers available. |
> | Action | Microsoft.DBforPostgreSQL/performanceTiers/read | Returns the list of Performance Tiers available. |
> | Action | Microsoft.DBforPostgreSQL/servers/advisors/read | Return the list of advisros |
> | Action | Microsoft.DBforPostgreSQL/servers/advisors/recommendedActions/read | Return the list of recommended actions |
> | Action | Microsoft.DBforPostgreSQL/servers/advisors/recommendedActionSessions/action | Make recommendations |
> | Action | Microsoft.DBforPostgreSQL/servers/configurations/read | Return the list of configurations for a server or gets the properties for the specified configuration. |
> | Action | Microsoft.DBforPostgreSQL/servers/configurations/write | Update the value for the specified configuration |
> | Action | Microsoft.DBforPostgreSQL/servers/delete | Deletes an existing server. |
> | Action | Microsoft.DBforPostgreSQL/servers/firewallRules/delete | Deletes an existing firewall rule. |
> | Action | Microsoft.DBforPostgreSQL/servers/firewallRules/read | Return the list of firewall rules for a server or gets the properties for the specified firewall rule. |
> | Action | Microsoft.DBforPostgreSQL/servers/firewallRules/write | Creates a firewall rule with the specified parameters or update an existing rule. |
> | Action | Microsoft.DBforPostgreSQL/servers/providers/Microsoft.Insights/diagnosticSettings/read | Gets the disagnostic setting for the resource |
> | Action | Microsoft.DBforPostgreSQL/servers/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.DBforPostgreSQL/servers/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Postgres servers |
> | Action | Microsoft.DBforPostgreSQL/servers/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for databases |
> | Action | Microsoft.DBforPostgreSQL/servers/queryTexts/action | Return the text of a query |
> | Action | Microsoft.DBforPostgreSQL/servers/read | Return the list of servers or gets the properties for the specified server. |
> | Action | Microsoft.DBforPostgreSQL/servers/recoverableServers/read | Return the recoverable PostgreSQL Server info |
> | Action | Microsoft.DBforPostgreSQL/servers/securityAlertPolicies/read | Retrieve details of the server threat detection policy configured on a given server |
> | Action | Microsoft.DBforPostgreSQL/servers/securityAlertPolicies/write | Change the server threat detection policy for a given server |
> | Action | Microsoft.DBforPostgreSQL/servers/topQueryStatistics/read | Return the list of Query Statistics for the top queries. |
> | Action | Microsoft.DBforPostgreSQL/servers/updateConfigurations/action | Update configurations for the specified server |
> | Action | Microsoft.DBforPostgreSQL/servers/virtualNetworkRules/delete | Deletes an existing Virtual Network Rule |
> | Action | Microsoft.DBforPostgreSQL/servers/virtualNetworkRules/read | Return the list of virtual network rules or gets the properties for the specified virtual network rule. |
> | Action | Microsoft.DBforPostgreSQL/servers/virtualNetworkRules/write | Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule. |
> | Action | Microsoft.DBforPostgreSQL/servers/waitStatistics/read | Return wait statistics for an instance |
> | Action | Microsoft.DBforPostgreSQL/servers/write | Creates a server with the specified parameters or update the properties or tags for the specified server. |

## Microsoft.Devices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Devices/checkNameAvailability/Action | Check If IotHub name is available |
> | Action | Microsoft.Devices/checkProvisioningServiceNameAvailability/Action | Check If Provisioning service name is available |
> | Action | Microsoft.Devices/ElasticPools/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Devices/ElasticPools/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/certificates/Delete | Deletes Certificate |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/certificates/generateVerificationCode/Action | Generate Verification code |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/certificates/Read | Gets the Certificate |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/certificates/verify/Action | Verify Certificate resource |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/certificates/Write | Create or Update Certificate |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/Delete | Delete the IotHub tenant resource |
> | Action | Microsoft.Devices/ElasticPools/IotHubTenants/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Devices/ElasticPools/IotHubTenants/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/eventHubEndpoints/consumerGroups/Delete | Delete EventHub Consumer Group |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/eventHubEndpoints/consumerGroups/Read | Get EventHub Consumer Group(s) |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/eventHubEndpoints/consumerGroups/Write | Create EventHub Consumer Group |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/exportDevices/Action | Export Devices |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/getStats/Read | Gets the IotHub tenant stats resource |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/importDevices/Action | Import Devices |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/iotHubKeys/listkeys/Action | Gets the IotHub tenant key |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/jobs/Read | Get Job(s) details submitted on given IotHub |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/listKeys/Action | Gets IotHub tenant keys |
> | Action | Microsoft.Devices/ElasticPools/IotHubTenants/logDefinitions/read | Gets the available log definitions for the IotHub Service |
> | Action | Microsoft.Devices/ElasticPools/IotHubTenants/metricDefinitions/read | Gets the available metrics for the IotHub service |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/quotaMetrics/Read | Get Quota Metrics |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/Read | Gets the IotHub tenant resource |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/routing/routes/$testall/Action | Test a message against all existing Routes |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/routing/routes/$testnew/Action | Test a message against a provided test Route |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/routingEndpointsHealth/Read | Gets the health of all routing Endpoints for an IotHub |
> | Action | Microsoft.Devices/elasticPools/iotHubTenants/Write | Create or Update the IotHub tenant resource |
> | Action | Microsoft.Devices/ElasticPools/metricDefinitions/read | Gets the available metrics for the IotHub service |
> | Action | Microsoft.Devices/iotHubs/certificates/Delete | Deletes Certificate |
> | Action | Microsoft.Devices/iotHubs/certificates/generateVerificationCode/Action | Generate Verification code |
> | Action | Microsoft.Devices/iotHubs/certificates/Read | Gets the Certificate |
> | Action | Microsoft.Devices/iotHubs/certificates/verify/Action | Verify Certificate resource |
> | Action | Microsoft.Devices/iotHubs/certificates/Write | Create or Update Certificate |
> | Action | Microsoft.Devices/iotHubs/Delete | Delete IotHub Resource |
> | Action | Microsoft.Devices/IotHubs/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Devices/IotHubs/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Devices/iotHubs/eventGridFilters/Delete | Deletes the Event Grid filter |
> | Action | Microsoft.Devices/iotHubs/eventGridFilters/Read | Gets the Event Grid filter |
> | Action | Microsoft.Devices/iotHubs/eventGridFilters/Write | Create new or Update existing Event Grid filter |
> | Action | Microsoft.Devices/iotHubs/eventHubEndpoints/consumerGroups/Delete | Delete EventHub Consumer Group |
> | Action | Microsoft.Devices/iotHubs/eventHubEndpoints/consumerGroups/Read | Get EventHub Consumer Group(s) |
> | Action | Microsoft.Devices/iotHubs/eventHubEndpoints/consumerGroups/Write | Create EventHub Consumer Group |
> | Action | Microsoft.Devices/iotHubs/exportDevices/Action | Export Devices |
> | Action | Microsoft.Devices/iotHubs/importDevices/Action | Import Devices |
> | Action | Microsoft.Devices/iotHubs/iotHubKeys/listkeys/Action | Get IotHub Key for the given name |
> | Action | Microsoft.Devices/iotHubs/iotHubStats/Read | Get IotHub Statistics |
> | Action | Microsoft.Devices/iotHubs/jobs/Read | Get Job(s) details submitted on given IotHub |
> | Action | Microsoft.Devices/iotHubs/listkeys/Action | Get all IotHub Keys |
> | Action | Microsoft.Devices/IotHubs/logDefinitions/read | Gets the available log definitions for the IotHub Service |
> | Action | Microsoft.Devices/IotHubs/metricDefinitions/read | Gets the available metrics for the IotHub service |
> | Action | Microsoft.Devices/iotHubs/operationresults/Read | Get Operation Result (Obsolete API) |
> | Action | Microsoft.Devices/iotHubs/quotaMetrics/Read | Get Quota Metrics |
> | Action | Microsoft.Devices/iotHubs/Read | Gets the IotHub resource(s) |
> | Action | Microsoft.Devices/iotHubs/routing/$testall/Action | Test a message against all existing Routes |
> | Action | Microsoft.Devices/iotHubs/routing/$testnew/Action | Test a message against a provided test Route |
> | Action | Microsoft.Devices/iotHubs/routingEndpointsHealth/Read | Gets the health of all routing Endpoints for an IotHub |
> | Action | Microsoft.Devices/iotHubs/skus/Read | Get valid IotHub Skus |
> | Action | Microsoft.Devices/iotHubs/Write | Create or update IotHub Resource |
> | Action | Microsoft.Devices/locations/operationresults/Read | Get Location based Operation Result |
> | Action | Microsoft.Devices/operationresults/Read | Get Operation Result |
> | Action | Microsoft.Devices/operations/Read | Get All ResourceProvider Operations |
> | Action | Microsoft.Devices/provisioningServices/certificates/Delete | Deletes Certificate |
> | Action | Microsoft.Devices/provisioningServices/certificates/generateVerificationCode/Action | Generate Verification code |
> | Action | Microsoft.Devices/provisioningServices/certificates/Read | Gets the Certificate |
> | Action | Microsoft.Devices/provisioningServices/certificates/verify/Action | Verify Certificate resource |
> | Action | Microsoft.Devices/provisioningServices/certificates/Write | Create or Update Certificate |
> | Action | Microsoft.Devices/provisioningServices/Delete | Delete IotDps resource |
> | Action | Microsoft.Devices/provisioningServices/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Devices/provisioningServices/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Devices/provisioningServices/keys/listkeys/Action | Get IotDps Keys for key name |
> | Action | Microsoft.Devices/provisioningServices/listkeys/Action | Get all IotDps keys |
> | Action | Microsoft.Devices/provisioningServices/logDefinitions/read | Gets the available log definitions for the provisioning Service |
> | Action | Microsoft.Devices/provisioningServices/metricDefinitions/read | Gets the available metrics for the provisioning service |
> | Action | Microsoft.Devices/provisioningServices/operationresults/Read | Get DPS Operation Result |
> | Action | Microsoft.Devices/provisioningServices/Read | Get IotDps resource |
> | Action | Microsoft.Devices/provisioningServices/skus/Read | Get valid IotDps Skus |
> | Action | Microsoft.Devices/provisioningServices/Write | Create IotDps resource |
> | Action | Microsoft.Devices/register/action | Register the subscription for the IotHub resource provider and enables the creation of IotHub resources |
> | Action | Microsoft.Devices/register/action | Register the subscription for the IotHub resource provider and enables the creation of IotHub resources |
> | Action | Microsoft.Devices/usages/Read | Get subscription usage details for this provider. |

## Microsoft.DevTestLab

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DevTestLab/labCenters/delete | Delete lab centers. |
> | Action | Microsoft.DevTestLab/labCenters/read | Read lab centers. |
> | Action | Microsoft.DevTestLab/labCenters/write | Add or modify lab centers. |
> | Action | Microsoft.DevTestLab/labs/artifactSources/armTemplates/read | Read azure resource manager templates. |
> | Action | Microsoft.DevTestLab/labs/artifactSources/artifacts/GenerateArmTemplate/action | Generates an ARM template for the given artifact, uploads the required files to a storage account, and validates the generated artifact. |
> | Action | Microsoft.DevTestLab/labs/artifactSources/artifacts/read | Read artifacts. |
> | Action | Microsoft.DevTestLab/labs/artifactSources/delete | Delete artifact sources. |
> | Action | Microsoft.DevTestLab/labs/artifactSources/read | Read artifact sources. |
> | Action | Microsoft.DevTestLab/labs/artifactSources/write | Add or modify artifact sources. |
> | Action | Microsoft.DevTestLab/labs/ClaimAnyVm/action | Claim a random claimable virtual machine in the lab. |
> | Action | Microsoft.DevTestLab/labs/costs/read | Read costs. |
> | Action | Microsoft.DevTestLab/labs/costs/write | Add or modify costs. |
> | Action | Microsoft.DevTestLab/labs/CreateEnvironment/action | Create virtual machines in a lab. |
> | Action | Microsoft.DevTestLab/labs/customImages/delete | Delete custom images. |
> | Action | Microsoft.DevTestLab/labs/customImages/read | Read custom images. |
> | Action | Microsoft.DevTestLab/labs/customImages/write | Add or modify custom images. |
> | Action | Microsoft.DevTestLab/labs/delete | Delete labs. |
> | Action | Microsoft.DevTestLab/labs/ExportResourceUsage/action | Exports the lab resource usage into a storage account |
> | Action | Microsoft.DevTestLab/labs/formulas/delete | Delete formulas. |
> | Action | Microsoft.DevTestLab/labs/formulas/read | Read formulas. |
> | Action | Microsoft.DevTestLab/labs/formulas/write | Add or modify formulas. |
> | Action | Microsoft.DevTestLab/labs/galleryImages/read | Read gallery images. |
> | Action | Microsoft.DevTestLab/labs/GenerateUploadUri/action | Generate a URI for uploading custom disk images to a Lab. |
> | Action | Microsoft.DevTestLab/labs/ImportVirtualMachine/action | Import a virtual machine into a different lab. |
> | Action | Microsoft.DevTestLab/labs/ListVhds/action | List disk images available for custom image creation. |
> | Action | Microsoft.DevTestLab/labs/notificationChannels/delete | Delete notificationchannels. |
> | Action | Microsoft.DevTestLab/labs/notificationChannels/Notify/action | Send notification to provided channel. |
> | Action | Microsoft.DevTestLab/labs/notificationChannels/read | Read notificationchannels. |
> | Action | Microsoft.DevTestLab/labs/notificationChannels/write | Add or modify notificationchannels. |
> | Action | Microsoft.DevTestLab/labs/policySets/EvaluatePolicies/action | Evaluates lab policy. |
> | Action | Microsoft.DevTestLab/labs/policySets/policies/delete | Delete policies. |
> | Action | Microsoft.DevTestLab/labs/policySets/policies/read | Read policies. |
> | Action | Microsoft.DevTestLab/labs/policySets/policies/write | Add or modify policies. |
> | Action | Microsoft.DevTestLab/labs/read | Read labs. |
> | Action | Microsoft.DevTestLab/labs/schedules/delete | Delete schedules. |
> | Action | Microsoft.DevTestLab/labs/schedules/Execute/action | Execute a schedule. |
> | Action | Microsoft.DevTestLab/labs/schedules/ListApplicable/action | Lists all applicable schedules |
> | Action | Microsoft.DevTestLab/labs/schedules/read | Read schedules. |
> | Action | Microsoft.DevTestLab/labs/schedules/write | Add or modify schedules. |
> | Action | Microsoft.DevTestLab/labs/serviceRunners/delete | Delete service runners. |
> | Action | Microsoft.DevTestLab/labs/serviceRunners/read | Read service runners. |
> | Action | Microsoft.DevTestLab/labs/serviceRunners/write | Add or modify service runners. |
> | Action | Microsoft.DevTestLab/labs/users/delete | Delete user profiles. |
> | Action | Microsoft.DevTestLab/labs/users/disks/Attach/action | Attach and create the lease of the disk to the virtual machine. |
> | Action | Microsoft.DevTestLab/labs/users/disks/delete | Delete disks. |
> | Action | Microsoft.DevTestLab/labs/users/disks/Detach/action | Detach and break the lease of the disk attached to the virtual machine. |
> | Action | Microsoft.DevTestLab/labs/users/disks/read | Read disks. |
> | Action | Microsoft.DevTestLab/labs/users/disks/write | Add or modify disks. |
> | Action | Microsoft.DevTestLab/labs/users/environments/delete | Delete environments. |
> | Action | Microsoft.DevTestLab/labs/users/environments/read | Read environments. |
> | Action | Microsoft.DevTestLab/labs/users/environments/write | Add or modify environments. |
> | Action | Microsoft.DevTestLab/labs/users/read | Read user profiles. |
> | Action | Microsoft.DevTestLab/labs/users/secrets/delete | Delete secrets. |
> | Action | Microsoft.DevTestLab/labs/users/secrets/read | Read secrets. |
> | Action | Microsoft.DevTestLab/labs/users/secrets/write | Add or modify secrets. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/delete | Delete service fabrics. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/ListApplicableSchedules/action | Lists the applicable start/stop schedules, if any. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/read | Read service fabrics. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/schedules/delete | Delete schedules. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/schedules/Execute/action | Execute a schedule. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/schedules/read | Read schedules. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/schedules/write | Add or modify schedules. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/Start/action | Start a service fabric. |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/Stop/action | Stop a service fabric |
> | Action | Microsoft.DevTestLab/labs/users/serviceFabrics/write | Add or modify service fabrics. |
> | Action | Microsoft.DevTestLab/labs/users/write | Add or modify user profiles. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/AddDataDisk/action | Attach a new or existing data disk to virtual machine. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/ApplyArtifacts/action | Apply artifacts to virtual machine. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/Claim/action | Take ownership of an existing virtual machine |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/delete | Delete virtual machines. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/DetachDataDisk/action | Detach the specified disk from the virtual machine. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/GetRdpFileContents/action | Gets a string that represents the contents of the RDP file for the virtual machine |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/ListApplicableSchedules/action | Lists the applicable start/stop schedules, if any. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/read | Read virtual machines. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/Redeploy/action | Redeploy a virtual machine |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/Resize/action | Resize Virtual Machine. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/Restart/action | Restart a virtual machine. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/schedules/delete | Delete schedules. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/schedules/Execute/action | Execute a schedule. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/schedules/read | Read schedules. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/schedules/write | Add or modify schedules. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/Start/action | Start a virtual machine. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/Stop/action | Stop a virtual machine |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/TransferDisks/action | Transfers all data disks attached to the virtual machine to be owned by the current user. |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/UnClaim/action | Release ownership of an existing virtual machine |
> | Action | Microsoft.DevTestLab/labs/virtualMachines/write | Add or modify virtual machines. |
> | Action | Microsoft.DevTestLab/labs/virtualNetworks/delete | Delete virtual networks. |
> | Action | Microsoft.DevTestLab/labs/virtualNetworks/read | Read virtual networks. |
> | Action | Microsoft.DevTestLab/labs/virtualNetworks/write | Add or modify virtual networks. |
> | Action | Microsoft.DevTestLab/labs/vmPools/delete | Delete virtual machine pools. |
> | Action | Microsoft.DevTestLab/labs/vmPools/read | Read virtual machine pools. |
> | Action | Microsoft.DevTestLab/labs/vmPools/write | Add or modify virtual machine pools. |
> | Action | Microsoft.DevTestLab/labs/write | Add or modify labs. |
> | Action | Microsoft.DevTestLab/locations/operations/read | Read operations. |
> | Action | Microsoft.DevTestLab/register/action | Registers the subscription |
> | Action | Microsoft.DevTestLab/schedules/delete | Delete schedules. |
> | Action | Microsoft.DevTestLab/schedules/Execute/action | Execute a schedule. |
> | Action | Microsoft.DevTestLab/schedules/read | Read schedules. |
> | Action | Microsoft.DevTestLab/schedules/Retarget/action | Updates a schedule's target resource Id. |
> | Action | Microsoft.DevTestLab/schedules/write | Add or modify schedules. |

## Microsoft.DocumentDB

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DocumentDB/databaseAccountNames/read | Checks for name availability. |
> | Action | Microsoft.DocumentDB/databaseAccounts/changeResourceGroup/action | Change resource group of a database account |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/metricDefinitions/read | Reads the collection metric definitions. |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/metrics/read | Reads the collection metrics. |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/partitionKeyRangeId/metrics/read | Read database account partition key level metrics |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/partitions/metrics/read | Read database account partition level metrics |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/partitions/read | Read database account partitions in a collection |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/partitions/usages/read | Read database account partition level usages |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/collections/usages/read | Reads the collection usages. |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/metricDefinitions/read | Reads the database metric definitions |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/metrics/read | Reads the database metrics. |
> | Action | Microsoft.DocumentDB/databaseAccounts/databases/usages/read | Reads the database usages. |
> | Action | Microsoft.DocumentDB/databaseAccounts/delete | Deletes the database accounts. |
> | Action | Microsoft.DocumentDB/databaseAccounts/failoverPriorityChange/action | Change failover priorities of regions of a database account. This is used to perform manual failover operation |
> | Action | Microsoft.DocumentDB/databaseAccounts/listConnectionStrings/action | Get the connection strings for a database account |
> | Action | Microsoft.DocumentDB/databaseAccounts/listKeys/action | List keys of a database account |
> | Action | Microsoft.DocumentDB/databaseAccounts/metricDefinitions/read | Reads the database account metrics definitions. |
> | Action | Microsoft.DocumentDB/databaseAccounts/metrics/read | Reads the database account metrics. |
> | Action | Microsoft.DocumentDB/databaseAccounts/offlineRegion/action | Offline a region of a database account.  |
> | Action | Microsoft.DocumentDB/databaseAccounts/onlineRegion/action | Online a region of a database account. |
> | Action | Microsoft.DocumentDB/databaseAccounts/operationResults/read | Read status of the asynchronous operation |
> | Action | Microsoft.DocumentDB/databaseAccounts/percentile/metrics/read | Read latency metrics |
> | Action | Microsoft.DocumentDB/databaseAccounts/percentile/read | Read percentiles of replication latencies |
> | Action | Microsoft.DocumentDB/databaseAccounts/percentile/sourceRegion/targetRegion/metrics/read | Read latency metrics for a specific source and target region |
> | Action | Microsoft.DocumentDB/databaseAccounts/percentile/targetRegion/metrics/read | Read latency metrics for a specific target region |
> | Action | Microsoft.DocumentDB/databaseAccounts/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.DocumentDB/databaseAccounts/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.DocumentDB/databaseAccounts/providers/Microsoft.Insights/logDefinitions/read | Gets the available log catageries for Database Account |
> | Action | Microsoft.DocumentDB/databaseAccounts/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for the database Account |
> | Action | Microsoft.DocumentDB/databaseAccounts/read | Reads a database account. |
> | Action | Microsoft.DocumentDB/databaseAccounts/readonlykeys/action | Reads the database account readonly keys. |
> | Action | Microsoft.DocumentDB/databaseAccounts/readonlykeys/read | Reads the database account readonly keys. |
> | Action | Microsoft.DocumentDB/databaseAccounts/regenerateKey/action | Rotate keys of a database account |
> | Action | Microsoft.DocumentDB/databaseAccounts/region/databases/collections/metrics/read | Reads the regional collection metrics. |
> | Action | Microsoft.DocumentDB/databaseAccounts/region/databases/collections/partitionKeyRangeId/metrics/read | Read regional database account partition key level metrics |
> | Action | Microsoft.DocumentDB/databaseAccounts/region/databases/collections/partitions/metrics/read | Read regional database account partition level metrics |
> | Action | Microsoft.DocumentDB/databaseAccounts/region/databases/collections/partitions/read | Read regional database account partitions in a collection |
> | Action | Microsoft.DocumentDB/databaseAccounts/region/metrics/read | Reads the region and database account metrics. |
> | Action | Microsoft.DocumentDB/databaseAccounts/usages/read | Reads the database account usages. |
> | Action | Microsoft.DocumentDB/databaseAccounts/write | Update a database accounts. |
> | Action | Microsoft.DocumentDB/locations/deleteVirtualNetworkOrSubnets/action | Notifies Microsoft.DocumentDB that VirtualNetwork or Subnet is being deleted |
> | Action | Microsoft.DocumentDB/locations/deleteVirtualNetworkOrSubnets/operationResults/read | Read Status of deleteVirtualNetworkOrSubnets asynchronous operation |
> | Action | Microsoft.DocumentDB/operationResults/read | Read status of the asynchronous operation |
> | Action | Microsoft.DocumentDB/operations/read | Read operations available for the Microsoft DocumentDB  |
> | Action | Microsoft.DocumentDB/register/action |  Register the Microsoft DocumentDB resource provider for the subscription |

## Microsoft.DomainRegistration

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DomainRegistration/checkDomainAvailability/Action | Check if a domain is available for purchase |
> | Action | Microsoft.DomainRegistration/domains/Delete | Delete an existing domain. |
> | Action | Microsoft.DomainRegistration/domains/domainownershipidentifiers/Delete | Delete ownership identifier |
> | Action | Microsoft.DomainRegistration/domains/domainownershipidentifiers/Read | List ownership identifiers |
> | Action | Microsoft.DomainRegistration/domains/domainownershipidentifiers/Read | Get ownership identifier |
> | Action | Microsoft.DomainRegistration/domains/domainownershipidentifiers/Write | Create or update identifier |
> | Action | Microsoft.DomainRegistration/domains/operationresults/Read | Get a domain operation |
> | Action | Microsoft.DomainRegistration/domains/Read | Get the list of domains |
> | Action | Microsoft.DomainRegistration/domains/Read | Get domain |
> | Action | Microsoft.DomainRegistration/domains/renew/Action | Renew an existing domain. |
> | Action | Microsoft.DomainRegistration/domains/Write | Add a new Domain or update an existing one |
> | Action | Microsoft.DomainRegistration/generateSsoRequest/Action | Generate a request for signing into domain control center. |
> | Action | Microsoft.DomainRegistration/listDomainRecommendations/Action | Retrieve the list domain recommendations based on keywords |
> | Action | Microsoft.DomainRegistration/operations/Read | List all operations from app service domain registration |
> | Action | Microsoft.DomainRegistration/register/action | Register the Microsoft Domains resource provider for the subscription |
> | Action | Microsoft.DomainRegistration/topLevelDomains/listAgreements/Action | List Agreement action |
> | Action | Microsoft.DomainRegistration/topLevelDomains/Read | Get toplevel domains |
> | Action | Microsoft.DomainRegistration/topLevelDomains/Read | Get toplevel domain |
> | Action | Microsoft.DomainRegistration/validateDomainRegistrationInformation/Action | Validate domain purchase object without submitting it |

## Microsoft.DynamicsLcs

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.DynamicsLcs/lcsprojects/clouddeployments/read | Display Microsoft Dynamics AX 2012 R3 Evaluation deployments in a Microsoft Dynamics Lifecycle Services project that belong to a user |
> | Action | Microsoft.DynamicsLcs/lcsprojects/clouddeployments/write | Create Microsoft Dynamics AX 2012 R3 Evaluation deployment in a Microsoft Dynamics Lifecycle Services project that belong to a user. Deployments can be managed from Azure management portal |
> | Action | Microsoft.DynamicsLcs/lcsprojects/connectors/read | Read connectors that belong to a Microsoft Dynamics Lifecycle Services project |
> | Action | Microsoft.DynamicsLcs/lcsprojects/connectors/write | Create and update connectors that belong to a Microsoft Dynamics Lifecycle Services project |
> | Action | Microsoft.DynamicsLcs/lcsprojects/delete | Delete Microsoft Dynamics Lifecycle Services projects that belong to the user |
> | Action | Microsoft.DynamicsLcs/lcsprojects/read | Display Microsoft Dynamics Lifecycle Services projects that belong to a user |
> | Action | Microsoft.DynamicsLcs/lcsprojects/write | Create and update Microsoft Dynamics Lifecycle Services projects that belong to the user. Only the name and description properties can be updated. The subscription and location associated with the project cannot be updated after creation |

## Microsoft.EventGrid

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.EventGrid/domains/delete | Delete a domain |
> | Action | Microsoft.EventGrid/domains/listKeys/action | List keys for a domain |
> | Action | Microsoft.EventGrid/domains/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for domains |
> | Action | Microsoft.EventGrid/domains/read | Read a domain |
> | Action | Microsoft.EventGrid/domains/regenerateKey/action | Regenerate key for a domain |
> | Action | Microsoft.EventGrid/domains/topics/read | Read a domain topic |
> | Action | Microsoft.EventGrid/domains/write | Create or update a domain |
> | Action | Microsoft.EventGrid/eventSubscriptions/delete | Delete a eventSubscription |
> | Action | Microsoft.EventGrid/eventSubscriptions/getFullUrl/action | Get full url for the event subscription |
> | Action | Microsoft.EventGrid/eventSubscriptions/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for event subscriptions |
> | Action | Microsoft.EventGrid/eventSubscriptions/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for event subscriptions |
> | Action | Microsoft.EventGrid/eventSubscriptions/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for eventSubscriptions |
> | Action | Microsoft.EventGrid/eventSubscriptions/read | Read a eventSubscription |
> | Action | Microsoft.EventGrid/eventSubscriptions/write | Create or update a eventSubscription |
> | Action | Microsoft.EventGrid/extensionTopics/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for topics |
> | Action | Microsoft.EventGrid/extensionTopics/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for topics |
> | Action | Microsoft.EventGrid/extensionTopics/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for topics |
> | Action | Microsoft.EventGrid/locations/operationResults/read | Read the result of a regional operation |
> | Action | Microsoft.EventGrid/locations/operationsStatus/read | Read the status of a regional operation |
> | Action | Microsoft.EventGrid/operationResults/read | Read the result of an operation |
> | Action | Microsoft.EventGrid/operationsStatus/read | Read the status of an operation |
> | Action | Microsoft.EventGrid/register/action | Registers the subscription for the EventGrid resource provider. |
> | Action | Microsoft.EventGrid/topics/delete | Delete a topic |
> | Action | Microsoft.EventGrid/topics/listKeys/action | List keys for a topic |
> | Action | Microsoft.EventGrid/topics/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for topics |
> | Action | Microsoft.EventGrid/topics/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for topics |
> | Action | Microsoft.EventGrid/topics/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for topics |
> | Action | Microsoft.EventGrid/topics/read | Read a topic |
> | Action | Microsoft.EventGrid/topics/regenerateKey/action | Regenerate key for a topic |
> | Action | Microsoft.EventGrid/topics/write | Create or update a topic |
> | Action | Microsoft.EventGrid/topictypes/eventtypes/read | Read eventtypes supported by a topictype |
> | Action | Microsoft.EventGrid/topictypes/read | Read a topictype |

## Microsoft.EventHub

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.EventHub/checkNameAvailability/action | Checks availability of namespace under given subscription. |
> | Action | Microsoft.EventHub/checkNamespaceAvailability/action | Checks availability of namespace under given subscription. This API is deprecated please use CheckNameAvailabiltiy instead. |
> | Action | Microsoft.EventHub/clusters/providers/Microsoft.Insights/metricDefinitions/read | Get list of Cluster metrics Resource Descriptions |
> | Action | Microsoft.EventHub/clusters/read | Gets the Cluster Resource Description |
> | Action | Microsoft.EventHub/clusters/write | Gets the Cluster Resource Description |
> | Action | Microsoft.EventHub/namespaces/authorizationRules/action | Updates Namespace Authorization Rule. This API is depricated. Please use a PUT call to update the Namespace Authorization Rule instead.. This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.EventHub/namespaces/authorizationRules/delete | Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted.  |
> | Action | Microsoft.EventHub/namespaces/authorizationRules/listkeys/action | Get the Connection String to the Namespace |
> | Action | Microsoft.EventHub/namespaces/authorizationRules/read | Get the list of Namespaces Authorization Rules description. |
> | Action | Microsoft.EventHub/namespaces/authorizationRules/regenerateKeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.EventHub/namespaces/authorizationRules/write | Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated. |
> | Action | Microsoft.EventHub/namespaces/Delete | Delete Namespace Resource |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/authorizationRules/listkeys/action | Gets the authorization rules keys for the Disaster Recovery primary namespace |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/authorizationRules/read | Get Disaster Recovery Primary Namespace's Authorization Rules |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/breakPairing/action | Disables Disaster Recovery and stops replicating changes from primary to secondary namespaces. |
> | Action | Microsoft.EventHub/namespaces/disasterrecoveryconfigs/checkNameAvailability/action | Checks availability of namespace alias under given subscription. |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/delete | Deletes the Disaster Recovery configuration associated with the namespace. This operation can only be invoked via the primary namespace. |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/failover/action | Invokes a GEO DR failover and reconfigures the namespace alias to point to the secondary namespace. |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/read | Gets the Disaster Recovery configuration associated with the namespace. |
> | Action | Microsoft.EventHub/namespaces/disasterRecoveryConfigs/write | Creates or Updates the Disaster Recovery configuration associated with the namespace. |
> | Action | Microsoft.EventHub/namespaces/eventhubs/authorizationRules/action | Operation to update EventHub. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule. |
> | Action | Microsoft.EventHub/namespaces/eventhubs/authorizationRules/delete | Operation to delete EventHub Authorization Rules |
> | Action | Microsoft.EventHub/namespaces/eventhubs/authorizationRules/listkeys/action | Get the Connection String to EventHub |
> | Action | Microsoft.EventHub/namespaces/eventhubs/authorizationRules/read |  Get the list of EventHub Authorization Rules |
> | Action | Microsoft.EventHub/namespaces/eventhubs/authorizationRules/regenerateKeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.EventHub/namespaces/eventhubs/authorizationRules/write | Create EventHub Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated. |
> | Action | Microsoft.EventHub/namespaces/eventHubs/consumergroups/Delete | Operation to delete ConsumerGroup Resource |
> | Action | Microsoft.EventHub/namespaces/eventHubs/consumergroups/read | Get list of ConsumerGroup Resource Descriptions |
> | Action | Microsoft.EventHub/namespaces/eventHubs/consumergroups/write | Create or Update ConsumerGroup properties. |
> | Action | Microsoft.EventHub/namespaces/eventhubs/Delete | Operation to delete EventHub Resource |
> | Action | Microsoft.EventHub/namespaces/eventhubs/read | Get list of EventHub Resource Descriptions |
> | Action | Microsoft.EventHub/namespaces/eventhubs/write | Create or Update EventHub properties. |
> | Action | Microsoft.EventHub/namespaces/messagingPlan/read | Gets the Messaging Plan for a namespace.<br>This API is deprecated.<br>Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions..<br>This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.EventHub/namespaces/messagingPlan/write | Updates the Messaging Plan for a namespace.<br>This API is deprecated.<br>Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions..<br>This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.EventHub/namespaces/operationresults/read | Get the status of Namespace operation |
> | Action | Microsoft.EventHub/namespaces/providers/Microsoft.Insights/diagnosticSettings/read | Get list of Namespace diagnostic settings Resource Descriptions |
> | Action | Microsoft.EventHub/namespaces/providers/Microsoft.Insights/diagnosticSettings/write | Get list of Namespace diagnostic settings Resource Descriptions |
> | Action | Microsoft.EventHub/namespaces/providers/Microsoft.Insights/logDefinitions/read | Get list of Namespace logs Resource Descriptions |
> | Action | Microsoft.EventHub/namespaces/providers/Microsoft.Insights/metricDefinitions/read | Get list of Namespace metrics Resource Descriptions |
> | Action | Microsoft.EventHub/namespaces/read | Get the list of Namespace Resource Description |
> | Action | Microsoft.EventHub/namespaces/removeAcsNamepsace/action | Remove ACS namespace |
> | Action | Microsoft.EventHub/namespaces/write | Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated. |
> | Action | Microsoft.EventHub/operations/read | Get Operations |
> | Action | Microsoft.EventHub/register/action | Registers the subscription for the EventHub resource provider and enables the creation of EventHub resources |
> | Action | Microsoft.EventHub/sku/read | Get list of Sku Resource Descriptions |
> | Action | Microsoft.EventHub/sku/regions/read | Get list of SkuRegions Resource Descriptions |
> | Action | Microsoft.EventHub/unregister/action | Registers the EventHub Resource Provider |

## Microsoft.Features

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Features/features/read | Gets the features of a subscription. |
> | Action | Microsoft.Features/operations/read | Gets the list of operations. |
> | Action | Microsoft.Features/providers/features/read | Gets the feature of a subscription in a given resource provider. |
> | Action | Microsoft.Features/providers/features/register/action | Registers the feature for a subscription in a given resource provider. |
> | Action | Microsoft.Features/providers/features/unregister/action | Unregisters the feature for a subscription in a given resource provider. |
> | Action | Microsoft.Features/register/action | Registers the feature of a subscription. |

## Microsoft.GuestConfiguration

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.GuestConfiguration/guestConfigurationAssignments/read | Get guest configuration assignment. |
> | Action | Microsoft.GuestConfiguration/guestConfigurationAssignments/write | Create new guest configuration assignment. |

## Microsoft.HDInsight

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.HDInsight/clusters/applications/delete | Delete Application for HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/applications/read | Get Application for HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/applications/write | Create or Update Application for HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/changerdpsetting/action | Change RDP setting for HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/configurations/action | Update HDInsight Cluster Configuration |
> | Action | Microsoft.HDInsight/clusters/configurations/read | Get HDInsight Cluster Configurations |
> | Action | Microsoft.HDInsight/clusters/delete | Delete a HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/read | Get details about HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/roles/resize/action | Resize a HDInsight Cluster |
> | Action | Microsoft.HDInsight/clusters/write | Create or Update HDInsight Cluster |
> | Action | Microsoft.HDInsight/locations/capabilities/read | Get Subscription Capabilities |
> | Action | Microsoft.HDInsight/locations/checkNameAvailability/read | Check Name Availability |

## Microsoft.ImportExport

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ImportExport/jobs/delete | Deletes an existing job. |
> | Action | Microsoft.ImportExport/jobs/listBitLockerKeys/action | Gets the BitLocker keys for the specified job. |
> | Action | Microsoft.ImportExport/jobs/read | Gets the properties for the specified job or returns the list of jobs. |
> | Action | Microsoft.ImportExport/jobs/write | Creates a job with the specified parameters or update the properties or tags for the specified job. |
> | Action | Microsoft.ImportExport/locations/read | Gets the properties for the specified location or returns the list of locations. |
> | Action | Microsoft.ImportExport/register/action | Registers the subscription for the import/export resource provider and enables the creation of import/export jobs. |

## Microsoft.Insights

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Insights/ActionGroups/Delete | Delete an action group |
> | Action | Microsoft.Insights/ActionGroups/Read | Read an action group |
> | Action | Microsoft.Insights/ActionGroups/Write | Create or update an action group |
> | Action | Microsoft.Insights/ActivityLogAlerts/Activated/Action | Activity Log Alert activated |
> | Action | Microsoft.Insights/ActivityLogAlerts/Delete | Delete an activity log alert |
> | Action | Microsoft.Insights/ActivityLogAlerts/Read | Read an activity log alert |
> | Action | Microsoft.Insights/ActivityLogAlerts/Write | Create or update an activity log alert |
> | Action | Microsoft.Insights/AlertRules/Activated/Action | Classic metric alert activated |
> | Action | Microsoft.Insights/AlertRules/Delete | Delete a classic metric alert |
> | Action | Microsoft.Insights/AlertRules/Incidents/Read | Read a classic metric alert incident |
> | Action | Microsoft.Insights/AlertRules/Read | Read a classic metric alert |
> | Action | Microsoft.Insights/AlertRules/Resolved/Action | Classic metric alert resolved |
> | Action | Microsoft.Insights/AlertRules/Throttled/Action | Classic metric alert rule throttled |
> | Action | Microsoft.Insights/AlertRules/Write | Create or update a classic metric alert |
> | Action | Microsoft.Insights/AutoscaleSettings/Delete | Delete an autoscale setting |
> | Action | Microsoft.Insights/AutoscaleSettings/providers/Microsoft.Insights/diagnosticSettings/Read | Read a resource diagnostic setting |
> | Action | Microsoft.Insights/AutoscaleSettings/providers/Microsoft.Insights/diagnosticSettings/Write | Create or update a resource diagnostic setting |
> | Action | Microsoft.Insights/AutoscaleSettings/providers/Microsoft.Insights/logDefinitions/Read | Read log definitions |
> | Action | Microsoft.Insights/AutoscaleSettings/providers/Microsoft.Insights/MetricDefinitions/Read | Read metric definitions |
> | Action | Microsoft.Insights/AutoscaleSettings/Read | Read an autoscale setting |
> | Action | Microsoft.Insights/AutoscaleSettings/Scaledown/Action | Autoscale scale down initiated |
> | Action | Microsoft.Insights/AutoscaleSettings/ScaledownResult/Action | Autoscale scale down completed |
> | Action | Microsoft.Insights/AutoscaleSettings/Scaleup/Action | Autoscale scale up initiated |
> | Action | Microsoft.Insights/AutoscaleSettings/ScaleupResult/Action | Autoscale scale up completed |
> | Action | Microsoft.Insights/AutoscaleSettings/Write | Create or update an autoscale setting |
> | Action | Microsoft.Insights/Components/AnalyticsItems/Delete | Deleting an Application Insights analytics item |
> | Action | Microsoft.Insights/Components/AnalyticsItems/Read | Reading an Application Insights analytics item |
> | Action | Microsoft.Insights/Components/AnalyticsItems/Write | Writing an Application Insights analytics item |
> | Action | Microsoft.Insights/Components/AnalyticsTables/Action | Application Insights analytics table action |
> | Action | Microsoft.Insights/Components/AnalyticsTables/Delete | Deleting an Application Insights analytics table schema |
> | Action | Microsoft.Insights/Components/AnalyticsTables/Read | Reading an Application Insights analytics table schema |
> | Action | Microsoft.Insights/Components/AnalyticsTables/Write | Writing an Application Insights analytics table schema |
> | Action | Microsoft.Insights/Components/Annotations/Delete | Deleting an Application Insights annotation |
> | Action | Microsoft.Insights/Components/Annotations/Read | Reading an Application Insights annotation |
> | Action | Microsoft.Insights/Components/Annotations/Write | Writing an Application Insights annotation |
> | Action | Microsoft.Insights/Components/Api/Read | Reading Application Insights component data API |
> | Action | Microsoft.Insights/Components/ApiKeys/Action | Generating an Application Insights API key |
> | Action | Microsoft.Insights/Components/ApiKeys/Delete | Deleting an Application Insights API key |
> | Action | Microsoft.Insights/Components/ApiKeys/Read | Reading an Application Insights API key |
> | Action | Microsoft.Insights/Components/BillingPlanForComponent/Read | Reading a billing plan for Application Insights component |
> | Action | Microsoft.Insights/Components/CurrentBillingFeatures/Read | Reading current billing features for Application Insights component |
> | Action | Microsoft.Insights/Components/CurrentBillingFeatures/Write | Writing current billing features for Application Insights component |
> | Action | Microsoft.Insights/Components/DefaultWorkItemConfig/Read | Reading an Application Insights default ALM integration configuration |
> | Action | Microsoft.Insights/Components/Delete | Deleting an application insights component configuration |
> | Action | Microsoft.Insights/Components/Events/Read | Get logs from Application Insights using OData query format |
> | Action | Microsoft.Insights/Components/ExportConfiguration/Action | Application Insights export settings action |
> | Action | Microsoft.Insights/Components/ExportConfiguration/Delete | Deleting Application Insights export settings |
> | Action | Microsoft.Insights/Components/ExportConfiguration/Read | Reading Application Insights export settings |
> | Action | Microsoft.Insights/Components/ExportConfiguration/Write | Writing Application Insights export settings |
> | Action | Microsoft.Insights/Components/ExtendQueries/Read | Reading Application Insights component extended query results |
> | Action | Microsoft.Insights/Components/Favorites/Delete | Deleting an Application Insights favorite |
> | Action | Microsoft.Insights/Components/Favorites/Read | Reading an Application Insights favorite |
> | Action | Microsoft.Insights/Components/Favorites/Write | Writing an Application Insights favorite |
> | Action | Microsoft.Insights/Components/FeatureCapabilities/Read | Reading Application Insights component feature capabilities |
> | Action | Microsoft.Insights/Components/GetAvailableBillingFeatures/Read | Reading Application Insights component available billing features |
> | Action | Microsoft.Insights/Components/GetToken/Read | Reading an Application Insights component token |
> | Action | Microsoft.Insights/Components/MetricDefinitions/Read | Reading Application Insights component metric definitions |
> | Action | Microsoft.Insights/Components/Metrics/Read | Reading Application Insights component metrics |
> | Action | Microsoft.Insights/Components/Move/Action | Move an Application Insights Component to another resource group or subscription |
> | Action | Microsoft.Insights/Components/MyAnalyticsItems/Delete | Deleting an Application Insights personal analytics item |
> | Action | Microsoft.Insights/Components/MyAnalyticsItems/Read | Reading an Application Insights personal analytics item |
> | Action | Microsoft.Insights/Components/MyAnalyticsItems/Write | Writing an Application Insights personal analytics item |
> | Action | Microsoft.Insights/Components/MyFavorites/Read | Reading an Application Insights personal favorite |
> | Action | Microsoft.Insights/Components/Operations/Read | Get status of long-running operations in Application Insights |
> | Action | Microsoft.Insights/Components/PricingPlans/Read | Reading an Application Insights component pricing plan |
> | Action | Microsoft.Insights/Components/PricingPlans/Write | Writing an Application Insights component pricing plan |
> | Action | Microsoft.Insights/Components/ProactiveDetectionConfigs/Read | Reading Application Insights proactive detection configuration |
> | Action | Microsoft.Insights/Components/ProactiveDetectionConfigs/Write | Writing Application Insights proactive detection configuration |
> | Action | Microsoft.Insights/Components/providers/Microsoft.Insights/MetricDefinitions/Read | Read metric definitions |
> | Action | Microsoft.Insights/Components/Purge/Action | Purging data from Application Insights |
> | Action | Microsoft.Insights/Components/Query/Read | Run queries against Application Insights logs |
> | Action | Microsoft.Insights/Components/QuotaStatus/Read | Reading Application Insights component quota status |
> | Action | Microsoft.Insights/Components/Read | Reading an application insights component configuration |
> | Action | Microsoft.Insights/Components/SyntheticMonitorLocations/Read | Reading Application Insights webtest locations |
> | Action | Microsoft.Insights/Components/Webtests/Read | Reading a webtest configuration |
> | Action | Microsoft.Insights/Components/WorkItemConfigs/Delete | Deleting an Application Insights ALM integration configuration |
> | Action | Microsoft.Insights/Components/WorkItemConfigs/Read | Reading an Application Insights ALM integration configuration |
> | Action | Microsoft.Insights/Components/WorkItemConfigs/Write | Writing an Application Insights ALM integration configuration |
> | Action | Microsoft.Insights/Components/Write | Writing to an application insights component configuration |
> | Action | Microsoft.Insights/DiagnosticSettings/Delete | Delete a resource diagnostic setting |
> | Action | Microsoft.Insights/DiagnosticSettings/Read | Read a resource diagnostic setting |
> | Action | Microsoft.Insights/DiagnosticSettings/Write | Create or update a resource diagnostic setting |
> | Action | Microsoft.Insights/EventCategories/Read | Read available Activity Log event categories |
> | Action | Microsoft.Insights/eventtypes/digestevents/Read | Read management event type digest |
> | Action | Microsoft.Insights/eventtypes/values/Read | Read Activity Log events |
> | Action | Microsoft.Insights/ExtendedDiagnosticSettings/Delete | Delete a network flow log diagnostic setting |
> | Action | Microsoft.Insights/ExtendedDiagnosticSettings/Read | Read a network flow log diagnostic setting |
> | Action | Microsoft.Insights/ExtendedDiagnosticSettings/Write | Create or update a network flow log diagnostic setting |
> | Action | Microsoft.Insights/ListMigrationDate/Action | Get back Subscription migration date |
> | Action | Microsoft.Insights/ListMigrationDate/Read | Get back subscription migration date |
> | Action | Microsoft.Insights/LogDefinitions/Read | Read log definitions |
> | Action | Microsoft.Insights/LogProfiles/Delete | Delete an Activity Log log profile |
> | Action | Microsoft.Insights/LogProfiles/Read | Read an Activity Log log profile |
> | Action | Microsoft.Insights/LogProfiles/Write | Create or update an Activity Log log profile |
> | Action | Microsoft.Insights/Logs/ADAssessmentRecommendation/Read | Read data from the ADAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/ADReplicationResult/Read | Read data from the ADReplicationResult table |
> | Action | Microsoft.Insights/Logs/ADSecurityAssessmentRecommendation/Read | Read data from the ADSecurityAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/Alert/Read | Read data from the Alert table |
> | Action | Microsoft.Insights/Logs/AlertHistory/Read | Read data from the AlertHistory table |
> | Action | Microsoft.Insights/Logs/ApplicationInsights/Read | Read data from the ApplicationInsights table |
> | Action | Microsoft.Insights/Logs/AzureActivity/Read | Read data from the AzureActivity table |
> | Action | Microsoft.Insights/Logs/AzureMetrics/Read | Read data from the AzureMetrics table |
> | Action | Microsoft.Insights/Logs/BoundPort/Read | Read data from the BoundPort table |
> | Action | Microsoft.Insights/Logs/CommonSecurityLog/Read | Read data from the CommonSecurityLog table |
> | Action | Microsoft.Insights/Logs/ComputerGroup/Read | Read data from the ComputerGroup table |
> | Action | Microsoft.Insights/Logs/ConfigurationChange/Read | Read data from the ConfigurationChange table |
> | Action | Microsoft.Insights/Logs/ConfigurationData/Read | Read data from the ConfigurationData table |
> | Action | Microsoft.Insights/Logs/ContainerImageInventory/Read | Read data from the ContainerImageInventory table |
> | Action | Microsoft.Insights/Logs/ContainerInventory/Read | Read data from the ContainerInventory table |
> | Action | Microsoft.Insights/Logs/ContainerLog/Read | Read data from the ContainerLog table |
> | Action | Microsoft.Insights/Logs/ContainerServiceLog/Read | Read data from the ContainerServiceLog table |
> | Action | Microsoft.Insights/Logs/DeviceAppCrash/Read | Read data from the DeviceAppCrash table |
> | Action | Microsoft.Insights/Logs/DeviceAppLaunch/Read | Read data from the DeviceAppLaunch table |
> | Action | Microsoft.Insights/Logs/DeviceCalendar/Read | Read data from the DeviceCalendar table |
> | Action | Microsoft.Insights/Logs/DeviceCleanup/Read | Read data from the DeviceCleanup table |
> | Action | Microsoft.Insights/Logs/DeviceConnectSession/Read | Read data from the DeviceConnectSession table |
> | Action | Microsoft.Insights/Logs/DeviceEtw/Read | Read data from the DeviceEtw table |
> | Action | Microsoft.Insights/Logs/DeviceHardwareHealth/Read | Read data from the DeviceHardwareHealth table |
> | Action | Microsoft.Insights/Logs/DeviceHealth/Read | Read data from the DeviceHealth table |
> | Action | Microsoft.Insights/Logs/DeviceHeartbeat/Read | Read data from the DeviceHeartbeat table |
> | Action | Microsoft.Insights/Logs/DeviceSkypeHeartbeat/Read | Read data from the DeviceSkypeHeartbeat table |
> | Action | Microsoft.Insights/Logs/DeviceSkypeSignIn/Read | Read data from the DeviceSkypeSignIn table |
> | Action | Microsoft.Insights/Logs/DeviceSleepState/Read | Read data from the DeviceSleepState table |
> | Action | Microsoft.Insights/Logs/DHAppFailure/Read | Read data from the DHAppFailure table |
> | Action | Microsoft.Insights/Logs/DHAppReliability/Read | Read data from the DHAppReliability table |
> | Action | Microsoft.Insights/Logs/DHDriverReliability/Read | Read data from the DHDriverReliability table |
> | Action | Microsoft.Insights/Logs/DHLogonFailures/Read | Read data from the DHLogonFailures table |
> | Action | Microsoft.Insights/Logs/DHLogonMetrics/Read | Read data from the DHLogonMetrics table |
> | Action | Microsoft.Insights/Logs/DHOSCrashData/Read | Read data from the DHOSCrashData table |
> | Action | Microsoft.Insights/Logs/DHOSReliability/Read | Read data from the DHOSReliability table |
> | Action | Microsoft.Insights/Logs/DHWipAppLearning/Read | Read data from the DHWipAppLearning table |
> | Action | Microsoft.Insights/Logs/DnsEvents/Read | Read data from the DnsEvents table |
> | Action | Microsoft.Insights/Logs/DnsInventory/Read | Read data from the DnsInventory table |
> | Action | Microsoft.Insights/Logs/ETWEvent/Read | Read data from the ETWEvent table |
> | Action | Microsoft.Insights/Logs/Event/Read | Read data from the Event table |
> | Action | Microsoft.Insights/Logs/ExchangeAssessmentRecommendation/Read | Read data from the ExchangeAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/ExchangeOnlineAssessmentRecommendation/Read | Read data from the ExchangeOnlineAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/Heartbeat/Read | Read data from the Heartbeat table |
> | Action | Microsoft.Insights/Logs/IISAssessmentRecommendation/Read | Read data from the IISAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/InboundConnection/Read | Read data from the InboundConnection table |
> | Action | Microsoft.Insights/Logs/KubeNodeInventory/Read | Read data from the KubeNodeInventory table |
> | Action | Microsoft.Insights/Logs/KubePodInventory/Read | Read data from the KubePodInventory table |
> | Action | Microsoft.Insights/Logs/LinuxAuditLog/Read | Read data from the LinuxAuditLog table |
> | Action | Microsoft.Insights/Logs/MAApplication/Read | Read data from the MAApplication table |
> | Action | Microsoft.Insights/Logs/MAApplicationHealth/Read | Read data from the MAApplicationHealth table |
> | Action | Microsoft.Insights/Logs/MAApplicationHealthAlternativeVersions/Read | Read data from the MAApplicationHealthAlternativeVersions table |
> | Action | Microsoft.Insights/Logs/MAApplicationHealthIssues/Read | Read data from the MAApplicationHealthIssues table |
> | Action | Microsoft.Insights/Logs/MAApplicationInstance/Read | Read data from the MAApplicationInstance table |
> | Action | Microsoft.Insights/Logs/MAApplicationInstanceReadiness/Read | Read data from the MAApplicationInstanceReadiness table |
> | Action | Microsoft.Insights/Logs/MAApplicationReadiness/Read | Read data from the MAApplicationReadiness table |
> | Action | Microsoft.Insights/Logs/MADeploymentPlan/Read | Read data from the MADeploymentPlan table |
> | Action | Microsoft.Insights/Logs/MADevice/Read | Read data from the MADevice table |
> | Action | Microsoft.Insights/Logs/MADevicePnPHealth/Read | Read data from the MADevicePnPHealth table |
> | Action | Microsoft.Insights/Logs/MADevicePnPHealthAlternativeVersions/Read | Read data from the MADevicePnPHealthAlternativeVersions table |
> | Action | Microsoft.Insights/Logs/MADevicePnPHealthIssues/Read | Read data from the MADevicePnPHealthIssues table |
> | Action | Microsoft.Insights/Logs/MADeviceReadiness/Read | Read data from the MADeviceReadiness table |
> | Action | Microsoft.Insights/Logs/MADriverInstanceReadiness/Read | Read data from the MADriverInstanceReadiness table |
> | Action | Microsoft.Insights/Logs/MADriverReadiness/Read | Read data from the MADriverReadiness table |
> | Action | Microsoft.Insights/Logs/MAOfficeAddin/Read | Read data from the MAOfficeAddin table |
> | Action | Microsoft.Insights/Logs/MAOfficeAddinHealth/Read | Read data from the MAOfficeAddinHealth table |
> | Action | Microsoft.Insights/Logs/MAOfficeAddinHealthIssues/Read | Read data from the MAOfficeAddinHealthIssues table |
> | Action | Microsoft.Insights/Logs/MAOfficeAddinInstance/Read | Read data from the MAOfficeAddinInstance table |
> | Action | Microsoft.Insights/Logs/MAOfficeAddinInstanceReadiness/Read | Read data from the MAOfficeAddinInstanceReadiness table |
> | Action | Microsoft.Insights/Logs/MAOfficeAddinReadiness/Read | Read data from the MAOfficeAddinReadiness table |
> | Action | Microsoft.Insights/Logs/MAOfficeApp/Read | Read data from the MAOfficeApp table |
> | Action | Microsoft.Insights/Logs/MAOfficeAppHealth/Read | Read data from the MAOfficeAppHealth table |
> | Action | Microsoft.Insights/Logs/MAOfficeAppInstance/Read | Read data from the MAOfficeAppInstance table |
> | Action | Microsoft.Insights/Logs/MAOfficeAppReadiness/Read | Read data from the MAOfficeAppReadiness table |
> | Action | Microsoft.Insights/Logs/MAOfficeBuildInfo/Read | Read data from the MAOfficeBuildInfo table |
> | Action | Microsoft.Insights/Logs/MAOfficeCurrencyAssessment/Read | Read data from the MAOfficeCurrencyAssessment table |
> | Action | Microsoft.Insights/Logs/MAOfficeCurrencyAssessmentDailyCounts/Read | Read data from the MAOfficeCurrencyAssessmentDailyCounts table |
> | Action | Microsoft.Insights/Logs/MAOfficeDeploymentStatus/Read | Read data from the MAOfficeDeploymentStatus table |
> | Action | Microsoft.Insights/Logs/MAOfficeMacroHealth/Read | Read data from the MAOfficeMacroHealth table |
> | Action | Microsoft.Insights/Logs/MAOfficeMacroHealthIssues/Read | Read data from the MAOfficeMacroHealthIssues table |
> | Action | Microsoft.Insights/Logs/MAOfficeMacroIssueInstanceReadiness/Read | Read data from the MAOfficeMacroIssueInstanceReadiness table |
> | Action | Microsoft.Insights/Logs/MAOfficeMacroIssueReadiness/Read | Read data from the MAOfficeMacroIssueReadiness table |
> | Action | Microsoft.Insights/Logs/MAOfficeMacroSummary/Read | Read data from the MAOfficeMacroSummary table |
> | Action | Microsoft.Insights/Logs/MAOfficeSuite/Read | Read data from the MAOfficeSuite table |
> | Action | Microsoft.Insights/Logs/MAOfficeSuiteInstance/Read | Read data from the MAOfficeSuiteInstance table |
> | Action | Microsoft.Insights/Logs/MAProposedPilotDevices/Read | Read data from the MAProposedPilotDevices table |
> | Action | Microsoft.Insights/Logs/MAWindowsBuildInfo/Read | Read data from the MAWindowsBuildInfo table |
> | Action | Microsoft.Insights/Logs/MAWindowsCurrencyAssessment/Read | Read data from the MAWindowsCurrencyAssessment table |
> | Action | Microsoft.Insights/Logs/MAWindowsCurrencyAssessmentDailyCounts/Read | Read data from the MAWindowsCurrencyAssessmentDailyCounts table |
> | Action | Microsoft.Insights/Logs/MAWindowsDeploymentStatus/Read | Read data from the MAWindowsDeploymentStatus table |
> | Action | Microsoft.Insights/Logs/MAWindowsSysReqInstanceReadiness/Read | Read data from the MAWindowsSysReqInstanceReadiness table |
> | Action | Microsoft.Insights/Logs/NetworkMonitoring/Read | Read data from the NetworkMonitoring table |
> | Action | Microsoft.Insights/Logs/OfficeActivity/Read | Read data from the OfficeActivity table |
> | Action | Microsoft.Insights/Logs/Operation/Read | Read data from the Operation table |
> | Action | Microsoft.Insights/Logs/OutboundConnection/Read | Read data from the OutboundConnection table |
> | Action | Microsoft.Insights/Logs/Perf/Read | Read data from the Perf table |
> | Action | Microsoft.Insights/Logs/ProtectionStatus/Read | Read data from the ProtectionStatus table |
> | Action | Microsoft.Insights/Logs/Read | Reading data from all your logs |
> | Action | Microsoft.Insights/Logs/ReservedAzureCommonFields/Read | Read data from the ReservedAzureCommonFields table |
> | Action | Microsoft.Insights/Logs/ReservedCommonFields/Read | Read data from the ReservedCommonFields table |
> | Action | Microsoft.Insights/Logs/SCCMAssessmentRecommendation/Read | Read data from the SCCMAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SCOMAssessmentRecommendation/Read | Read data from the SCOMAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SecurityAlert/Read | Read data from the SecurityAlert table |
> | Action | Microsoft.Insights/Logs/SecurityBaseline/Read | Read data from the SecurityBaseline table |
> | Action | Microsoft.Insights/Logs/SecurityBaselineSummary/Read | Read data from the SecurityBaselineSummary table |
> | Action | Microsoft.Insights/Logs/SecurityDetection/Read | Read data from the SecurityDetection table |
> | Action | Microsoft.Insights/Logs/SecurityEvent/Read | Read data from the SecurityEvent table |
> | Action | Microsoft.Insights/Logs/ServiceFabricOperationalEvent/Read | Read data from the ServiceFabricOperationalEvent table |
> | Action | Microsoft.Insights/Logs/ServiceFabricReliableActorEvent/Read | Read data from the ServiceFabricReliableActorEvent table |
> | Action | Microsoft.Insights/Logs/ServiceFabricReliableServiceEvent/Read | Read data from the ServiceFabricReliableServiceEvent table |
> | Action | Microsoft.Insights/Logs/SfBAssessmentRecommendation/Read | Read data from the SfBAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SfBOnlineAssessmentRecommendation/Read | Read data from the SfBOnlineAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SharePointOnlineAssessmentRecommendation/Read | Read data from the SharePointOnlineAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SPAssessmentRecommendation/Read | Read data from the SPAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SQLAssessmentRecommendation/Read | Read data from the SQLAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/SQLQueryPerformance/Read | Read data from the SQLQueryPerformance table |
> | Action | Microsoft.Insights/Logs/Syslog/Read | Read data from the Syslog table |
> | Action | Microsoft.Insights/Logs/SysmonEvent/Read | Read data from the SysmonEvent table |
> | Action | Microsoft.Insights/Logs/UAApp/Read | Read data from the UAApp table |
> | Action | Microsoft.Insights/Logs/UAComputer/Read | Read data from the UAComputer table |
> | Action | Microsoft.Insights/Logs/UAComputerRank/Read | Read data from the UAComputerRank table |
> | Action | Microsoft.Insights/Logs/UADriver/Read | Read data from the UADriver table |
> | Action | Microsoft.Insights/Logs/UADriverProblemCodes/Read | Read data from the UADriverProblemCodes table |
> | Action | Microsoft.Insights/Logs/UAFeedback/Read | Read data from the UAFeedback table |
> | Action | Microsoft.Insights/Logs/UAHardwareSecurity/Read | Read data from the UAHardwareSecurity table |
> | Action | Microsoft.Insights/Logs/UAIESiteDiscovery/Read | Read data from the UAIESiteDiscovery table |
> | Action | Microsoft.Insights/Logs/UAOfficeAddIn/Read | Read data from the UAOfficeAddIn table |
> | Action | Microsoft.Insights/Logs/UAProposedActionPlan/Read | Read data from the UAProposedActionPlan table |
> | Action | Microsoft.Insights/Logs/UASysReqIssue/Read | Read data from the UASysReqIssue table |
> | Action | Microsoft.Insights/Logs/UAUpgradedComputer/Read | Read data from the UAUpgradedComputer table |
> | Action | Microsoft.Insights/Logs/Update/Read | Read data from the Update table |
> | Action | Microsoft.Insights/Logs/UpdateRunProgress/Read | Read data from the UpdateRunProgress table |
> | Action | Microsoft.Insights/Logs/UpdateSummary/Read | Read data from the UpdateSummary table |
> | Action | Microsoft.Insights/Logs/Usage/Read | Read data from the Usage table |
> | Action | Microsoft.Insights/Logs/W3CIISLog/Read | Read data from the W3CIISLog table |
> | Action | Microsoft.Insights/Logs/WaaSDeploymentStatus/Read | Read data from the WaaSDeploymentStatus table |
> | Action | Microsoft.Insights/Logs/WaaSInsiderStatus/Read | Read data from the WaaSInsiderStatus table |
> | Action | Microsoft.Insights/Logs/WaaSUpdateStatus/Read | Read data from the WaaSUpdateStatus table |
> | Action | Microsoft.Insights/Logs/WDAVStatus/Read | Read data from the WDAVStatus table |
> | Action | Microsoft.Insights/Logs/WDAVThreat/Read | Read data from the WDAVThreat table |
> | Action | Microsoft.Insights/Logs/WindowsClientAssessmentRecommendation/Read | Read data from the WindowsClientAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/WindowsFirewall/Read | Read data from the WindowsFirewall table |
> | Action | Microsoft.Insights/Logs/WindowsServerAssessmentRecommendation/Read | Read data from the WindowsServerAssessmentRecommendation table |
> | Action | Microsoft.Insights/Logs/WireData/Read | Read data from the WireData table |
> | Action | Microsoft.Insights/Logs/WUDOAggregatedStatus/Read | Read data from the WUDOAggregatedStatus table |
> | Action | Microsoft.Insights/Logs/WUDOStatus/Read | Read data from the WUDOStatus table |
> | Action | Microsoft.Insights/MetricAlerts/Delete | Delete a metric alert |
> | Action | Microsoft.Insights/MetricAlerts/Read | Read a metric alert |
> | Action | Microsoft.Insights/MetricAlerts/Status/Read | Read metric alert status |
> | Action | Microsoft.Insights/MetricAlerts/Write | Create or update a metric alert |
> | Action | Microsoft.Insights/MetricDefinitions/Microsoft.Insights/Read | Read metric definitions |
> | Action | Microsoft.Insights/MetricDefinitions/providers/Microsoft.Insights/Read | Read metric definitions |
> | Action | Microsoft.Insights/MetricDefinitions/Read | Read metric definitions |
> | Action | Microsoft.Insights/Metrics/providers/Metrics/Read | Read metrics |
> | Action | Microsoft.Insights/Metrics/Read | Read metrics |
> | DataAction | Microsoft.Insights/Metrics/Write | Write metrics |
> | Action | Microsoft.Insights/MigrateToNewpricingModel/Action | Migrate subscription to new pricing model |
> | Action | Microsoft.Insights/Operations/Read | Read operations |
> | Action | Microsoft.Insights/Register/Action | Register the Microsoft Insights provider |
> | Action | Microsoft.Insights/RollbackToLegacyPricingModel/Action | Rollback subscription to legacy pricing model |
> | Action | Microsoft.Insights/ScheduledQueryRules/Delete | Deleting a scheduled query rule |
> | Action | Microsoft.Insights/ScheduledQueryRules/Read | Reading a scheduled query rule |
> | Action | Microsoft.Insights/ScheduledQueryRules/Write | Writing a scheduled query rule |
> | Action | Microsoft.Insights/Tenants/Register/Action | Initializes the Microsoft Insights provider |
> | Action | Microsoft.Insights/Unregister/Action | Register the Microsoft Insights provider |
> | Action | Microsoft.Insights/Webtests/Delete | Deleting a webtest configuration |
> | Action | Microsoft.Insights/Webtests/GetToken/Read | Reading a webtest token |
> | Action | Microsoft.Insights/Webtests/MetricDefinitions/Read | Reading a webtest metric definitions |
> | Action | Microsoft.Insights/Webtests/Metrics/Read | Reading a webtest metrics |
> | Action | Microsoft.Insights/Webtests/Read | Reading a webtest configuration |
> | Action | Microsoft.Insights/Webtests/Write | Writing to a webtest configuration |

## Microsoft.IoTSpaces

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.IoTSpaces/Graph/delete | Deletes Microsoft.IoTSpaces Graph resource |
> | Action | Microsoft.IoTSpaces/Graph/providers/Microsoft.Insights/diagnosticSettings/read | Get Diagnostic Settings for the resource |
> | Action | Microsoft.IoTSpaces/Graph/providers/Microsoft.Insights/diagnosticSettings/write | Set Diagnostic Settings for the resource |
> | Action | Microsoft.IoTSpaces/Graph/providers/Microsoft.Insights/logDefinitions/read | Gets the available log definitions for the Microsoft.IoTSpaces service |
> | Action | Microsoft.IoTSpaces/Graph/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metric definitions for the Microsoft.IoTSpaces service |
> | Action | Microsoft.IoTSpaces/Graph/read | Gets the Microsoft.IoTSpaces Graph resource(s) |
> | Action | Microsoft.IoTSpaces/Graph/write | Create Microsoft.IoTSpaces Graph resource |
> | Action | Microsoft.IoTSpaces/register/action | Register subscription for Microsoft.IoTSpaces Graph resource provider to enable creationg of resources |

## Microsoft.KeyVault

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.KeyVault/checkNameAvailability/read | Checks that a key vault name is valid and is not in use |
> | Action | Microsoft.KeyVault/deletedVaults/read | View the properties of soft deleted key vaults |
> | Action | Microsoft.KeyVault/hsmPools/delete | Delete an HSM pool |
> | Action | Microsoft.KeyVault/hsmPools/joinVault/action | Join a key vault to an HSM pool |
> | Action | Microsoft.KeyVault/hsmPools/read | View the properties of an HSM pool |
> | Action | Microsoft.KeyVault/hsmPools/write | Create a new HSM pool of update the properties of an existing HSM pool |
> | Action | Microsoft.KeyVault/locations/deletedVaults/purge/action | Purge a soft deleted key vault |
> | Action | Microsoft.KeyVault/locations/deletedVaults/read | View the properties of a soft deleted key vault |
> | Action | Microsoft.KeyVault/locations/deleteVirtualNetworkOrSubnets/action | Notifies Microsoft.KeyVault that a virtual network or subnet is being deleted |
> | Action | Microsoft.KeyVault/locations/operationResults/read | Check the result of a long run operation |
> | Action | Microsoft.KeyVault/operations/read | Lists operations available on Microsoft.KeyVault resource provider |
> | Action | Microsoft.KeyVault/register/action | Registers a subscription |
> | Action | Microsoft.KeyVault/unregister/action | Unregisters a subscription |
> | Action | Microsoft.KeyVault/vaults/accessPolicies/write | Update an existing access policy by merging or replacing, or add a new access policy to a vault. |
> | Action | Microsoft.KeyVault/vaults/delete | Delete a key vault |
> | Action | Microsoft.KeyVault/vaults/deploy/action | Enables access to secrets in a key vault when deploying Azure resources |
> | Action | Microsoft.KeyVault/vaults/providers/Microsoft.Insights/diagnosticSettings/Read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.KeyVault/vaults/providers/Microsoft.Insights/diagnosticSettings/Write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.KeyVault/vaults/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for a key vault |
> | Action | Microsoft.KeyVault/vaults/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for a key vault |
> | Action | Microsoft.KeyVault/vaults/read | View the properties of a key vault |
> | Action | Microsoft.KeyVault/vaults/secrets/read | View the properties of a secret, but not its value |
> | Action | Microsoft.KeyVault/vaults/secrets/write | Create a new secret or update the value of an existing secret |
> | Action | Microsoft.KeyVault/vaults/write | Create a new key vault or update the properties of an existing key vault |

## Microsoft.Kusto

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Kusto/Clusters/Databases/delete | Deletes a database resource. |
> | Action | Microsoft.Kusto/Clusters/Databases/EventHubConnections/delete | Deletes an event hub connections resource. |
> | Action | Microsoft.Kusto/Clusters/Databases/EventHubConnections/read | Reads an event hub connections resource. |
> | Action | Microsoft.Kusto/Clusters/Databases/EventHubConnections/write | Writes an event hub connetions resource. |
> | Action | Microsoft.Kusto/Clusters/Databases/read | Reads a database resource. |
> | Action | Microsoft.Kusto/Clusters/Databases/write | Writes a database resource. |
> | Action | Microsoft.Kusto/Clusters/delete | Deletes a cluster resource. |
> | Action | Microsoft.Kusto/Clusters/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic settings for the resource |
> | Action | Microsoft.Kusto/Clusters/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Kusto/Clusters/providers/Microsoft.Insights/metricDefinitions/read | Gets the metric definitions of the resource |
> | Action | Microsoft.Kusto/Clusters/read | Reads a cluster resource. |
> | Action | Microsoft.Kusto/Clusters/write | Writes a cluster resource. |
> | Action | Microsoft.Kusto/Locations/CheckNameAvailability/write | Reads check name availability resource |
> | Action | Microsoft.Kusto/locations/operationresults/read | Reads operations resources |
> | Action | Microsoft.Kusto/Operations/read | Reads operations resources |

## Microsoft.LabServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.LabServices/labAccounts/CreateLab/action | Create a lab in a lab account. |
> | Action | Microsoft.LabServices/labAccounts/delete | Delete lab accounts. |
> | Action | Microsoft.LabServices/labAccounts/galleryImages/delete | Delete gallery images. |
> | Action | Microsoft.LabServices/labAccounts/galleryImages/read | Read gallery images. |
> | Action | Microsoft.LabServices/labAccounts/galleryImages/write | Add or modify gallery images. |
> | Action | Microsoft.LabServices/labAccounts/GetRegionalAvailability/action | Get regional availability information for each size category configured under a lab account |
> | Action | Microsoft.LabServices/labAccounts/labs/AddUsers/action | Add users to a lab |
> | Action | Microsoft.LabServices/labAccounts/labs/delete | Delete labs. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/ClaimAny/action | Claims a random environment for a user in an environment settings |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/delete | Delete environment setting. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/environments/Claim/action | Claims the environment and assigns it to the user |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/environments/delete | Delete environments. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/environments/read | Read environments. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/environments/Start/action | Starts an environment by starting all resources inside the environment. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/environments/Stop/action | Stops an environment by stopping all resources inside the environment |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/environments/write | Add or modify environments. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/Publish/action | Provisions/deprovisions required resources for an environment setting based on current state of the lab/environment setting. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/read | Read environment setting. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/Start/action | Starts a template by starting all resources inside the template. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/Stop/action | Starts a template by starting all resources inside the template. |
> | Action | Microsoft.LabServices/labAccounts/labs/environmentSettings/write | Add or modify environment setting. |
> | Action | Microsoft.LabServices/labAccounts/labs/read | Read labs. |
> | Action | Microsoft.LabServices/labAccounts/labs/Register/action | Register to managed lab. |
> | Action | Microsoft.LabServices/labAccounts/labs/users/delete | Delete users. |
> | Action | Microsoft.LabServices/labAccounts/labs/users/read | Read users. |
> | Action | Microsoft.LabServices/labAccounts/labs/users/write | Add or modify users. |
> | Action | Microsoft.LabServices/labAccounts/labs/write | Add or modify labs. |
> | Action | Microsoft.LabServices/labAccounts/read | Read lab accounts. |
> | Action | Microsoft.LabServices/labAccounts/write | Add or modify lab accounts. |
> | Action | Microsoft.LabServices/locations/operations/read | Read operations. |
> | Action | Microsoft.LabServices/register/action | Registers the subscription |
> | Action | Microsoft.LabServices/users/GetEnvironment/action | Gets the virtual machine details |
> | Action | Microsoft.LabServices/users/GetOperationBatchStatus/action | Get batch operation status |
> | Action | Microsoft.LabServices/users/GetOperationStatus/action | Gets the status of long running operation |
> | Action | Microsoft.LabServices/users/ListEnvironments/action | List Environments for the user |
> | Action | Microsoft.LabServices/users/ListLabs/action | List labs for the user. |
> | Action | Microsoft.LabServices/users/Register/action | Register a user to a managed lab |
> | Action | Microsoft.LabServices/users/StartEnvironment/action | Starts an environment by starting all resources inside the environment. |
> | Action | Microsoft.LabServices/users/StopEnvironment/action | Stops an environment by stopping all resources inside the environment |

## Microsoft.LocationBasedServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.LocationBasedServices/accounts/delete | (Deprecated: Please use /providers/Microsoft.Maps) Delete a Location Based Services Account. |
> | Action | Microsoft.LocationBasedServices/accounts/listKeys/action | (Deprecated: Please use /providers/Microsoft.Maps)List Location Based Services Account keys |
> | Action | Microsoft.LocationBasedServices/accounts/providers/Microsoft.Insights/diagnosticSettings/read | (Deprecated: Please use /providers/Microsoft.Maps) Gets the diagnostic setting for the resource |
> | Action | Microsoft.LocationBasedServices/accounts/providers/Microsoft.Insights/diagnosticSettings/write | (Deprecated: Please use /providers/Microsoft.Maps) Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.LocationBasedServices/accounts/providers/Microsoft.Insights/metricDefinitions/read | (Deprecated: Please use /providers/Microsoft.Maps) Gets the available metrics for Location Based Services Accounts |
> | Action | Microsoft.LocationBasedServices/accounts/read | (Deprecated: Please use /providers/Microsoft.Maps) Get a Location Based Services Account. |
> | Action | Microsoft.LocationBasedServices/accounts/regenerateKey/action | (Deprecated: Please use /providers/Microsoft.Maps) Generate new Location Based Services Account primary or secondary key |
> | Action | Microsoft.LocationBasedServices/accounts/write | (Deprecated: Please use /providers/Microsoft.Maps) Create or update a Location Based Services Account. |
> | Action | Microsoft.LocationBasedServices/register/action | (Deprecated: Please use /providers/Microsoft.Maps) Register the provider |

## Microsoft.LocationServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.LocationServices/accounts/delete | (Deprecated: Please use /providers/Microsoft.Maps) Delete a Location Services Account. |
> | Action | Microsoft.LocationServices/accounts/listKeys/action | (Deprecated: Please use /providers/Microsoft.Maps)List Location Based Services Account keys |
> | Action | Microsoft.LocationServices/accounts/providers/Microsoft.Insights/diagnosticSettings/read | (Deprecated: Please use /providers/Microsoft.Maps) Gets the diagnostic setting for the resource |
> | Action | Microsoft.LocationServices/accounts/providers/Microsoft.Insights/diagnosticSettings/write | (Deprecated: Please use /providers/Microsoft.Maps) Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.LocationServices/accounts/providers/Microsoft.Insights/metricDefinitions/read | (Deprecated: Please use /providers/Microsoft.Maps) Gets the available metrics for Location Based Services Accounts |
> | Action | Microsoft.LocationServices/accounts/read | (Deprecated: Please use /providers/Microsoft.Maps) Get a Location Services Account. |
> | Action | Microsoft.LocationServices/accounts/regenerateKey/action | (Deprecated: Please use /providers/Microsoft.Maps) Generate new Location Based Services Account primary or secondary key |
> | Action | Microsoft.LocationServices/accounts/write | (Deprecated: Please use /providers/Microsoft.Maps) Create or update a Location Services Account. |
> | Action | Microsoft.LocationServices/register/action | (Deprecated: Please use /providers/Microsoft.Maps) Register the provider |

## Microsoft.LogAnalytics

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | DataAction | Microsoft.LogAnalytics/logs/ADAssessmentRecommendation/read | Read data from the ADAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/ADReplicationResult/read | Read data from the ADReplicationResult table |
> | DataAction | Microsoft.LogAnalytics/logs/ADSecurityAssessmentRecommendation/read | Read data from the ADSecurityAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/Alert/read | Read data from the Alert table |
> | DataAction | Microsoft.LogAnalytics/logs/AlertHistory/read | Read data from the AlertHistory table |
> | DataAction | Microsoft.LogAnalytics/logs/ApplicationInsights/read | Read data from the ApplicationInsights table |
> | DataAction | Microsoft.LogAnalytics/logs/AuditLogs/read | Read data from the AuditLogs table |
> | DataAction | Microsoft.LogAnalytics/logs/AzureActivity/read | Read data from the AzureActivity table |
> | DataAction | Microsoft.LogAnalytics/logs/AzureMetrics/read | Read data from the AzureMetrics table |
> | DataAction | Microsoft.LogAnalytics/logs/BoundPort/read | Read data from the BoundPort table |
> | DataAction | Microsoft.LogAnalytics/logs/CommonSecurityLog/read | Read data from the CommonSecurityLog table |
> | DataAction | Microsoft.LogAnalytics/logs/ComputerGroup/read | Read data from the ComputerGroup table |
> | DataAction | Microsoft.LogAnalytics/logs/ConfigurationChange/read | Read data from the ConfigurationChange table |
> | DataAction | Microsoft.LogAnalytics/logs/ConfigurationData/read | Read data from the ConfigurationData table |
> | DataAction | Microsoft.LogAnalytics/logs/ContainerImageInventory/read | Read data from the ContainerImageInventory table |
> | DataAction | Microsoft.LogAnalytics/logs/ContainerInventory/read | Read data from the ContainerInventory table |
> | DataAction | Microsoft.LogAnalytics/logs/ContainerLog/read | Read data from the ContainerLog table |
> | DataAction | Microsoft.LogAnalytics/logs/ContainerServiceLog/read | Read data from the ContainerServiceLog table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceAppCrash/read | Read data from the DeviceAppCrash table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceAppLaunch/read | Read data from the DeviceAppLaunch table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceCalendar/read | Read data from the DeviceCalendar table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceCleanup/read | Read data from the DeviceCleanup table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceConnectSession/read | Read data from the DeviceConnectSession table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceEtw/read | Read data from the DeviceEtw table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceHardwareHealth/read | Read data from the DeviceHardwareHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceHealth/read | Read data from the DeviceHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceHeartbeat/read | Read data from the DeviceHeartbeat table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceSkypeHeartbeat/read | Read data from the DeviceSkypeHeartbeat table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceSkypeSignIn/read | Read data from the DeviceSkypeSignIn table |
> | DataAction | Microsoft.LogAnalytics/logs/DeviceSleepState/read | Read data from the DeviceSleepState table |
> | DataAction | Microsoft.LogAnalytics/logs/DHAppFailure/read | Read data from the DHAppFailure table |
> | DataAction | Microsoft.LogAnalytics/logs/DHAppReliability/read | Read data from the DHAppReliability table |
> | DataAction | Microsoft.LogAnalytics/logs/DHDriverReliability/read | Read data from the DHDriverReliability table |
> | DataAction | Microsoft.LogAnalytics/logs/DHLogonFailures/read | Read data from the DHLogonFailures table |
> | DataAction | Microsoft.LogAnalytics/logs/DHLogonMetrics/read | Read data from the DHLogonMetrics table |
> | DataAction | Microsoft.LogAnalytics/logs/DHOSCrashData/read | Read data from the DHOSCrashData table |
> | DataAction | Microsoft.LogAnalytics/logs/DHOSReliability/read | Read data from the DHOSReliability table |
> | DataAction | Microsoft.LogAnalytics/logs/DHWipAppLearning/read | Read data from the DHWipAppLearning table |
> | DataAction | Microsoft.LogAnalytics/logs/DnsEvents/read | Read data from the DnsEvents table |
> | DataAction | Microsoft.LogAnalytics/logs/DnsInventory/read | Read data from the DnsInventory table |
> | DataAction | Microsoft.LogAnalytics/logs/ETWEvent/read | Read data from the ETWEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/Event/read | Read data from the Event table |
> | DataAction | Microsoft.LogAnalytics/logs/ExchangeAssessmentRecommendation/read | Read data from the ExchangeAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/ExchangeOnlineAssessmentRecommendation/read | Read data from the ExchangeOnlineAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/Heartbeat/read | Read data from the Heartbeat table |
> | DataAction | Microsoft.LogAnalytics/logs/IISAssessmentRecommendation/read | Read data from the IISAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/InboundConnection/read | Read data from the InboundConnection table |
> | DataAction | Microsoft.LogAnalytics/logs/KubeEvents/read | Read data from the KubeEvents table |
> | DataAction | Microsoft.LogAnalytics/logs/KubeNodeInventory/read | Read data from the KubeNodeInventory table |
> | DataAction | Microsoft.LogAnalytics/logs/KubePodInventory/read | Read data from the KubePodInventory table |
> | DataAction | Microsoft.LogAnalytics/logs/KubeServices/read | Read data from the KubeServices table |
> | DataAction | Microsoft.LogAnalytics/logs/LinuxAuditLog/read | Read data from the LinuxAuditLog table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplication/read | Read data from the MAApplication table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplicationHealth/read | Read data from the MAApplicationHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplicationHealthAlternativeVersions/read | Read data from the MAApplicationHealthAlternativeVersions table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplicationHealthIssues/read | Read data from the MAApplicationHealthIssues table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplicationInstance/read | Read data from the MAApplicationInstance table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplicationInstanceReadiness/read | Read data from the MAApplicationInstanceReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAApplicationReadiness/read | Read data from the MAApplicationReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MADeploymentPlan/read | Read data from the MADeploymentPlan table |
> | DataAction | Microsoft.LogAnalytics/logs/MADevice/read | Read data from the MADevice table |
> | DataAction | Microsoft.LogAnalytics/logs/MADevicePnPHealth/read | Read data from the MADevicePnPHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/MADevicePnPHealthAlternativeVersions/read | Read data from the MADevicePnPHealthAlternativeVersions table |
> | DataAction | Microsoft.LogAnalytics/logs/MADevicePnPHealthIssues/read | Read data from the MADevicePnPHealthIssues table |
> | DataAction | Microsoft.LogAnalytics/logs/MADeviceReadiness/read | Read data from the MADeviceReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MADriverInstanceReadiness/read | Read data from the MADriverInstanceReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MADriverReadiness/read | Read data from the MADriverReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAddin/read | Read data from the MAOfficeAddin table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAddinHealth/read | Read data from the MAOfficeAddinHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAddinHealthIssues/read | Read data from the MAOfficeAddinHealthIssues table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAddinInstance/read | Read data from the MAOfficeAddinInstance table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAddinInstanceReadiness/read | Read data from the MAOfficeAddinInstanceReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAddinReadiness/read | Read data from the MAOfficeAddinReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeApp/read | Read data from the MAOfficeApp table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAppHealth/read | Read data from the MAOfficeAppHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAppInstance/read | Read data from the MAOfficeAppInstance table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeAppReadiness/read | Read data from the MAOfficeAppReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeBuildInfo/read | Read data from the MAOfficeBuildInfo table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeCurrencyAssessment/read | Read data from the MAOfficeCurrencyAssessment table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeCurrencyAssessmentDailyCounts/read | Read data from the MAOfficeCurrencyAssessmentDailyCounts table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeDeploymentStatus/read | Read data from the MAOfficeDeploymentStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeMacroHealth/read | Read data from the MAOfficeMacroHealth table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeMacroHealthIssues/read | Read data from the MAOfficeMacroHealthIssues table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeMacroIssueInstanceReadiness/read | Read data from the MAOfficeMacroIssueInstanceReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeMacroIssueReadiness/read | Read data from the MAOfficeMacroIssueReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeMacroSummary/read | Read data from the MAOfficeMacroSummary table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeSuite/read | Read data from the MAOfficeSuite table |
> | DataAction | Microsoft.LogAnalytics/logs/MAOfficeSuiteInstance/read | Read data from the MAOfficeSuiteInstance table |
> | DataAction | Microsoft.LogAnalytics/logs/MAProposedPilotDevices/read | Read data from the MAProposedPilotDevices table |
> | DataAction | Microsoft.LogAnalytics/logs/MAWindowsBuildInfo/read | Read data from the MAWindowsBuildInfo table |
> | DataAction | Microsoft.LogAnalytics/logs/MAWindowsCurrencyAssessment/read | Read data from the MAWindowsCurrencyAssessment table |
> | DataAction | Microsoft.LogAnalytics/logs/MAWindowsCurrencyAssessmentDailyCounts/read | Read data from the MAWindowsCurrencyAssessmentDailyCounts table |
> | DataAction | Microsoft.LogAnalytics/logs/MAWindowsDeploymentStatus/read | Read data from the MAWindowsDeploymentStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/MAWindowsSysReqInstanceReadiness/read | Read data from the MAWindowsSysReqInstanceReadiness table |
> | DataAction | Microsoft.LogAnalytics/logs/NetworkMonitoring/read | Read data from the NetworkMonitoring table |
> | DataAction | Microsoft.LogAnalytics/logs/OfficeActivity/read | Read data from the OfficeActivity table |
> | DataAction | Microsoft.LogAnalytics/logs/Operation/read | Read data from the Operation table |
> | DataAction | Microsoft.LogAnalytics/logs/OutboundConnection/read | Read data from the OutboundConnection table |
> | DataAction | Microsoft.LogAnalytics/logs/Perf/read | Read data from the Perf table |
> | DataAction | Microsoft.LogAnalytics/logs/ProtectionStatus/read | Read data from the ProtectionStatus table |
> | Action | Microsoft.LogAnalytics/logs/read | Reading data from all your logs |
> | DataAction | Microsoft.LogAnalytics/logs/ReservedAzureCommonFields/read | Read data from the ReservedAzureCommonFields table |
> | DataAction | Microsoft.LogAnalytics/logs/ReservedCommonFields/read | Read data from the ReservedCommonFields table |
> | DataAction | Microsoft.LogAnalytics/logs/SCCMAssessmentRecommendation/read | Read data from the SCCMAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SCOMAssessmentRecommendation/read | Read data from the SCOMAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SecurityAlert/read | Read data from the SecurityAlert table |
> | DataAction | Microsoft.LogAnalytics/logs/SecurityBaseline/read | Read data from the SecurityBaseline table |
> | DataAction | Microsoft.LogAnalytics/logs/SecurityBaselineSummary/read | Read data from the SecurityBaselineSummary table |
> | DataAction | Microsoft.LogAnalytics/logs/SecurityDetection/read | Read data from the SecurityDetection table |
> | DataAction | Microsoft.LogAnalytics/logs/SecurityEvent/read | Read data from the SecurityEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/ServiceFabricOperationalEvent/read | Read data from the ServiceFabricOperationalEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/ServiceFabricReliableActorEvent/read | Read data from the ServiceFabricReliableActorEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/ServiceFabricReliableServiceEvent/read | Read data from the ServiceFabricReliableServiceEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/SfBAssessmentRecommendation/read | Read data from the SfBAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SfBOnlineAssessmentRecommendation/read | Read data from the SfBOnlineAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SharePointOnlineAssessmentRecommendation/read | Read data from the SharePointOnlineAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SigninLogs/read | Read data from the SigninLogs table |
> | DataAction | Microsoft.LogAnalytics/logs/SPAssessmentRecommendation/read | Read data from the SPAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SQLAssessmentRecommendation/read | Read data from the SQLAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/SQLQueryPerformance/read | Read data from the SQLQueryPerformance table |
> | DataAction | Microsoft.LogAnalytics/logs/Syslog/read | Read data from the Syslog table |
> | DataAction | Microsoft.LogAnalytics/logs/SysmonEvent/read | Read data from the SysmonEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/Tables.Custom/read | Reading data from any custom log |
> | DataAction | Microsoft.LogAnalytics/logs/UAApp/read | Read data from the UAApp table |
> | DataAction | Microsoft.LogAnalytics/logs/UAComputer/read | Read data from the UAComputer table |
> | DataAction | Microsoft.LogAnalytics/logs/UAComputerRank/read | Read data from the UAComputerRank table |
> | DataAction | Microsoft.LogAnalytics/logs/UADriver/read | Read data from the UADriver table |
> | DataAction | Microsoft.LogAnalytics/logs/UADriverProblemCodes/read | Read data from the UADriverProblemCodes table |
> | DataAction | Microsoft.LogAnalytics/logs/UAFeedback/read | Read data from the UAFeedback table |
> | DataAction | Microsoft.LogAnalytics/logs/UAHardwareSecurity/read | Read data from the UAHardwareSecurity table |
> | DataAction | Microsoft.LogAnalytics/logs/UAIESiteDiscovery/read | Read data from the UAIESiteDiscovery table |
> | DataAction | Microsoft.LogAnalytics/logs/UAOfficeAddIn/read | Read data from the UAOfficeAddIn table |
> | DataAction | Microsoft.LogAnalytics/logs/UAProposedActionPlan/read | Read data from the UAProposedActionPlan table |
> | DataAction | Microsoft.LogAnalytics/logs/UASysReqIssue/read | Read data from the UASysReqIssue table |
> | DataAction | Microsoft.LogAnalytics/logs/UAUpgradedComputer/read | Read data from the UAUpgradedComputer table |
> | DataAction | Microsoft.LogAnalytics/logs/Update/read | Read data from the Update table |
> | DataAction | Microsoft.LogAnalytics/logs/UpdateRunProgress/read | Read data from the UpdateRunProgress table |
> | DataAction | Microsoft.LogAnalytics/logs/UpdateSummary/read | Read data from the UpdateSummary table |
> | DataAction | Microsoft.LogAnalytics/logs/Usage/read | Read data from the Usage table |
> | DataAction | Microsoft.LogAnalytics/logs/VMBoundPort/read | Read data from the VMBoundPort table |
> | DataAction | Microsoft.LogAnalytics/logs/VMConnection/read | Read data from the VMConnection table |
> | DataAction | Microsoft.LogAnalytics/logs/W3CIISLog/read | Read data from the W3CIISLog table |
> | DataAction | Microsoft.LogAnalytics/logs/WaaSDeploymentStatus/read | Read data from the WaaSDeploymentStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/WaaSInsiderStatus/read | Read data from the WaaSInsiderStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/WaaSUpdateStatus/read | Read data from the WaaSUpdateStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/WDAVStatus/read | Read data from the WDAVStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/WDAVThreat/read | Read data from the WDAVThreat table |
> | DataAction | Microsoft.LogAnalytics/logs/WindowsClientAssessmentRecommendation/read | Read data from the WindowsClientAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/WindowsEvent/read | Read data from the WindowsEvent table |
> | DataAction | Microsoft.LogAnalytics/logs/WindowsFirewall/read | Read data from the WindowsFirewall table |
> | DataAction | Microsoft.LogAnalytics/logs/WindowsServerAssessmentRecommendation/read | Read data from the WindowsServerAssessmentRecommendation table |
> | DataAction | Microsoft.LogAnalytics/logs/WireData/read | Read data from the WireData table |
> | DataAction | Microsoft.LogAnalytics/logs/WorkloadMonitoringPerf/read | Read data from the WorkloadMonitoringPerf table |
> | DataAction | Microsoft.LogAnalytics/logs/WUDOAggregatedStatus/read | Read data from the WUDOAggregatedStatus table |
> | DataAction | Microsoft.LogAnalytics/logs/WUDOStatus/read | Read data from the WUDOStatus table |

## Microsoft.Logic

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Logic/integrationAccounts/agreements/delete | Deletes the agreement in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/agreements/listContentCallbackUrl/action | Gets the callback URL for agreement content in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/agreements/read | Reads the agreement in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/agreements/write | Creates or updates the agreement in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/assemblies/delete | Deletes the assembly in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/assemblies/listContentCallbackUrl/action | Gets the callback URL for assembly content in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/assemblies/read | Reads the assembly in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/assemblies/write | Creates or updates the assembly in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/batchConfigurations/delete | Deletes the batch configuration in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/batchConfigurations/read | Reads the batch configuration in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/batchConfigurations/write | Creates or updates the batch configuration in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/certificates/delete | Deletes the certificate in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/certificates/read | Reads the certificate in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/certificates/write | Creates or updates the certificate in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/delete | Deletes the integration account. |
> | Action | Microsoft.Logic/integrationAccounts/join/action | Joins the Integration Account. |
> | Action | Microsoft.Logic/integrationAccounts/listCallbackUrl/action | Gets the callback URL for integration account. |
> | Action | Microsoft.Logic/integrationAccounts/listKeyVaultKeys/action | Gets the keys in the key vault. |
> | Action | Microsoft.Logic/integrationAccounts/logTrackingEvents/action | Logs the tracking events in the integration account. |
> | Action | Microsoft.Logic/integrationAccounts/maps/delete | Deletes the map in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/maps/listContentCallbackUrl/action | Gets the callback URL for map content in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/maps/read | Reads the map in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/maps/write | Creates or updates the map in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/partners/delete | Deletes the partner in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/partners/listContentCallbackUrl/action | Gets the callback URL for partner content in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/partners/read | Reads the parter in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/partners/write | Creates or updates the partner in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/providers/Microsoft.Insights/logDefinitions/read | Reads the Integration Account log definitions. |
> | Action | Microsoft.Logic/integrationAccounts/read | Reads the integration account. |
> | Action | Microsoft.Logic/integrationAccounts/regenerateAccessKey/action | Regenerates the access key secrets. |
> | Action | Microsoft.Logic/integrationAccounts/schemas/delete | Deletes the schema in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/schemas/listContentCallbackUrl/action | Gets the callback URL for schema content in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/schemas/read | Reads the schema in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/schemas/write | Creates or updates the schema in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/sessions/delete | Deletes the session in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/sessions/read | Reads the batch configuration in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/sessions/write | Creates or updates the session in integration account. |
> | Action | Microsoft.Logic/integrationAccounts/write | Creates or updates the integration account. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/delete | Deletes the integration service environment. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/join/action | Joins the Integration Service Environment. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/managedApis/apiOperations/read | Reads the integration service environment managed API operation. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/managedApis/read | Reads the integration service environment managed API. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/providers/Microsoft.Insights/metricDefinitions/read | Reads the integration service environment metric definitions. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/read | Reads the integration service environment. |
> | Action | Microsoft.Logic/integrationServiceEnvironments/write | Creates or updates the integration service environment. |
> | Action | Microsoft.Logic/locations/workflows/recommendOperationGroups/action | Gets the workflow recommend operation groups. |
> | Action | Microsoft.Logic/locations/workflows/validate/action | Validates the workflow. |
> | Action | Microsoft.Logic/operations/read | Gets the operation. |
> | Action | Microsoft.Logic/register/action | Registers the Microsoft.Logic resource provider for a given subscription. |
> | Action | Microsoft.Logic/workflows/accessKeys/delete | Deletes the access key. |
> | Action | Microsoft.Logic/workflows/accessKeys/list/action | Lists the access key secrets. |
> | Action | Microsoft.Logic/workflows/accessKeys/read | Reads the access key. |
> | Action | Microsoft.Logic/workflows/accessKeys/regenerate/action | Regenerates the access key secrets. |
> | Action | Microsoft.Logic/workflows/accessKeys/write | Creates or updates the access key. |
> | Action | Microsoft.Logic/workflows/delete | Deletes the workflow. |
> | Action | Microsoft.Logic/workflows/disable/action | Disables the workflow. |
> | Action | Microsoft.Logic/workflows/enable/action | Enables the workflow. |
> | Action | Microsoft.Logic/workflows/listCallbackUrl/action | Gets the callback URL for workflow. |
> | Action | Microsoft.Logic/workflows/listSwagger/action | Gets the workflow swagger definitions. |
> | Action | Microsoft.Logic/workflows/move/action | Moves Workflow from its existing subscription id, resource group, and/or name to a different subscription id, resource group, and/or name. |
> | Action | Microsoft.Logic/workflows/providers/Microsoft.Insights/diagnosticSettings/read | Reads the workflow diagnostic settings. |
> | Action | Microsoft.Logic/workflows/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the workflow diagnostic setting. |
> | Action | Microsoft.Logic/workflows/providers/Microsoft.Insights/logDefinitions/read | Reads the workflow log definitions. |
> | Action | Microsoft.Logic/workflows/providers/Microsoft.Insights/metricDefinitions/read | Reads the workflow metric definitions. |
> | Action | Microsoft.Logic/workflows/read | Reads the workflow. |
> | Action | Microsoft.Logic/workflows/regenerateAccessKey/action | Regenerates the access key secrets. |
> | Action | Microsoft.Logic/workflows/run/action | Starts a run of the workflow. |
> | Action | Microsoft.Logic/workflows/runs/actions/listExpressionTraces/action | Gets the workflow run action expression traces. |
> | Action | Microsoft.Logic/workflows/runs/actions/read | Reads the workflow run action. |
> | Action | Microsoft.Logic/workflows/runs/actions/repetitions/listExpressionTraces/action | Gets the workflow run action repetition expression traces. |
> | Action | Microsoft.Logic/workflows/runs/actions/repetitions/read | Reads the workflow run action repetition. |
> | Action | Microsoft.Logic/workflows/runs/actions/repetitions/requestHistories/read | Reads the workflow run repetition action request history. |
> | Action | Microsoft.Logic/workflows/runs/actions/requestHistories/read | Reads the workflow run action request history. |
> | Action | Microsoft.Logic/workflows/runs/actions/scoperepetitions/read | Reads the workflow run action scope repetition. |
> | Action | Microsoft.Logic/workflows/runs/cancel/action | Cancels the run of a workflow. |
> | Action | Microsoft.Logic/workflows/runs/operations/read | Reads the workflow run operation status. |
> | Action | Microsoft.Logic/workflows/runs/read | Reads the workflow run. |
> | Action | Microsoft.Logic/workflows/suspend/action | Suspends the workflow. |
> | Action | Microsoft.Logic/workflows/triggers/histories/read | Reads the trigger histories. |
> | Action | Microsoft.Logic/workflows/triggers/histories/resubmit/action | Resubmits the workflow trigger. |
> | Action | Microsoft.Logic/workflows/triggers/listCallbackUrl/action | Gets the callback URL for trigger. |
> | Action | Microsoft.Logic/workflows/triggers/read | Reads the trigger. |
> | Action | Microsoft.Logic/workflows/triggers/reset/action | Resets the trigger. |
> | Action | Microsoft.Logic/workflows/triggers/run/action | Executes the trigger. |
> | Action | Microsoft.Logic/workflows/triggers/setState/action | Sets the trigger state. |
> | Action | Microsoft.Logic/workflows/validate/action | Validates the workflow. |
> | Action | Microsoft.Logic/workflows/versions/read | Reads the workflow version. |
> | Action | Microsoft.Logic/workflows/versions/triggers/listCallbackUrl/action | Gets the callback URL for trigger. |
> | Action | Microsoft.Logic/workflows/write | Creates or updates the workflow. |

## Microsoft.MachineLearning

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.MachineLearning/commitmentPlans/commitmentAssociations/move/action | Move any Machine Learning Commitment Plan Association |
> | Action | Microsoft.MachineLearning/commitmentPlans/commitmentAssociations/read | Read any Machine Learning Commitment Plan Association |
> | Action | Microsoft.MachineLearning/commitmentPlans/delete | Delete any Machine Learning Commitment Plan |
> | Action | Microsoft.MachineLearning/commitmentPlans/join/action | Join any Machine Learning Commitment Plan |
> | Action | Microsoft.MachineLearning/commitmentPlans/read | Read any Machine Learning Commitment Plan |
> | Action | Microsoft.MachineLearning/commitmentPlans/write | Create or Update any Machine Learning Commitment Plan |
> | Action | Microsoft.MachineLearning/locations/operationresults/read | Get result of a Machine Learning Operation |
> | Action | Microsoft.MachineLearning/locations/operationsstatus/read | Get status of an ongoing Machine Learning Operation |
> | Action | Microsoft.MachineLearning/operations/read | Get Machine Learning Operations |
> | Action | Microsoft.MachineLearning/register/action | Registers the subscription for the machine learning web service resource provider and enables the creation of web services. |
> | Action | Microsoft.MachineLearning/skus/read | Get Machine Learning Commitment Plan SKUs |
> | Action | Microsoft.MachineLearning/webServices/action | Create regional Web Service Properties for supported regions |
> | Action | Microsoft.MachineLearning/webServices/delete | Delete any Machine Learning Web Service |
> | Action | Microsoft.MachineLearning/webServices/listkeys/read | Get keys to a Machine Learning Web Service |
> | Action | Microsoft.MachineLearning/webServices/read | Read any Machine Learning Web Service |
> | Action | Microsoft.MachineLearning/webServices/write | Create or Update any Machine Learning Web Service |
> | Action | Microsoft.MachineLearning/Workspaces/delete | Delete any Machine Learning Workspace |
> | Action | Microsoft.MachineLearning/Workspaces/listworkspacekeys/action | List keys for a Machine Learning Workspace |
> | Action | Microsoft.MachineLearning/Workspaces/read | Read any Machine Learning Workspace |
> | Action | Microsoft.MachineLearning/Workspaces/resyncstoragekeys/action | Resync keys of storage account configured for a Machine Learning Workspace |
> | Action | Microsoft.MachineLearning/Workspaces/write | Create or Update any Machine Learning Workspace |

## Microsoft.MachineLearningCompute

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.MachineLearningCompute/operationalizationClusters/checkUpdate/action | Check if updates are available for system services for the operationalization cluster |
> | Action | Microsoft.MachineLearningCompute/operationalizationClusters/delete | Delete any hosting account |
> | Action | Microsoft.MachineLearningCompute/operationalizationClusters/listKeys/action | List the keys associated with operationalization cluster |
> | Action | Microsoft.MachineLearningCompute/operationalizationClusters/read | Read any hosting account |
> | Action | Microsoft.MachineLearningCompute/operationalizationClusters/updateSystem/action | Update the system services in an operationalization cluster |
> | Action | Microsoft.MachineLearningCompute/operationalizationClusters/write | Create or update any hosting account |
> | Action | Microsoft.MachineLearningCompute/register/action | Registers subscription ID to the resource provider and enables the creation of a machine learning compute resources |

## Microsoft.MachineLearningModelManagement

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.MachineLearningModelManagement/accounts/delete | Delete any hosting account |
> | Action | Microsoft.MachineLearningModelManagement/accounts/read | Read any hosting account |
> | Action | Microsoft.MachineLearningModelManagement/accounts/write | Create or update any hosting account |
> | Action | Microsoft.MachineLearningModelManagement/register/action | Registers subscription ID to the resource provider and enables the creation of a hosting account |

## Microsoft.MachineLearningServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.MachineLearningServices/register/action | Registers the subscription for the Machine Learning Services Resource Provider |
> | Action | Microsoft.MachineLearningServices/workspaces/computes/delete | Deletes the compute resources in Machine Learning Services Workspace(s) |
> | Action | Microsoft.MachineLearningServices/workspaces/computes/listKeys/action | List secrets for compute resources in Machine Learning Services Workspace |
> | Action | Microsoft.MachineLearningServices/workspaces/computes/read | Gets the compute resources in Machine Learning Services Workspace(s) |
> | Action | Microsoft.MachineLearningServices/workspaces/computes/write | Creates or updates the compute resources in Machine Learning Services Workspace(s) |
> | Action | Microsoft.MachineLearningServices/workspaces/delete | Deletes the Machine Learning Services Workspace(s) |
> | Action | Microsoft.MachineLearningServices/workspaces/listKeys/action | List secrets for a Machine Learning Services Workspace |
> | Action | Microsoft.MachineLearningServices/workspaces/read | Gets the Machine Learning Services Workspace(s) |
> | Action | Microsoft.MachineLearningServices/workspaces/write | Creates or updates a Machine Learning Services Workspace(s) |

## Microsoft.ManagedIdentity

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ManagedIdentity/userAssignedIdentities/assign/action | RBAC action for assigning an existing user assigned identity to a resource |
> | Action | Microsoft.ManagedIdentity/userAssignedIdentities/delete | Deletes an existing user assigned identity |
> | Action | Microsoft.ManagedIdentity/userAssignedIdentities/read | Gets an existing user assigned identity |
> | Action | Microsoft.ManagedIdentity/userAssignedIdentities/write | Creates a new user assigned identity or updates the tags associated with an existing user assigned identity |

## Microsoft.ManagedLab

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ManagedLab/labAccounts/CreateLab/action | Create a lab in a lab account. |
> | Action | Microsoft.ManagedLab/labAccounts/delete | Delete lab accounts. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/delete | Delete labs. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/environmentSettings/delete | Delete environment setting. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/environmentSettings/environments/delete | Delete environments. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/environmentSettings/environments/read | Read environments. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/environmentSettings/environments/write | Add or modify environments. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/environmentSettings/read | Read environment setting. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/environmentSettings/write | Add or modify environment setting. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/labVms/delete | Delete lab virtual machines. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/labVms/read | Read lab virtual machines. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/labVms/write | Add or modify lab virtual machines. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/read | Read labs. |
> | Action | Microsoft.ManagedLab/labAccounts/labs/write | Add or modify labs. |
> | Action | Microsoft.ManagedLab/labAccounts/read | Read lab accounts. |
> | Action | Microsoft.ManagedLab/labAccounts/write | Add or modify lab accounts. |
> | Action | Microsoft.ManagedLab/locations/operations/read | Read operations. |
> | Action | Microsoft.ManagedLab/register/action | Registers the subscription |

## Microsoft.Management

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Management/checkNameAvailability/action | Checks if the specified management group name is valid and unique. |
> | Action | Microsoft.Management/getEntities/action | List all entities (Management Groups, Subscriptions, etc.) for the authenticated user. |
> | Action | Microsoft.Management/managementGroups/delete | Delete management group. |
> | Action | Microsoft.Management/managementGroups/read | List management groups for the authenticated user. |
> | Action | Microsoft.Management/managementGroups/subscriptions/delete | De-associates subscription from the management group. |
> | Action | Microsoft.Management/managementGroups/subscriptions/write | Associates existing subscription with the management group. |
> | Action | Microsoft.Management/managementGroups/write | Create or update a management group. |
> | Action | Microsoft.Management/register/action | Register the specified subscription with Microsoft.Management |

## Microsoft.Maps

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | DataAction | Microsoft.Maps/accounts/data/read | Grants data read access to a maps account. |
> | Action | Microsoft.Maps/accounts/delete | Delete a Maps Account. |
> | Action | Microsoft.Maps/accounts/eventGridFilters/delete | Delete an Event Grid filter |
> | Action | Microsoft.Maps/accounts/eventGridFilters/read | Get an Event Grid filter |
> | Action | Microsoft.Maps/accounts/eventGridFilters/write | Create or update an Event Grid filter |
> | Action | Microsoft.Maps/accounts/listKeys/action | List Maps Account keys |
> | Action | Microsoft.Maps/accounts/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Maps/accounts/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Maps/accounts/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Maps Accounts |
> | Action | Microsoft.Maps/accounts/read | Get a Maps Account. |
> | Action | Microsoft.Maps/accounts/regenerateKey/action | Generate new Maps Account primary or secondary key |
> | Action | Microsoft.Maps/accounts/write | Create or update a Maps Account. |
> | Action | Microsoft.Maps/register/action | Register the provider |

## Microsoft.Marketplace

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Marketplace/offerTypes/publishers/offers/plans/agreements/read | Returns an Agreement. |
> | Action | Microsoft.Marketplace/offerTypes/publishers/offers/plans/agreements/write | Accepts a signed agreement. |
> | Action | Microsoft.Marketplace/offerTypes/publishers/offers/plans/configs/importImage/action | Imports an image to the end user's ACR. |
> | Action | Microsoft.Marketplace/offerTypes/publishers/offers/plans/configs/read | Returns a config. |
> | Action | Microsoft.Marketplace/offerTypes/publishers/offers/plans/configs/write | Saves a config. |

## Microsoft.MarketplaceApps

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.MarketplaceApps/ClassicDevServices/delete | Does a DELETE operation on a classic dev service resource. |
> | Action | Microsoft.MarketplaceApps/ClassicDevServices/listSecrets/action | Gets a classic dev service resource management keys. |
> | Action | Microsoft.MarketplaceApps/ClassicDevServices/listSingleSignOnToken/action | Gets the Single Sign On URL for a classic dev service. |
> | Action | Microsoft.MarketplaceApps/ClassicDevServices/read | Does a GET operation on a classic dev service. |
> | Action | Microsoft.MarketplaceApps/ClassicDevServices/regenerateKey/action | Generates a classic dev service resource management keys. |
> | Action | Microsoft.MarketplaceApps/Operations/read | Read the operations for all resource types. |

## Microsoft.MarketplaceOrdering

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.MarketplaceOrdering/agreements/offers/plans/cancel/action | Cancel an agreement for a given marketplace item |
> | Action | Microsoft.MarketplaceOrdering/agreements/offers/plans/read | Return an agreement for a given marketplace item |
> | Action | Microsoft.MarketplaceOrdering/agreements/offers/plans/sign/action | Sign an agreement for a given marketplace item |
> | Action | Microsoft.MarketplaceOrdering/agreements/read | Return all agreements under given subscription |
> | Action | Microsoft.MarketplaceOrdering/offertypes/publishers/offers/plans/agreements/read | Get an agreement for a given marketplace virtual machine item |
> | Action | Microsoft.MarketplaceOrdering/offertypes/publishers/offers/plans/agreements/write | Sign or Cancel an agreement for a given marketplace virtual machine item |

## Microsoft.Media

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Media/checknameavailability/action | Checks if a Media Services account name is available |
> | Action | Microsoft.Media/locations/checkNameAvailability/action | Checks if a Media Services account name is available |
> | Action | Microsoft.Media/mediaservices/assets/delete | Delete any Asset |
> | Action | Microsoft.Media/mediaservices/assets/getEncryptionKey/action | Get Asset Encryption Key |
> | Action | Microsoft.Media/mediaservices/assets/listContainerSas/action | List Asset Container SAS URLs |
> | Action | Microsoft.Media/mediaservices/assets/read | Read any Asset |
> | Action | Microsoft.Media/mediaservices/assets/write | Create or Update any Asset |
> | Action | Microsoft.Media/mediaservices/contentKeyPolicies/delete | Delete any Content Key Policy |
> | Action | Microsoft.Media/mediaservices/contentKeyPolicies/getPolicyPropertiesWithSecrets/action | Get Policy Properties With Secrets |
> | Action | Microsoft.Media/mediaservices/contentKeyPolicies/read | Read any Content Key Policy |
> | Action | Microsoft.Media/mediaservices/contentKeyPolicies/write | Create or Update any Content Key Policy |
> | Action | Microsoft.Media/mediaservices/delete | Delete any Media Services Account |
> | Action | Microsoft.Media/mediaservices/eventGridFilters/delete | Delete any Event Grid Filter |
> | Action | Microsoft.Media/mediaservices/eventGridFilters/read | Read any Event Grid Filter |
> | Action | Microsoft.Media/mediaservices/eventGridFilters/write | Create or Update any Event Grid Filter |
> | Action | Microsoft.Media/mediaservices/liveEventOperations/read | Read any Live Event Operation |
> | Action | Microsoft.Media/mediaservices/liveEvents/delete | Delete any Live Event |
> | Action | Microsoft.Media/mediaservices/liveEvents/liveOutputs/delete | Delete any Live Output |
> | Action | Microsoft.Media/mediaservices/liveEvents/liveOutputs/read | Read any Live Output |
> | Action | Microsoft.Media/mediaservices/liveEvents/liveOutputs/write | Create or Update any Live Output |
> | Action | Microsoft.Media/mediaservices/liveEvents/read | Read any Live Event |
> | Action | Microsoft.Media/mediaservices/liveEvents/reset/action | Reset any Live Event Operation |
> | Action | Microsoft.Media/mediaservices/liveEvents/start/action | Start any Live Event Operation |
> | Action | Microsoft.Media/mediaservices/liveEvents/stop/action | Stop any Live Event Operation |
> | Action | Microsoft.Media/mediaservices/liveEvents/write | Create or Update any Live Event |
> | Action | Microsoft.Media/mediaservices/liveOutputOperations/read | Read any Live Output Operation |
> | Action | Microsoft.Media/mediaservices/read | Read any Media Services Account |
> | Action | Microsoft.Media/mediaservices/streamingEndpointOperations/read | Read any Streaming Endpoint Operation |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/delete | Delete any Streaming Endpoint |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/providers/Microsoft.Insights/metricDefinitions/read | Get list of Media Services Streaming Endpoint Metrics definitions. |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/read | Read any Streaming Endpoint |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/scale/action | Scale any Streaming Endpoint Operation |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/start/action | Start any Streaming Endpoint Operation |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/stop/action | Stop any Streaming Endpoint Operation |
> | Action | Microsoft.Media/mediaservices/streamingEndpoints/write | Create or Update any Streaming Endpoint |
> | Action | Microsoft.Media/mediaservices/streamingLocators/delete | Delete any Streaming Locator |
> | Action | Microsoft.Media/mediaservices/streamingLocators/listContentKeys/action | List Content Keys |
> | Action | Microsoft.Media/mediaservices/streamingLocators/listPaths/action | List Paths |
> | Action | Microsoft.Media/mediaservices/streamingLocators/read | Read any Streaming Locator |
> | Action | Microsoft.Media/mediaservices/streamingLocators/write | Create or Update any Streaming Locator |
> | Action | Microsoft.Media/mediaservices/streamingPolicies/delete | Delete any Streaming Policy |
> | Action | Microsoft.Media/mediaservices/streamingPolicies/read | Read any Streaming Policy |
> | Action | Microsoft.Media/mediaservices/streamingPolicies/write | Create or Update any Streaming Policy |
> | Action | Microsoft.Media/mediaservices/syncStorageKeys/action | Synchronize the Storage Keys for an attached Azure Storage account |
> | Action | Microsoft.Media/mediaservices/transforms/delete | Delete any Transform |
> | Action | Microsoft.Media/mediaservices/transforms/jobs/cancelJob/action | Cancel Job |
> | Action | Microsoft.Media/mediaservices/transforms/jobs/delete | Delete any Job |
> | Action | Microsoft.Media/mediaservices/transforms/jobs/read | Read any Job |
> | Action | Microsoft.Media/mediaservices/transforms/jobs/write | Create or Update any Job |
> | Action | Microsoft.Media/mediaservices/transforms/read | Read any Transform |
> | Action | Microsoft.Media/mediaservices/transforms/write | Create or Update any Transform |
> | Action | Microsoft.Media/mediaservices/write | Create or Update any Media Services Account |
> | Action | Microsoft.Media/operations/read | Get Available Operations |
> | Action | Microsoft.Media/register/action | Registers the subscription for the Media Services resource provider and enables the creation of Media Services accounts |
> | Action | Microsoft.Media/unregister/action | Unregisters the subscription for the Media Services resource provider |

## Microsoft.Migrate

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Migrate/locations/assessmentOptions/read | Gets the assessment options which are available in the given location |
> | Action | Microsoft.Migrate/locations/checknameavailability/action | Checks availability of the resouce name for the given subscription in the given location |
> | Action | Microsoft.Migrate/Operations/read | Lists operations available on Microsoft.Migrate resource provider |
> | Action | Microsoft.Migrate/projects/assessments/read | Lists assessments within a project |
> | Action | Microsoft.Migrate/projects/delete | Deletes the project |
> | Action | Microsoft.Migrate/projects/groups/assessments/assessedmachines/read | Get the properties of an assessed machine |
> | Action | Microsoft.Migrate/projects/groups/assessments/delete | Deletes an assessment |
> | Action | Microsoft.Migrate/projects/groups/assessments/downloadurl/action | Downloads an assessment report's URL |
> | Action | Microsoft.Migrate/projects/groups/assessments/read | Gets the properties of an assessment |
> | Action | Microsoft.Migrate/projects/groups/assessments/write | Creates a new assessment or updates an existing assessment |
> | Action | Microsoft.Migrate/projects/groups/delete | Deletes a group |
> | Action | Microsoft.Migrate/projects/groups/read | Get the properties of a group |
> | Action | Microsoft.Migrate/projects/groups/write | Creates a new group or updates an existing group |
> | Action | Microsoft.Migrate/projects/keys/action | Gets shared keys for the project |
> | Action | Microsoft.Migrate/projects/machines/read | Gets the properties of a machine |
> | Action | Microsoft.Migrate/projects/read | Gets the properties of a project |
> | Action | Microsoft.Migrate/projects/write | Creates a new project or updates an existing project |
> | Action | Microsoft.Migrate/register/action | Registers Subscription with Microsoft.Migrate resource provider |

## Microsoft.NetApp

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.NetApp/locations/operationresults/read | Reads an operation result resource. |
> | Action | Microsoft.NetApp/locations/read | Reads an availability check resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/delete | Deletes a pool resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/providers/Microsoft.Insights/diagnosticSettings/read | Deletes a pool resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/providers/Microsoft.Insights/diagnosticSettings/write | Deletes a pool resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/providers/Microsoft.Insights/metricDefinitions/read | Deletes a pool resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/read | Reads a pool resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/delete | Deletes a volume resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/MountTargets/delete | Deletes a mount target resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/MountTargets/read | Reads a mount target resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/MountTargets/write | Writes a mount target resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/providers/Microsoft.Insights/diagnosticSettings/read | Deletes a volume resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/providers/Microsoft.Insights/diagnosticSettings/write | Deletes a volume resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/providers/Microsoft.Insights/metricDefinitions/read | Deletes a volume resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/read | Reads a volume resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/Snapshots/delete | Deletes a snapshot resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/Snapshots/read | Reads a snapshot resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/Snapshots/write | Writes a snapshot resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/Volumes/write | Writes a volume resource. |
> | Action | Microsoft.NetApp/netAppAccounts/capacityPools/write | Writes a pool resource. |
> | Action | Microsoft.NetApp/netAppAccounts/delete | Deletes a account resource. |
> | Action | Microsoft.NetApp/netAppAccounts/read | Reads an account resource. |
> | Action | Microsoft.NetApp/netAppAccounts/write | Writes an account resource. |
> | Action | Microsoft.NetApp/Operations/read | Reads an operation resources. |

## Microsoft.Network

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Network/applicationGatewayAvailableSslOptions/predefinedPolicies/read | Application Gateway Ssl Predefined Policy |
> | Action | Microsoft.Network/applicationGatewayAvailableSslOptions/read | Application Gateway available Ssl Options |
> | Action | Microsoft.Network/applicationGatewayAvailableWafRuleSets/read | Gets Application Gateway Available Waf Rule Sets |
> | Action | Microsoft.Network/applicationGateways/backendAddressPools/join/action | Joins an application gateway backend address pool |
> | Action | Microsoft.Network/applicationGateways/backendhealth/action | Gets an application gateway backend health |
> | Action | Microsoft.Network/applicationGateways/delete | Deletes an application gateway |
> | Action | Microsoft.Network/applicationGateways/effectiveNetworkSecurityGroups/action | Get Route Table configured On Application Gateway |
> | Action | Microsoft.Network/applicationGateways/effectiveRouteTable/action | Get Route Table configured On Application Gateway |
> | Action | Microsoft.Network/applicationGateways/providers/Microsoft.Insights/logDefinitions/read | Gets the events for Application Gateway |
> | Action | Microsoft.Network/applicationGateways/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Application Gateway |
> | Action | Microsoft.Network/applicationGateways/read | Gets an application gateway |
> | Action | Microsoft.Network/applicationGateways/setSecurityCenterConfiguration/action | Sets Application Gateway Security Center Configuration |
> | Action | Microsoft.Network/applicationGateways/start/action | Starts an application gateway |
> | Action | Microsoft.Network/applicationGateways/stop/action | Stops an application gateway |
> | Action | Microsoft.Network/applicationGateways/write | Creates an application gateway or updates an application gateway |
> | Action | Microsoft.Network/applicationSecurityGroups/delete | Deletes an Application Security Group |
> | Action | Microsoft.Network/applicationSecurityGroups/joinIpConfiguration/action | Joins an IP Configuration to Application Security Groups. |
> | Action | Microsoft.Network/applicationSecurityGroups/joinNetworkSecurityRule/action | Joins a Security Rule to Application Security Groups. |
> | Action | Microsoft.Network/applicationSecurityGroups/read | Gets an Application Security Group ID. |
> | Action | Microsoft.Network/applicationSecurityGroups/write | Creates an Application Security Group, or updates an existing Application Security Group. |
> | Action | Microsoft.Network/azureFirewallFqdnTags/read | Gets Azure Firewall FQDN Tags |
> | Action | Microsoft.Network/azurefirewalls/delete | Delete Azure Firewall |
> | Action | Microsoft.Network/azurefirewalls/providers/Microsoft.Insights/logDefinitions/read | Gets the events for Azure Firewall |
> | Action | Microsoft.Network/azurefirewalls/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Azure Firewall |
> | Action | Microsoft.Network/azurefirewalls/read | Get Azure Firewall |
> | Action | Microsoft.Network/azurefirewalls/write | Creates or updates an Azure Firewall |
> | Action | Microsoft.Network/bgpServiceCommunities/read | Get Bgp Service Communities |
> | Action | Microsoft.Network/checkTrafficManagerNameAvailability/action | Checks the availability of a Traffic Manager Relative DNS name. |
> | Action | Microsoft.Network/connections/delete | Deletes VirtualNetworkGatewayConnection |
> | Action | Microsoft.Network/connections/providers/Microsoft.Insights/diagnosticSettings/read | Gets diagnostic settings for Connections |
> | Action | Microsoft.Network/connections/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates diagnostic settings for Connections |
> | Action | Microsoft.Network/connections/providers/Microsoft.Insights/metricDefinitions/read | Gets the metric definitions for Connections |
> | Action | Microsoft.Network/connections/read | Gets VirtualNetworkGatewayConnection |
> | Action | Microsoft.Network/connections/sharedkey/action | Get VirtualNetworkGatewayConnection SharedKey |
> | Action | Microsoft.Network/connections/sharedKey/read | Gets VirtualNetworkGatewayConnection SharedKey |
> | Action | Microsoft.Network/connections/sharedKey/write | Creates or updates an existing VirtualNetworkGatewayConnection SharedKey |
> | Action | Microsoft.Network/connections/vpndeviceconfigurationscript/action | Gets Vpn Device Configuration of VirtualNetworkGatewayConnection |
> | Action | Microsoft.Network/connections/write | Creates or updates an existing VirtualNetworkGatewayConnection |
> | Action | Microsoft.Network/ddosProtectionPlans/ddosProtectionPlanProxies/delete | Deletes a DDoS Protection Plan Proxy |
> | Action | Microsoft.Network/ddosProtectionPlans/ddosProtectionPlanProxies/read | Gets a DDoS Protection Plan Proxy definition |
> | Action | Microsoft.Network/ddosProtectionPlans/ddosProtectionPlanProxies/write | Creates a DDoS Protection Plan Proxy or updates and existing DDoS Protection Plan Proxy |
> | Action | Microsoft.Network/ddosProtectionPlans/delete | Deletes a DDoS Protection Plan |
> | Action | Microsoft.Network/ddosProtectionPlans/join/action | Joins a DDoS Protection Plan |
> | Action | Microsoft.Network/ddosProtectionPlans/read | Gets a DDoS Protection Plan |
> | Action | Microsoft.Network/ddosProtectionPlans/write | Creates a DDoS Protection Plan or updates a DDoS Protection Plan  |
> | Action | Microsoft.Network/dnsoperationresults/read | Gets results of a DNS operation |
> | Action | Microsoft.Network/dnsoperationstatuses/read | Gets status of a DNS operation  |
> | Action | Microsoft.Network/dnszones/A/delete | Remove the record set of a given name and type ‘A’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/A/read | Get the record set of type ‘A’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/A/write | Create or update a record set of type ‘A’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/AAAA/delete | Remove the record set of a given name and type ‘AAAA’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/AAAA/read | Get the record set of type ‘AAAA’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/AAAA/write | Create or update a record set of type ‘AAAA’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/all/read | Gets DNS record sets across types |
> | Action | Microsoft.Network/dnszones/CAA/delete | Remove the record set of a given name and type ‘CAA’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/CAA/read | Get the record set of type ‘CAA’, in JSON format. The record set contains the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/CAA/write | Create or update a record set of type ‘CAA’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/CNAME/delete | Remove the record set of a given name and type ‘CNAME’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/CNAME/read | Get the record set of type ‘CNAME’, in JSON format. The record set contains the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/CNAME/write | Create or update a record set of type ‘CNAME’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/delete | Delete the DNS zone, in JSON format. The zone properties include tags, etag, numberOfRecordSets, and maxNumberOfRecordSets. |
> | Action | Microsoft.Network/dnszones/MX/delete | Remove the record set of a given name and type ‘MX’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/MX/read | Get the record set of type ‘MX’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/MX/write | Create or update a record set of type ‘MX’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/NS/delete | Deletes the DNS record set of type NS |
> | Action | Microsoft.Network/dnszones/NS/read | Gets DNS record set of type NS |
> | Action | Microsoft.Network/dnszones/NS/write | Creates or updates DNS record set of type NS |
> | Action | Microsoft.Network/dnszones/providers/Microsoft.Insights/diagnosticSettings/read | Gets the DNS zone diagnostic settings |
> | Action | Microsoft.Network/dnszones/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the DNS zone diagnostic settings |
> | Action | Microsoft.Network/dnszones/providers/Microsoft.Insights/metricDefinitions/read | Gets the DNS zone metric definitions |
> | Action | Microsoft.Network/dnszones/PTR/delete | Remove the record set of a given name and type ‘PTR’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/PTR/read | Get the record set of type ‘PTR’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/PTR/write | Create or update a record set of type ‘PTR’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/read | Get the DNS zone, in JSON format. The zone properties include tags, etag, numberOfRecordSets, and maxNumberOfRecordSets. Note that this command does not retrieve the record sets contained within the zone. |
> | Action | Microsoft.Network/dnszones/recordsets/read | Gets DNS record sets across types |
> | Action | Microsoft.Network/dnszones/SOA/read | Gets DNS record set of type SOA |
> | Action | Microsoft.Network/dnszones/SOA/write | Creates or updates DNS record set of type SOA |
> | Action | Microsoft.Network/dnszones/SRV/delete | Remove the record set of a given name and type ‘SRV’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/SRV/read | Get the record set of type ‘SRV’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/SRV/write | Create or update record set of type SRV |
> | Action | Microsoft.Network/dnszones/TXT/delete | Remove the record set of a given name and type ‘TXT’ from a DNS zone. |
> | Action | Microsoft.Network/dnszones/TXT/read | Get the record set of type ‘TXT’, in JSON format. The record set contains a list of records as well as the TTL, tags, and etag. |
> | Action | Microsoft.Network/dnszones/TXT/write | Create or update a record set of type ‘TXT’ within a DNS zone. The records specified will replace the current records in the record set. |
> | Action | Microsoft.Network/dnszones/write | Create or update a DNS zone within a resource group.  Used to update the tags on a DNS zone resource. Note that this command can not be used to create or update record sets within the zone. |
> | Action | Microsoft.Network/expressRouteCircuits/authorizations/delete | Deletes an ExpressRouteCircuit Authorization |
> | Action | Microsoft.Network/expressRouteCircuits/authorizations/read | Gets an ExpressRouteCircuit Authorization |
> | Action | Microsoft.Network/expressRouteCircuits/authorizations/write | Creates or updates an existing ExpressRouteCircuit Authorization |
> | Action | Microsoft.Network/expressRouteCircuits/delete | Deletes an ExpressRouteCircuit |
> | Action | Microsoft.Network/expressRouteCircuits/join/action | Joins an Express Route Circuit |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/arpTables/action | Gets an ExpressRouteCircuit Peering ArpTable |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/connections/delete | Deletes an ExpressRouteCircuit Connection |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/connections/read | Gets an ExpressRouteCircuit Connection |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/connections/write | Creates or updates an existing ExpressRouteCircuit Connection Resource |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/delete | Deletes an ExpressRouteCircuit Peering |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/providers/Microsoft.Insights/diagnosticSettings/read | Gets diagnostic settings for ExpressRoute Circuit Peerings |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates diagnostic settings for ExpressRoute Circuit Peerings |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/providers/Microsoft.Insights/metricDefinitions/read | Gets the metric definitions for ExpressRoute Circuit Peerings |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/read | Gets an ExpressRouteCircuit Peering |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/routeTables/action | Gets an ExpressRouteCircuit Peering RouteTable |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/routeTablesSummary/action | Gets an ExpressRouteCircuit Peering RouteTable Summary |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/stats/read | Gets an ExpressRouteCircuit Peering Stat |
> | Action | Microsoft.Network/expressRouteCircuits/peerings/write | Creates or updates an existing ExpressRouteCircuit Peering |
> | Action | Microsoft.Network/expressRouteCircuits/providers/Microsoft.Insights/diagnosticSettings/read | Gets diagnostic settings for ExpressRoute Circuits |
> | Action | Microsoft.Network/expressRouteCircuits/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates diagnostic settings for ExpressRoute Circuits |
> | Action | Microsoft.Network/expressRouteCircuits/providers/Microsoft.Insights/logDefinitions/read | Get the events for ExpressRoute Circuits |
> | Action | Microsoft.Network/expressRouteCircuits/providers/Microsoft.Insights/metricDefinitions/read | Gets the metric definitions for ExpressRoute Circuits |
> | Action | Microsoft.Network/expressRouteCircuits/read | Get an ExpressRouteCircuit |
> | Action | Microsoft.Network/expressRouteCircuits/stats/read | Gets an ExpressRouteCircuit Stat |
> | Action | Microsoft.Network/expressRouteCircuits/write | Creates or updates an existing ExpressRouteCircuit |
> | Action | Microsoft.Network/expressRouteCrossConnections/delete | Delete Express Route Cross Connection |
> | Action | Microsoft.Network/expressRouteCrossConnections/join/action | Joins an Express Route Cross Connection |
> | Action | Microsoft.Network/expressRouteCrossConnections/peerings/arpTables/action | Gets an Express Route Cross Connection Peering Arp Table |
> | Action | Microsoft.Network/expressRouteCrossConnections/peerings/delete | Deletes an Express Route Cross Connection Peering |
> | Action | Microsoft.Network/expressRouteCrossConnections/peerings/read | Gets an Express Route Cross Connection Peering |
> | Action | Microsoft.Network/expressRouteCrossConnections/peerings/routeTables/action | Gets an Express Route Cross Connection Peering Route Table |
> | Action | Microsoft.Network/expressRouteCrossConnections/peerings/routeTableSummary/action | Gets an Express Route Cross Connection Peering Route Table Summary |
> | Action | Microsoft.Network/expressRouteCrossConnections/peerings/write | Creates an Express Route Cross Connection Peering or Updates an existing Express Route Cross Connection Peering |
> | Action | Microsoft.Network/expressRouteCrossConnections/read | Get Express Route Cross Connection |
> | Action | Microsoft.Network/expressRouteCrossConnections/write | Create or Update Express Route Cross Connection |
> | Action | Microsoft.Network/expressRouteGateways/delete | Delete Express Route Gateway |
> | Action | Microsoft.Network/expressRouteGateways/expressRouteConnections/delete | Deletes an Express Route Connection |
> | Action | Microsoft.Network/expressRouteGateways/expressRouteConnections/read | Gets an Express Route Connection |
> | Action | Microsoft.Network/expressRouteGateways/expressRouteConnections/write | Creates an Express Route Connection or Updates an existing Express Route Connection |
> | Action | Microsoft.Network/expressRouteGateways/join/action | Joins an Express Route Gateway |
> | Action | Microsoft.Network/expressRouteGateways/read | Get Express Route Gateway |
> | Action | Microsoft.Network/expressRouteGateways/write | Create or Update Express Route Gateway |
> | Action | Microsoft.Network/expressRoutePorts/delete | Deletes ExpressRoutePorts |
> | Action | Microsoft.Network/expressRoutePorts/join/action | Joins ExpressRoutePorts |
> | Action | Microsoft.Network/expressRoutePorts/links/read | Gets ExpressRouteLink |
> | Action | Microsoft.Network/expressRoutePorts/providers/Microsoft.Insights/metricDefinitions/read | Gets the metric definitions for ExpressRoute Ports |
> | Action | Microsoft.Network/expressRoutePorts/read | Gets ExpressRoutePorts |
> | Action | Microsoft.Network/expressRoutePorts/write | Creates or updates ExpressRoutePorts |
> | Action | Microsoft.Network/expressRoutePortsLocations/read | Get Express Route Ports Locations |
> | Action | Microsoft.Network/expressRouteServiceProviders/read | Gets Express Route Service Providers |
> | Action | Microsoft.Network/frontdoors/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic setting for the Frontdoor resource |
> | Action | Microsoft.Network/frontdoors/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the Frontdoor resource |
> | Action | Microsoft.Network/frontdoors/providers/Microsoft.Insights/logDefinitions/read | Get available logs for Frontdoor resources |
> | Action | Microsoft.Network/frontdoors/providers/Microsoft.Insights/metricDefinitions/read | Get available metrics for Frontdoor resources |
> | Action | Microsoft.Network/frontdoors/read | Get Frontdoor |
> | Action | Microsoft.Network/getDnsResourceReference/action | DNS alias resource dependency request |
> | Action | Microsoft.Network/interfaceEndpoints/delete | Deletes an interface endpoint resource. |
> | Action | Microsoft.Network/interfaceEndpoints/read | Gets an interface endpoint resource. |
> | Action | Microsoft.Network/interfaceEndpoints/write | Creates a new interface endpoint, or updates an existing interface endpoint. |
> | Action | Microsoft.Network/internalNotify/action | DNS alias resource notification |
> | Action | Microsoft.Network/loadBalancers/backendAddressPools/join/action | Joins a load balancer backend address pool |
> | Action | Microsoft.Network/loadBalancers/backendAddressPools/read | Gets a load balancer backend address pool definition |
> | Action | Microsoft.Network/loadBalancers/delete | Deletes a load balancer |
> | Action | Microsoft.Network/loadBalancers/inboundNatPools/join/action | Joins a load balancer inbound nat pool |
> | Action | Microsoft.Network/loadBalancers/inboundNatPools/read | Gets a load balancer inbound nat pool definition |
> | Action | Microsoft.Network/loadBalancers/inboundNatRules/delete | Deletes a load balancer inbound nat rule |
> | Action | Microsoft.Network/loadBalancers/inboundNatRules/join/action | Joins a load balancer inbound nat rule |
> | Action | Microsoft.Network/loadBalancers/inboundNatRules/read | Gets a load balancer inbound nat rule definition |
> | Action | Microsoft.Network/loadBalancers/inboundNatRules/write | Creates a load balancer inbound nat rule or updates an existing load balancer inbound nat rule |
> | Action | Microsoft.Network/loadBalancers/loadBalancingRules/read | Gets a load balancer load balancing rule definition |
> | Action | Microsoft.Network/loadBalancers/networkInterfaces/read | Gets references to all the network interfaces under a load balancer |
> | Action | Microsoft.Network/loadBalancers/outboundRules/read | Gets a load balancer outbound rule definition |
> | Action | Microsoft.Network/loadBalancers/probes/join/action | Allows using probes of a load balancer. For example, with this permission healthProbe property of VM scale set can reference the probe. |
> | Action | Microsoft.Network/loadBalancers/probes/read | Gets a load balancer probe |
> | Action | Microsoft.Network/loadBalancers/providers/Microsoft.Insights/diagnosticSettings/read | Gets the Load Balancer Diagnostic Settings |
> | Action | Microsoft.Network/loadBalancers/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the Load Balancer Diagnostic Settings |
> | Action | Microsoft.Network/loadBalancers/providers/Microsoft.Insights/logDefinitions/read | Gets the events for Load Balancer |
> | Action | Microsoft.Network/loadBalancers/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Load Balancer |
> | Action | Microsoft.Network/loadBalancers/read | Gets a load balancer definition |
> | Action | Microsoft.Network/loadBalancers/virtualMachines/read | Gets references to all the virtual machines under a load balancer |
> | Action | Microsoft.Network/loadBalancers/write | Creates a load balancer or updates an existing load balancer |
> | Action | Microsoft.Network/localnetworkgateways/delete | Deletes LocalNetworkGateway |
> | Action | Microsoft.Network/localnetworkgateways/read | Gets LocalNetworkGateway |
> | Action | Microsoft.Network/localnetworkgateways/write | Creates or updates an existing LocalNetworkGateway |
> | Action | Microsoft.Network/locations/availableDelegations/read | Gets Available Delegations |
> | Action | Microsoft.Network/locations/bareMetalTenants/action | Allocates or validates a Bare Metal Tenant |
> | Action | Microsoft.Network/locations/checkAcceleratedNetworkingSupport/action | Checks Accelerated Networking support |
> | Action | Microsoft.Network/locations/checkDnsNameAvailability/read | Checks if dns label is available at the specified location |
> | Action | Microsoft.Network/locations/effectiveResourceOwnership/action | Gets Effective  Resource Ownership |
> | Action | Microsoft.Network/locations/operationResults/read | Gets operation result of an async POST or DELETE operation |
> | Action | Microsoft.Network/locations/operations/read | Gets operation resource that represents status of an asynchronous operation |
> | Action | Microsoft.Network/locations/setResourceOwnership/action | Sets Resource Ownership |
> | Action | Microsoft.Network/locations/supportedVirtualMachineSizes/read | Gets supported virtual machines sizes |
> | Action | Microsoft.Network/locations/usages/read | Gets the resources usage metrics |
> | Action | Microsoft.Network/locations/validateResourceOwnership/action | Validates Resource Ownership |
> | Action | Microsoft.Network/locations/virtualNetworkAvailableEndpointServices/read | Gets a list of available Virtual Network Endpoint Services |
> | Action | Microsoft.Network/networkIntentPolicies/delete | Deletes an Network Intent Policy |
> | Action | Microsoft.Network/networkIntentPolicies/read | Gets an Network Intent Policy Description |
> | Action | Microsoft.Network/networkIntentPolicies/write | Creates an Network Intent Policy or updates an existing Network Intent Policy |
> | Action | Microsoft.Network/networkInterfaces/delete | Deletes a network interface |
> | Action | Microsoft.Network/networkInterfaces/diagnosticIdentity/read | Gets Diagnostic Identity Of The Resource |
> | Action | Microsoft.Network/networkInterfaces/effectiveNetworkSecurityGroups/action | Get Network Security Groups configured On Network Interface Of The Vm |
> | Action | Microsoft.Network/networkInterfaces/effectiveRouteTable/action | Get Route Table configured On Network Interface Of The Vm |
> | Action | Microsoft.Network/networkInterfaces/ipconfigurations/join/action | Joins a Network Interface IP Configuration. |
> | Action | Microsoft.Network/networkInterfaces/ipconfigurations/read | Gets a network interface ip configuration definition.  |
> | Action | Microsoft.Network/networkInterfaces/join/action | Joins a Virtual Machine to a network interface |
> | Action | Microsoft.Network/networkInterfaces/joinViaPrivateIp/action | Joins a resource to a Network interface via a Service Association |
> | Action | Microsoft.Network/networkInterfaces/loadBalancers/read | Gets all the load balancers that the network interface is part of |
> | Action | Microsoft.Network/networkInterfaces/providers/Microsoft.Insights/metricDefinitions/read | Gets available metrics for the Network Interface |
> | Action | Microsoft.Network/networkInterfaces/read | Gets a network interface definition.  |
> | Action | Microsoft.Network/networkInterfaces/serviceAssociations/delete | Deletes a Service Association |
> | Action | Microsoft.Network/networkInterfaces/serviceAssociations/read | Gets a Service Association Definition |
> | Action | Microsoft.Network/networkInterfaces/serviceAssociations/validate/action | Validates a Service Association |
> | Action | Microsoft.Network/networkInterfaces/serviceAssociations/write | Creates a new Service Association or modifies an existing Service Association |
> | Action | Microsoft.Network/networkInterfaces/tapConfigurations/delete | Deletes a Network Interface Tap Configuration. |
> | Action | Microsoft.Network/networkInterfaces/tapConfigurations/read | Gets a Network Interface Tap Configuration. |
> | Action | Microsoft.Network/networkInterfaces/tapConfigurations/write | Creates a Network Interface Tap Configuration or updates an existing Network Interface Tap Configuration. |
> | Action | Microsoft.Network/networkInterfaces/write | Creates a network interface or updates an existing network interface.  |
> | Action | Microsoft.Network/networkProfiles/delete | Deletes a Network Profile |
> | Action | Microsoft.Network/networkProfiles/read | Gets a Network Profile |
> | Action | Microsoft.Network/networkProfiles/removeContainers/action | Removes Containers |
> | Action | Microsoft.Network/networkProfiles/setContainers/action | Sets Containers |
> | Action | Microsoft.Network/networkProfiles/setNetworkInterfaces/action | Sets Container Network Interfaces |
> | Action | Microsoft.Network/networkProfiles/write | Creates or updates a Network Profile |
> | Action | Microsoft.Network/networkSecurityGroups/defaultSecurityRules/read | Gets a default security rule definition |
> | Action | Microsoft.Network/networkSecurityGroups/delete | Deletes a network security group |
> | Action | Microsoft.Network/networkSecurityGroups/join/action | Joins a network security group |
> | Action | Microsoft.Network/networksecuritygroups/providers/Microsoft.Insights/diagnosticSettings/read | Gets the Network Security Groups Diagnostic Settings |
> | Action | Microsoft.Network/networksecuritygroups/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the Network Security Groups diagnostic settings, this operation is supplemented by insghts resource provider. |
> | Action | Microsoft.Network/networksecuritygroups/providers/Microsoft.Insights/logDefinitions/read | Gets the events for network security group |
> | Action | Microsoft.Network/networkSecurityGroups/read | Gets a network security group definition |
> | Action | Microsoft.Network/networkSecurityGroups/securityRules/delete | Deletes a security rule |
> | Action | Microsoft.Network/networkSecurityGroups/securityRules/read | Gets a security rule definition |
> | Action | Microsoft.Network/networkSecurityGroups/securityRules/write | Creates a security rule or updates an existing security rule |
> | Action | Microsoft.Network/networkSecurityGroups/write | Creates a network security group or updates an existing network security group |
> | Action | Microsoft.Network/networkWatchers/availableProvidersList/action | Returns all available internet service providers for a specified Azure region. |
> | Action | Microsoft.Network/networkWatchers/azureReachabilityReport/action | Returns the relative latency score for internet service providers from a specified location to Azure regions. |
> | Action | Microsoft.Network/networkWatchers/configureFlowLog/action | Configures flow logging for a target resource. |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/delete | Deletes a Connection Monitor |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic settings of Connection Monitor |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the Connection Monitor Diagnostic Settings |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Connection Monitor |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/query/action | Query monitoring connectivity between specified endpoints |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/read | Get Connection Monitor details |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/start/action | Start monitoring connectivity between specified endpoints |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/stop/action | Stop/pause monitoring connectivity between specified endpoints |
> | Action | Microsoft.Network/networkWatchers/connectionMonitors/write | Creates a Connection Monitor |
> | Action | Microsoft.Network/networkWatchers/connectivityCheck/action | Verifies the possibility of establishing a direct TCP connection from a virtual machine to a given endpoint including another VM or an arbitrary remote server. |
> | Action | Microsoft.Network/networkWatchers/delete | Deletes a network watcher |
> | Action | Microsoft.Network/networkWatchers/ipFlowVerify/action | Returns whether the packet is allowed or denied to or from a particular destination. |
> | Action | Microsoft.Network/networkWatchers/lenses/delete | Deletes a Lens |
> | Action | Microsoft.Network/networkWatchers/lenses/query/action | Query monitoring network traffic on a specified endpoint |
> | Action | Microsoft.Network/networkWatchers/lenses/read | Get Lens details |
> | Action | Microsoft.Network/networkWatchers/lenses/start/action | Start monitoring network traffic on a specified endpoint |
> | Action | Microsoft.Network/networkWatchers/lenses/stop/action | Stop/pause monitoring network traffic on a specified endpoint |
> | Action | Microsoft.Network/networkWatchers/lenses/write | Creates a Lens |
> | Action | Microsoft.Network/networkWatchers/networkConfigurationDiagnostic/action | Diagnostic of network configuration. |
> | Action | Microsoft.Network/networkWatchers/nextHop/action | For a specified target and destination IP address, return the next hop type and next hope IP address. |
> | Action | Microsoft.Network/networkWatchers/packetCaptures/delete | Deletes a packet capture |
> | Action | Microsoft.Network/networkWatchers/packetCaptures/queryStatus/action | Gets information about properties and status of a packet capture resource. |
> | Action | Microsoft.Network/networkWatchers/packetCaptures/read | Get the packet capture definition |
> | Action | Microsoft.Network/networkWatchers/packetCaptures/stop/action | Stop the running packet capture session. |
> | Action | Microsoft.Network/networkWatchers/packetCaptures/write | Creates a packet capture |
> | Action | Microsoft.Network/networkWatchers/pingMeshes/delete | Deletes a PingMesh |
> | Action | Microsoft.Network/networkWatchers/pingMeshes/read | Get PingMesh details |
> | Action | Microsoft.Network/networkWatchers/pingMeshes/start/action | Start PingMesh between specified VMs |
> | Action | Microsoft.Network/networkWatchers/pingMeshes/stop/action | Stop PingMesh between specified VMs |
> | Action | Microsoft.Network/networkWatchers/pingMeshes/write | Creates a PingMesh |
> | Action | Microsoft.Network/networkWatchers/queryConnectionMonitors/action | Batch query monitoring connectivity between specified endpoints |
> | Action | Microsoft.Network/networkWatchers/queryFlowLogStatus/action | Gets the status of flow logging on a resource. |
> | Action | Microsoft.Network/networkWatchers/queryTroubleshootResult/action | Gets the troubleshooting result from the previously run or currently running troubleshooting operation. |
> | Action | Microsoft.Network/networkWatchers/read | Get the network watcher definition |
> | Action | Microsoft.Network/networkWatchers/securityGroupView/action | View the configured and effective network security group rules applied on a VM. |
> | Action | Microsoft.Network/networkWatchers/topology/action | Gets a network level view of resources and their relationships in a resource group. |
> | Action | Microsoft.Network/networkWatchers/troubleshoot/action | Starts troubleshooting on a Networking resource in Azure. |
> | Action | Microsoft.Network/networkWatchers/write | Creates a network watcher or updates an existing network watcher |
> | Action | Microsoft.Network/operations/read | Get Available Operations |
> | Action | Microsoft.Network/p2sVpnGateways/delete | Deletes a P2SVpnGateway. |
> | Action | Microsoft.Network/p2sVpnGateways/generatevpnprofile/action | Generate Vpn Profile for P2SVpnGateway |
> | Action | Microsoft.Network/p2sVpnGateways/read | Gets a P2SVpnGateway. |
> | Action | Microsoft.Network/p2sVpnGateways/write | Puts a P2SVpnGateway. |
> | Action | Microsoft.Network/privateLinkServices/delete | Deletes an private link service resource. |
> | Action | Microsoft.Network/privateLinkServices/interfaceEndpointConnections/delete | Deletes an interface endpoint connection. |
> | Action | Microsoft.Network/privateLinkServices/interfaceEndpointConnections/read | Gets an interface endpoint connection definition. |
> | Action | Microsoft.Network/privateLinkServices/interfaceEndpointConnections/write | Creates a new interface endpoint connection, or updates an existing interface endpoint connection. |
> | Action | Microsoft.Network/privateLinkServices/read | Gets an private link service resource. |
> | Action | Microsoft.Network/privateLinkServices/write | Creates a new private link service, or updates an existing private link service. |
> | Action | Microsoft.Network/publicIPAddresses/delete | Deletes a public Ip address. |
> | Action | Microsoft.Network/publicIPAddresses/dnsAliases/delete | Deletes a Public Ip Address Dns Alias resource |
> | Action | Microsoft.Network/publicIPAddresses/dnsAliases/read | Gets a Public Ip Address Dns Alias resource |
> | Action | Microsoft.Network/publicIPAddresses/dnsAliases/write | Creates a Public Ip Address Dns Alias resource |
> | Action | Microsoft.Network/publicIPAddresses/join/action | Joins a public ip address |
> | Action | Microsoft.Network/publicIPAddresses/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic settings of Public IP Address |
> | Action | Microsoft.Network/publicIPAddresses/providers/Microsoft.Insights/diagnosticSettings/write | Create or update the diagnostic settings of Public IP Address |
> | Action | Microsoft.Network/publicIPAddresses/providers/Microsoft.Insights/logDefinitions/read | Get the log definitions of Public IP Address |
> | Action | Microsoft.Network/publicIPAddresses/providers/Microsoft.Insights/metricDefinitions/read | Get the metrics definitions of Public IP Address |
> | Action | Microsoft.Network/publicIPAddresses/read | Gets a public ip address definition. |
> | Action | Microsoft.Network/publicIPAddresses/write | Creates a public Ip address or updates an existing public Ip address.  |
> | Action | Microsoft.Network/publicIPPrefixes/delete | Deletes A Public Ip Prefix |
> | Action | Microsoft.Network/publicIPPrefixes/join/action | Joins a PublicIPPrefix |
> | Action | Microsoft.Network/publicIPPrefixes/read | Gets a Public Ip Prefix Definition |
> | Action | Microsoft.Network/publicIPPrefixes/write | Creates A Public Ip Prefix Or Updates An Existing Public Ip Prefix |
> | Action | Microsoft.Network/register/action | Registers the subscription |
> | Action | Microsoft.Network/routeFilters/delete | Deletes a route filter definition |
> | Action | Microsoft.Network/routeFilters/join/action | Joins a route filter |
> | Action | Microsoft.Network/routeFilters/read | Gets a route filter definition |
> | Action | Microsoft.Network/routeFilters/routeFilterRules/delete | Deletes a route filter rule definition |
> | Action | Microsoft.Network/routeFilters/routeFilterRules/read | Gets a route filter rule definition |
> | Action | Microsoft.Network/routeFilters/routeFilterRules/write | Creates a route filter rule or Updates an existing route filter rule |
> | Action | Microsoft.Network/routeFilters/write | Creates a route filter or Updates an existing rotue filter |
> | Action | Microsoft.Network/routeTables/delete | Deletes a route table definition |
> | Action | Microsoft.Network/routeTables/join/action | Joins a route table |
> | Action | Microsoft.Network/routeTables/read | Gets a route table definition |
> | Action | Microsoft.Network/routeTables/routes/delete | Deletes a route definition |
> | Action | Microsoft.Network/routeTables/routes/read | Gets a route definition |
> | Action | Microsoft.Network/routeTables/routes/write | Creates a route or Updates an existing route |
> | Action | Microsoft.Network/routeTables/write | Creates a route table or Updates an existing rotue table |
> | Action | Microsoft.Network/securegateways/applicationRuleCollections/delete | Deletes an Application Rule Collection for a Secure Gateway |
> | Action | Microsoft.Network/securegateways/applicationRuleCollections/read | Retrieve an Application Rule Collection for a given Secure Gateway |
> | Action | Microsoft.Network/securegateways/applicationRuleCollections/write | Creates or updates an Application Rule Collection for a Secure Gateway |
> | Action | Microsoft.Network/securegateways/delete | Delete Secure Gateway |
> | Action | Microsoft.Network/securegateways/networkRuleCollections/delete | Deletes a Network Rule Collection for a Secure Gateway |
> | Action | Microsoft.Network/securegateways/networkRuleCollections/read | Retrieve a Network Rule Collection for a given Secure Gateway |
> | Action | Microsoft.Network/securegateways/networkRuleCollections/write | Creates or updates a Network Rule Collection for a Secure Gateway |
> | Action | Microsoft.Network/securegateways/providers/Microsoft.Insights/logDefinitions/read | Gets the events for Azure Firewall |
> | Action | Microsoft.Network/securegateways/read | Get Secure Gateway |
> | Action | Microsoft.Network/securegateways/write | Creates or updates a Secure Gateway |
> | Action | Microsoft.Network/serviceEndpointPolicies/delete | Deletes a Service Endpoint Policy |
> | Action | Microsoft.Network/serviceEndpointPolicies/join/action | Joins a Service Endpoint Policy |
> | Action | Microsoft.Network/serviceEndpointPolicies/joinSubnet/action | Joins a Subnet To Service Endpoint Policies |
> | Action | Microsoft.Network/serviceEndpointPolicies/read | Gets a Service Endpoint Policy Description |
> | Action | Microsoft.Network/serviceEndpointPolicies/serviceEndpointPolicyDefinitions/delete | Deletes a Service Endpoint Policy Definition |
> | Action | Microsoft.Network/serviceEndpointPolicies/serviceEndpointPolicyDefinitions/read | Gets a Service Endpoint Policy Definition Decription |
> | Action | Microsoft.Network/serviceEndpointPolicies/serviceEndpointPolicyDefinitions/write | Creates a Service Endpoint Policy Definition or updates an existing Service Endpoint Policy Definition |
> | Action | Microsoft.Network/serviceEndpointPolicies/write | Creates a Service Endpoint Policy or updates an existing Service Endpoint Policy |
> | Action | Microsoft.Network/trafficManagerGeographicHierarchies/read | Gets the Traffic Manager Geographic Hierarchy containing regions which can be used with the Geographic traffic routing method |
> | Action | Microsoft.Network/trafficManagerProfiles/azureEndpoints/delete | Deletes an Azure Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted Azure Endpoint. |
> | Action | Microsoft.Network/trafficManagerProfiles/azureEndpoints/read | Gets an Azure Endpoint which belongs to a Traffic Manager Profile, including all the properties of that Azure Endpoint. |
> | Action | Microsoft.Network/trafficManagerProfiles/azureEndpoints/write | Add a new Azure Endpoint in an existing Traffic Manager Profile or update the properties of an existing Azure Endpoint in that Traffic Manager Profile. |
> | Action | Microsoft.Network/trafficManagerProfiles/delete | Delete the Traffic Manager profile. All settings associated with the Traffic Manager profile will be lost, and the profile can no longer be used to route traffic. |
> | Action | Microsoft.Network/trafficManagerProfiles/externalEndpoints/delete | Deletes an External Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted External Endpoint. |
> | Action | Microsoft.Network/trafficManagerProfiles/externalEndpoints/read | Gets an External Endpoint which belongs to a Traffic Manager Profile, including all the properties of that External Endpoint. |
> | Action | Microsoft.Network/trafficManagerProfiles/externalEndpoints/write | Add a new External Endpoint in an existing Traffic Manager Profile or update the properties of an existing External Endpoint in that Traffic Manager Profile. |
> | Action | Microsoft.Network/trafficManagerProfiles/heatMaps/read | Gets the Traffic Manager Heat Map for the given Traffic Manager profile which contains query counts and latency data by location and source IP. |
> | Action | Microsoft.Network/trafficManagerProfiles/nestedEndpoints/delete | Deletes an Nested Endpoint from an existing Traffic Manager Profile. Traffic Manager will stop routing traffic to the deleted Nested Endpoint. |
> | Action | Microsoft.Network/trafficManagerProfiles/nestedEndpoints/read | Gets an Nested Endpoint which belongs to a Traffic Manager Profile, including all the properties of that Nested Endpoint. |
> | Action | Microsoft.Network/trafficManagerProfiles/nestedEndpoints/write | Add a new Nested Endpoint in an existing Traffic Manager Profile or update the properties of an existing Nested Endpoint in that Traffic Manager Profile. |
> | Action | Microsoft.Network/trafficManagerProfiles/providers/Microsoft.Insights/diagnosticSettings/read | Gets the Traffic Manager Diagnostic Settings |
> | Action | Microsoft.Network/trafficManagerProfiles/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the Traffic Manager diagnostic settings, this operation is supplemented by insights resource provider. |
> | Action | Microsoft.Network/trafficManagerProfiles/providers/Microsoft.Insights/logDefinitions/read | Gets the events for Traffic Manager |
> | Action | Microsoft.Network/trafficManagerProfiles/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Traffic Manager. |
> | Action | Microsoft.Network/trafficManagerProfiles/read | Get the Traffic Manager profile configuration. This includes DNS settings, traffic routing settings, endpoint monitoring settings, and the list of endpoints routed by this Traffic Manager profile. |
> | Action | Microsoft.Network/trafficManagerProfiles/write | Create a Traffic Manager profile, or modify the configuration of an existing Traffic Manager profile.<br>This includes enabling or disabling a profile and modifying DNS settings, traffic routing settings, or endpoint monitoring settings.<br>Endpoints routed by the Traffic Manager profile can be added, removed, enabled or disabled. |
> | Action | Microsoft.Network/trafficManagerUserMetricsKeys/delete | Deletes the subscription-level key used for Realtime User Metrics collection. |
> | Action | Microsoft.Network/trafficManagerUserMetricsKeys/read | Gets the subscription-level key used for Realtime User Metrics collection. |
> | Action | Microsoft.Network/trafficManagerUserMetricsKeys/write | Creates a new subscription-level key to be used for Realtime User Metrics collection. |
> | Action | Microsoft.Network/unregister/action | Unregisters the subscription |
> | Action | Microsoft.Network/virtualHubs/delete | Deletes a Virtual Hub |
> | Action | Microsoft.Network/virtualHubs/hubVirtualNetworkConnections/delete | Deletes a HubVirtualNetworkConnection |
> | Action | Microsoft.Network/virtualHubs/hubVirtualNetworkConnections/read | Get a HubVirtualNetworkConnection |
> | Action | Microsoft.Network/virtualHubs/hubVirtualNetworkConnections/write | Create or update a HubVirtualNetworkConnection |
> | Action | Microsoft.Network/virtualHubs/read | Get a Virtual Hub |
> | Action | Microsoft.Network/virtualHubs/write | Create or update a Virtual Hub |
> | Action | microsoft.network/virtualnetworkgateways/connections/read | Get VirtualNetworkGatewayConnection |
> | Action | Microsoft.Network/virtualNetworkGateways/delete | Deletes a virtualNetworkGateway |
> | Action | microsoft.network/virtualnetworkgateways/generatevpnclientpackage/action | Generate VpnClient package for virtualNetworkGateway |
> | Action | microsoft.network/virtualnetworkgateways/generatevpnprofile/action | Generate VpnProfile package for VirtualNetworkGateway |
> | Action | microsoft.network/virtualnetworkgateways/getadvertisedroutes/action | Gets virtualNetworkGateway advertised routes |
> | Action | microsoft.network/virtualnetworkgateways/getbgppeerstatus/action | Gets virtualNetworkGateway bgp peer status |
> | Action | microsoft.network/virtualnetworkgateways/getlearnedroutes/action | Gets virtualnetworkgateway learned routes |
> | Action | microsoft.network/virtualnetworkgateways/getvpnclientconnectionhealth/action | Get Per Vpn Client Connection Health for VirtualNetworkGateway |
> | Action | microsoft.network/virtualnetworkgateways/getvpnclientipsecparameters/action | Get Vpnclient Ipsec parameters for VirtualNetworkGateway P2S client. |
> | Action | microsoft.network/virtualnetworkgateways/getvpnprofilepackageurl/action | Gets the URL of a pre-generated vpn client profile package |
> | Action | Microsoft.Network/virtualNetworkGateways/providers/Microsoft.Insights/diagnosticSettings/read | Gets the Virtual Network Gateway Diagnostic Settings |
> | Action | Microsoft.Network/virtualNetworkGateways/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the Virtual Network Gateway diagnostic settings, this operation is supplemented by insights resource provider. |
> | Action | Microsoft.Network/virtualNetworkGateways/providers/Microsoft.Insights/logDefinitions/read | Gets the events for Virtual Network Gateway |
> | Action | Microsoft.Network/virtualNetworkGateways/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Virtual Network Gateway |
> | Action | Microsoft.Network/virtualNetworkGateways/read | Gets a VirtualNetworkGateway |
> | Action | microsoft.network/virtualnetworkgateways/reset/action | Resets a virtualNetworkGateway |
> | Action | microsoft.network/virtualnetworkgateways/resetvpnclientsharedkey/action | Reset Vpnclient shared key for VirtualNetworkGateway P2S client. |
> | Action | microsoft.network/virtualnetworkgateways/setvpnclientipsecparameters/action | Set Vpnclient Ipsec parameters for VirtualNetworkGateway P2S client. |
> | Action | Microsoft.Network/virtualnetworkgateways/supportedvpndevices/action | Lists Supported Vpn Devices |
> | Action | Microsoft.Network/virtualNetworkGateways/write | Creates or updates a VirtualNetworkGateway |
> | Action | Microsoft.Network/virtualNetworks/checkIpAddressAvailability/read | Check if Ip Address is available at the specified virtual network |
> | Action | Microsoft.Network/virtualNetworks/customViews/get/action | Get a Virtual Network custom view content |
> | Action | Microsoft.Network/virtualNetworks/customViews/read | Get definition of a custom view of Virtual Network |
> | Action | Microsoft.Network/virtualNetworks/delete | Deletes a virtual network |
> | Action | Microsoft.Network/virtualNetworks/peer/action | Peers a virtual network with another virtual network |
> | Action | Microsoft.Network/virtualNetworks/providers/Microsoft.Insights/diagnosticSettings/read | Get the diagnostic settings of Virtual Network |
> | Action | Microsoft.Network/virtualNetworks/providers/Microsoft.Insights/diagnosticSettings/write | Create or update the diagnostic settings of the Virtual Network |
> | Action | Microsoft.Network/virtualNetworks/providers/Microsoft.Insights/logDefinitions/read | Get the log definitions of Virtual Network |
> | Action | Microsoft.Network/virtualNetworks/providers/Microsoft.Insights/metricDefinitions/read | Gets available metrics for the PingMesh |
> | Action | Microsoft.Network/virtualNetworks/read | Get the virtual network definition |
> | Action | Microsoft.Network/virtualNetworks/remoteVirtualNetworkPeeringProxies/delete | Deletes a virtual network peering proxy |
> | Action | Microsoft.Network/virtualNetworks/remoteVirtualNetworkPeeringProxies/read | Gets a virtual network peering proxy definition |
> | Action | Microsoft.Network/virtualNetworks/remoteVirtualNetworkPeeringProxies/write | Creates a virtual network peering proxy or updates an existing virtual network peering proxy |
> | Action | Microsoft.Network/virtualNetworks/subnets/delete | Deletes a virtual network subnet |
> | Action | Microsoft.Network/virtualNetworks/subnets/join/action | Joins a virtual network |
> | Action | Microsoft.Network/virtualNetworks/subnets/joinViaServiceEndpoint/action | Joins resource such as storage account or SQL database to a subnet. |
> | Action | Microsoft.Network/virtualNetworks/subnets/read | Gets a virtual network subnet definition |
> | Action | Microsoft.Network/virtualNetworks/subnets/resourceNavigationLinks/delete | Deletes a Resource Navigation Link |
> | Action | Microsoft.Network/virtualNetworks/subnets/resourceNavigationLinks/read | Get the Resource Navigation Link definition |
> | Action | Microsoft.Network/virtualNetworks/subnets/resourceNavigationLinks/write | Creates a Resource Navigation Link or updates an existing Resource Navigation Link |
> | Action | Microsoft.Network/virtualNetworks/subnets/serviceAssociationLinks/delete | Deletes a Service Association Link |
> | Action | Microsoft.Network/virtualNetworks/subnets/serviceAssociationLinks/details/read | Gets a Service Association Link Detail Definition |
> | Action | Microsoft.Network/virtualNetworks/subnets/serviceAssociationLinks/read | Gets a Service Association Link definition |
> | Action | Microsoft.Network/virtualNetworks/subnets/serviceAssociationLinks/validate/action | Validates a Service Association Link |
> | Action | Microsoft.Network/virtualNetworks/subnets/serviceAssociationLinks/write | Creates a Service Association Link or updates an existing Service Association Link |
> | Action | Microsoft.Network/virtualNetworks/subnets/virtualMachines/read | Gets references to all the virtual machines in a virtual network subnet |
> | Action | Microsoft.Network/virtualNetworks/subnets/write | Creates a virtual network subnet or updates an existing virtual network subnet |
> | Action | Microsoft.Network/virtualNetworks/taggedTrafficConsumers/delete | Deletes a Tagged Traffic Consumer |
> | Action | Microsoft.Network/virtualNetworks/taggedTrafficConsumers/read | Get the Tagged Traffic Consumer definition |
> | Action | Microsoft.Network/virtualNetworks/taggedTrafficConsumers/validate/action | Validates a Tagged Traffic Consumer |
> | Action | Microsoft.Network/virtualNetworks/taggedTrafficConsumers/write | Creates a Tagged Traffic Consumer or updates an existing Tagged Traffic Consumer |
> | Action | Microsoft.Network/virtualNetworks/usages/read | Get the IP usages for each subnet of the virtual network |
> | Action | Microsoft.Network/virtualNetworks/virtualMachines/read | Gets references to all the virtual machines in a virtual network |
> | Action | Microsoft.Network/virtualNetworks/virtualNetworkPeerings/delete | Deletes a virtual network peering |
> | Action | Microsoft.Network/virtualNetworks/virtualNetworkPeerings/read | Gets a virtual network peering definition |
> | Action | Microsoft.Network/virtualNetworks/virtualNetworkPeerings/write | Creates a virtual network peering or updates an existing virtual network peering |
> | Action | Microsoft.Network/virtualNetworks/write | Creates a virtual network or updates an existing virtual network |
> | Action | Microsoft.Network/virtualNetworkTaps/delete | Delete Virtual Network Tap |
> | Action | Microsoft.Network/virtualNetworkTaps/join/action | Joins a virtual network tap |
> | Action | Microsoft.Network/virtualNetworkTaps/networkInterfaceTapConfigurationProxies/delete | Deletes a Network Interface Tap Configuration Proxy. |
> | Action | Microsoft.Network/virtualNetworkTaps/networkInterfaceTapConfigurationProxies/read | Gets a Network Interface Tap Configuration Proxy. |
> | Action | Microsoft.Network/virtualNetworkTaps/networkInterfaceTapConfigurationProxies/write | Creates a Network Interface Tap Configuration Proxy Or updates an existing Network Interface Tap Configuration Proxy. |
> | Action | Microsoft.Network/virtualNetworkTaps/read | Get Virtual Network Tap |
> | Action | Microsoft.Network/virtualNetworkTaps/write | Create or Update Virtual Network Tap |
> | Action | Microsoft.Network/virtualWans/delete | Deletes a Virtual Wan |
> | Action | Microsoft.Network/virtualWans/p2sVpnGatewayProxies/delete | Deletes a P2SVpnGateway Proxy |
> | Action | Microsoft.Network/virtualWans/p2sVpnGatewayProxies/read | Gets a P2SVpnGateway Proxy definition |
> | Action | Microsoft.Network/virtualWans/p2sVpnGatewayProxies/write | Creates a P2SVpnGateway Proxy or updates a P2SVpnGateway Proxy |
> | Action | Microsoft.Network/virtualWans/p2sVpnServerConfigurations/delete | Deletes a virtual Wan P2SVpnServerConfiguration |
> | Action | Microsoft.Network/virtualWans/p2sVpnServerConfigurations/read | Gets a virtual Wan P2SVpnServerConfiguration definition |
> | Action | Microsoft.Network/virtualWans/p2sVpnServerConfigurations/write | Creates a virtual Wan P2SVpnServerConfiguration or updates an existing virtual Wan P2SVpnServerConfiguration |
> | Action | Microsoft.Network/virtualWans/read | Get a Virtual Wan |
> | Action | Microsoft.Network/virtualwans/supportedSecurityProviders/read | Gets supported VirtualWan Security Providers. |
> | Action | Microsoft.Network/virtualWans/virtualHubProxies/delete | Deletes a Virtual Hub proxy |
> | Action | Microsoft.Network/virtualWans/virtualHubProxies/read | Gets a Virtual Hub proxy definition |
> | Action | Microsoft.Network/virtualWans/virtualHubProxies/write | Creates a Virtual Hub proxy or updates a Virtual Hub proxy |
> | Action | Microsoft.Network/virtualWans/virtualHubs/read | Gets all Virtual Hubs that reference a Virtual Wan. |
> | Action | Microsoft.Network/virtualwans/vpnconfiguration/action | Gets a Vpn Configuration |
> | Action | Microsoft.Network/virtualWans/vpnSiteProxies/delete | Deletes a Vpn Site proxy |
> | Action | Microsoft.Network/virtualWans/vpnSiteProxies/read | Gets a Vpn Site proxy definition |
> | Action | Microsoft.Network/virtualWans/vpnSiteProxies/write | Creates a Vpn Site proxy or updates a Vpn Site proxy |
> | Action | Microsoft.Network/virtualWans/vpnSites/read | Gets all VPN Sites that reference a Virtual Wan. |
> | Action | Microsoft.Network/virtualWans/write | Create or update a Virtual Wan |
> | Action | Microsoft.Network/vpnGateways/delete | Deletes a VpnGateway. |
> | Action | microsoft.network/vpngateways/listvpnconnectionshealth/action | Gets connection health for all or a subset of connections on a VpnGateway |
> | Action | Microsoft.Network/vpnGateways/read | Gets a VpnGateway. |
> | Action | microsoft.network/vpngateways/reset/action | Resets a VpnGateway |
> | Action | microsoft.network/vpnGateways/vpnConnections/delete | Deletes a VpnConnection. |
> | Action | microsoft.network/vpnGateways/vpnConnections/read | Gets a VpnConnection. |
> | Action | microsoft.network/vpnGateways/vpnConnections/write | Puts a VpnConnection. |
> | Action | Microsoft.Network/vpnGateways/write | Puts a VpnGateway. |
> | Action | Microsoft.Network/vpnsites/delete | Deletes a Vpn Site resource. |
> | Action | Microsoft.Network/vpnsites/read | Gets a Vpn Site resource. |
> | Action | Microsoft.Network/vpnsites/write | Creates or updates a Vpn Site resource. |

## Microsoft.NotificationHubs

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.NotificationHubs/CheckNamespaceAvailability/action | Checks whether or not a given Namespace resource name is available within the NotificationHub service. |
> | Action | Microsoft.NotificationHubs/Namespaces/authorizationRules/action | Get the list of Namespaces Authorization Rules description. |
> | Action | Microsoft.NotificationHubs/Namespaces/authorizationRules/delete | Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted.  |
> | Action | Microsoft.NotificationHubs/Namespaces/authorizationRules/listkeys/action | Get the Connection String to the Namespace |
> | Action | Microsoft.NotificationHubs/Namespaces/authorizationRules/read | Get the list of Namespaces Authorization Rules description. |
> | Action | Microsoft.NotificationHubs/Namespaces/authorizationRules/regenerateKeys/action | Namespace Authorization Rule Regenerate Primary/SecondaryKey, Specify the Key that needs to be regenerated |
> | Action | Microsoft.NotificationHubs/Namespaces/authorizationRules/write | Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated. |
> | Action | Microsoft.NotificationHubs/Namespaces/CheckNotificationHubAvailability/action | Checks whether or not a given NotificationHub name is available inside a Namespace. |
> | Action | Microsoft.NotificationHubs/Namespaces/Delete | Delete Namespace Resource |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/authorizationRules/action | Get the list of Notification Hub Authorization Rules |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/authorizationRules/delete | Delete Notification Hub Authorization Rules |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/authorizationRules/listkeys/action | Get the Connection String to the Notification Hub |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/authorizationRules/read | Get the list of Notification Hub Authorization Rules |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/authorizationRules/regenerateKeys/action | Notification Hub Authorization Rule Regenerate Primary/SecondaryKey, Specify the Key that needs to be regenerated |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/authorizationRules/write | Create Notification Hub Authorization Rules and Update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated. |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/debugSend/action | Send a test push notification. |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/Delete | Delete Notification Hub Resource |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/metricDefinitions/read | Get list of Namespace metrics Resource Descriptions |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/pnsCredentials/action | Get All Notification Hub PNS Credentials. This includes, WNS, MPNS, APNS, GCM and Baidu credentials |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/read | Get list of Notification Hub Resource Descriptions |
> | Action | Microsoft.NotificationHubs/Namespaces/NotificationHubs/write | Create a Notification Hub and Update its properties. Its properties mainly include PNS Credentials. Authorization Rules and TTL |
> | Action | Microsoft.NotificationHubs/Namespaces/read | Get the list of Namespace Resource Description |
> | Action | Microsoft.NotificationHubs/Namespaces/write | Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated. |
> | Action | Microsoft.NotificationHubs/operationResults/read | Returns operation results for Notification Hubs provider |
> | Action | Microsoft.NotificationHubs/operations/read | Returns a list of supported operations for Notification Hubs provider |
> | Action | Microsoft.NotificationHubs/register/action | Registers the subscription for the NotifciationHubs resource provider and enables the creation of Namespaces and NotificationHubs |
> | Action | Microsoft.NotificationHubs/unregister/action | Unregisters the subscription for the NotifciationHubs resource provider and enables the creation of Namespaces and NotificationHubs |

## Microsoft.OffAzure

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.OffAzure/HyperVSites/clusters/read | Gets the properties of a Hyper-V cluster |
> | Action | Microsoft.OffAzure/HyperVSites/clusters/read | Gets the properties of a Hyper-V cluster |
> | Action | Microsoft.OffAzure/HyperVSites/clusters/write | Creates or updates the Hyper-V cluster |
> | Action | Microsoft.OffAzure/HyperVSites/clusters/write | Creates or updates the Hyper-V cluster |
> | Action | Microsoft.OffAzure/HyperVSites/delete | Deletes the Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/delete | Deletes the Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/hosts/read | Gets the properties of a Hyper-V host |
> | Action | Microsoft.OffAzure/HyperVSites/hosts/read | Gets the properties of a Hyper-V host |
> | Action | Microsoft.OffAzure/HyperVSites/hosts/write | Creates or updates the Hyper-V host |
> | Action | Microsoft.OffAzure/HyperVSites/hosts/write | Creates or updates the Hyper-V host |
> | Action | Microsoft.OffAzure/HyperVSites/jobs/read | Gets the properties of a Hyper-V jobs |
> | Action | Microsoft.OffAzure/HyperVSites/jobs/read | Gets the properties of a Hyper-V jobs |
> | Action | Microsoft.OffAzure/HyperVSites/machines/read | Gets the properties of a Hyper-V machines |
> | Action | Microsoft.OffAzure/HyperVSites/machines/read | Gets the properties of a Hyper-V machines |
> | Action | Microsoft.OffAzure/HyperVSites/machines/stop/action | Stops the Hyper-V machines |
> | Action | Microsoft.OffAzure/HyperVSites/machines/stop/action | Stops the Hyper-V machines |
> | Action | Microsoft.OffAzure/HyperVSites/operationsstatus/read | Gets the properties of a Hyper-V operation status |
> | Action | Microsoft.OffAzure/HyperVSites/operationsstatus/read | Gets the properties of a Hyper-V operation status |
> | Action | Microsoft.OffAzure/HyperVSites/read | Gets the properties of a Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/read | Gets the properties of a Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/refresh/action | Refreshes the objects within a Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/refresh/action | Refreshes the objects within a Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/runasaccounts/read | Gets the properties of a Hyper-V run as accounts |
> | Action | Microsoft.OffAzure/HyperVSites/runasaccounts/read | Gets the properties of a Hyper-V run as accounts |
> | Action | Microsoft.OffAzure/HyperVSites/usage/read | Gets the usages of a Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/usage/read | Gets the usages of a Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/write | Creates or updates the Hyper-V site |
> | Action | Microsoft.OffAzure/HyperVSites/write | Creates or updates the Hyper-V site |
> | Action | Microsoft.OffAzure/Operations/read | Reads the exposed operations |
> | Action | Microsoft.OffAzure/VMwareSites/delete | Deletes the VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/delete | Deletes the VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/jobs/read | Gets the properties of a VMware jobs |
> | Action | Microsoft.OffAzure/VMwareSites/jobs/read | Gets the properties of a VMware jobs |
> | Action | Microsoft.OffAzure/VMwareSites/machines/read | Gets the properties of a VMware machines |
> | Action | Microsoft.OffAzure/VMwareSites/machines/read | Gets the properties of a VMware machines |
> | Action | Microsoft.OffAzure/VMwareSites/machines/stop/action | Stops the VMware machines |
> | Action | Microsoft.OffAzure/VMwareSites/machines/stop/action | Stops the VMware machines |
> | Action | Microsoft.OffAzure/VMwareSites/operationsstatus/read | Gets the properties of a VMware operation status |
> | Action | Microsoft.OffAzure/VMwareSites/operationsstatus/read | Gets the properties of a VMware operation status |
> | Action | Microsoft.OffAzure/VMwareSites/read | Gets the properties of a VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/read | Gets the properties of a VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/refresh/action | Refreshes the objects within a VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/refresh/action | Refreshes the objects within a VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/runasaccounts/read | Gets the properties of a VMware run as accounts |
> | Action | Microsoft.OffAzure/VMwareSites/runasaccounts/read | Gets the properties of a VMware run as accounts |
> | Action | Microsoft.OffAzure/VMwareSites/usage/read | Gets the usages of a VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/usage/read | Gets the usages of a VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/vcenters/read | Gets the properties of a VMware vCenter |
> | Action | Microsoft.OffAzure/VMwareSites/vcenters/read | Gets the properties of a VMware vCenter |
> | Action | Microsoft.OffAzure/VMwareSites/vcenters/write | Creates or updates the VMware vCenter |
> | Action | Microsoft.OffAzure/VMwareSites/vcenters/write | Creates or updates the VMware vCenter |
> | Action | Microsoft.OffAzure/VMwareSites/write | Creates or updates the VMware site |
> | Action | Microsoft.OffAzure/VMwareSites/write | Creates or updates the VMware site |

## Microsoft.OperationalInsights

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.OperationalInsights/linkTargets/read | Lists existing accounts that are not associated with an Azure subscription. To link this Azure subscription to a workspace, use a customer id returned by this operation in the customer id property of the Create Workspace operation. |
> | Action | microsoft.operationalinsights/operations/read | Lists all of the available OperationalInsights Rest API operations. |
> | Action | Microsoft.OperationalInsights/register/action | Register a subscription to a resource provider. |
> | Action | Microsoft.OperationalInsights/workspaces/analytics/query/action | Search using new engine. |
> | Action | Microsoft.OperationalInsights/workspaces/analytics/query/schema/read | Get search schema V2. |
> | Action | Microsoft.OperationalInsights/workspaces/api/query/action | Search using new engine. |
> | Action | Microsoft.OperationalInsights/workspaces/api/query/schema/read | Get search schema V2. |
> | Action | Microsoft.OperationalInsights/workspaces/configurationScopes/delete | Delete Configuration Scope |
> | Action | Microsoft.OperationalInsights/workspaces/configurationScopes/read | Get Configuration Scope |
> | Action | Microsoft.OperationalInsights/workspaces/configurationScopes/write | Set Configuration Scope |
> | Action | Microsoft.OperationalInsights/workspaces/datasources/delete | Delete datasources under a workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/datasources/read | Get datasources under a workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/datasources/write | Create/Update datasources under a workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/delete | Deletes a workspace. If the workspace was linked to an existing workspace at creation time then the workspace it was linked to is not deleted. |
> | Action | Microsoft.OperationalInsights/workspaces/gateways/delete | Removes a gateway configured for the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/generateregistrationcertificate/action | Generates Registration Certificate for the workspace. This Certificate is used to connect Microsoft System Center Operation Manager to the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/intelligencepacks/disable/action | Disables an intelligence pack for a given workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/intelligencepacks/enable/action | Enables an intelligence pack for a given workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/intelligencepacks/read | Lists all intelligence packs that are visible for a given worksapce and also lists whether the pack is enabled or disabled for that workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/linkedServices/delete | Delete linked services under given workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/linkedServices/read | Get linked services under given workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/linkedServices/write | Create/Update linked services under given workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/listKeys/action | Retrieves the list keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/listKeys/read | Retrieves the list keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/managementGroups/read | Gets the names and metadata for System Center Operations Manager management groups connected to this workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/metricDefinitions/read | Get Metric Definitions under workspace |
> | Action | Microsoft.OperationalInsights/workspaces/notificationSettings/delete | Delete the user's notification settings for the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/notificationSettings/read | Get the user's notification settings for the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/notificationSettings/write | Set the user's notification settings for the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/purge/action | Delete specified data from workspace |
> | Action | Microsoft.OperationalInsights/workspaces/query/ADAssessmentRecommendation/read | Read data from the ADAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ADReplicationResult/read | Read data from the ADReplicationResult table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ADSecurityAssessmentRecommendation/read | Read data from the ADSecurityAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Alert/read | Read data from the Alert table |
> | Action | Microsoft.OperationalInsights/workspaces/query/AlertHistory/read | Read data from the AlertHistory table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ApplicationInsights/read | Read data from the ApplicationInsights table |
> | Action | Microsoft.OperationalInsights/workspaces/query/AuditLogs/read | Read data from the AuditLogs table |
> | Action | Microsoft.OperationalInsights/workspaces/query/AzureActivity/read | Read data from the AzureActivity table |
> | Action | Microsoft.OperationalInsights/workspaces/query/AzureMetrics/read | Read data from the AzureMetrics table |
> | Action | Microsoft.OperationalInsights/workspaces/query/BoundPort/read | Read data from the BoundPort table |
> | Action | Microsoft.OperationalInsights/workspaces/query/CommonSecurityLog/read | Read data from the CommonSecurityLog table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ComputerGroup/read | Read data from the ComputerGroup table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ConfigurationChange/read | Read data from the ConfigurationChange table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ConfigurationData/read | Read data from the ConfigurationData table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ContainerImageInventory/read | Read data from the ContainerImageInventory table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ContainerInventory/read | Read data from the ContainerInventory table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ContainerLog/read | Read data from the ContainerLog table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ContainerServiceLog/read | Read data from the ContainerServiceLog table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceAppCrash/read | Read data from the DeviceAppCrash table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceAppLaunch/read | Read data from the DeviceAppLaunch table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceCalendar/read | Read data from the DeviceCalendar table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceCleanup/read | Read data from the DeviceCleanup table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceConnectSession/read | Read data from the DeviceConnectSession table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceEtw/read | Read data from the DeviceEtw table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceHardwareHealth/read | Read data from the DeviceHardwareHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceHealth/read | Read data from the DeviceHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceHeartbeat/read | Read data from the DeviceHeartbeat table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceSkypeHeartbeat/read | Read data from the DeviceSkypeHeartbeat table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceSkypeSignIn/read | Read data from the DeviceSkypeSignIn table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DeviceSleepState/read | Read data from the DeviceSleepState table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHAppFailure/read | Read data from the DHAppFailure table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHAppReliability/read | Read data from the DHAppReliability table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHDriverReliability/read | Read data from the DHDriverReliability table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHLogonFailures/read | Read data from the DHLogonFailures table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHLogonMetrics/read | Read data from the DHLogonMetrics table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHOSCrashData/read | Read data from the DHOSCrashData table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHOSReliability/read | Read data from the DHOSReliability table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DHWipAppLearning/read | Read data from the DHWipAppLearning table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DnsEvents/read | Read data from the DnsEvents table |
> | Action | Microsoft.OperationalInsights/workspaces/query/DnsInventory/read | Read data from the DnsInventory table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ETWEvent/read | Read data from the ETWEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Event/read | Read data from the Event table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ExchangeAssessmentRecommendation/read | Read data from the ExchangeAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ExchangeOnlineAssessmentRecommendation/read | Read data from the ExchangeOnlineAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Heartbeat/read | Read data from the Heartbeat table |
> | Action | Microsoft.OperationalInsights/workspaces/query/IISAssessmentRecommendation/read | Read data from the IISAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/InboundConnection/read | Read data from the InboundConnection table |
> | Action | Microsoft.OperationalInsights/workspaces/query/KubeEvents/read | Read data from the KubeEvents table |
> | Action | Microsoft.OperationalInsights/workspaces/query/KubeNodeInventory/read | Read data from the KubeNodeInventory table |
> | Action | Microsoft.OperationalInsights/workspaces/query/KubePodInventory/read | Read data from the KubePodInventory table |
> | Action | Microsoft.OperationalInsights/workspaces/query/KubeServices/read | Read data from the KubeServices table |
> | Action | Microsoft.OperationalInsights/workspaces/query/LinuxAuditLog/read | Read data from the LinuxAuditLog table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplication/read | Read data from the MAApplication table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplicationHealth/read | Read data from the MAApplicationHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplicationHealthAlternativeVersions/read | Read data from the MAApplicationHealthAlternativeVersions table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplicationHealthIssues/read | Read data from the MAApplicationHealthIssues table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplicationInstance/read | Read data from the MAApplicationInstance table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplicationInstanceReadiness/read | Read data from the MAApplicationInstanceReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAApplicationReadiness/read | Read data from the MAApplicationReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADeploymentPlan/read | Read data from the MADeploymentPlan table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADevice/read | Read data from the MADevice table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADevicePnPHealth/read | Read data from the MADevicePnPHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADevicePnPHealthAlternativeVersions/read | Read data from the MADevicePnPHealthAlternativeVersions table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADevicePnPHealthIssues/read | Read data from the MADevicePnPHealthIssues table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADeviceReadiness/read | Read data from the MADeviceReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADriverInstanceReadiness/read | Read data from the MADriverInstanceReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MADriverReadiness/read | Read data from the MADriverReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAddin/read | Read data from the MAOfficeAddin table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAddinHealth/read | Read data from the MAOfficeAddinHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAddinHealthIssues/read | Read data from the MAOfficeAddinHealthIssues table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAddinInstance/read | Read data from the MAOfficeAddinInstance table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAddinInstanceReadiness/read | Read data from the MAOfficeAddinInstanceReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAddinReadiness/read | Read data from the MAOfficeAddinReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeApp/read | Read data from the MAOfficeApp table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAppHealth/read | Read data from the MAOfficeAppHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAppInstance/read | Read data from the MAOfficeAppInstance table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeAppReadiness/read | Read data from the MAOfficeAppReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeBuildInfo/read | Read data from the MAOfficeBuildInfo table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeCurrencyAssessment/read | Read data from the MAOfficeCurrencyAssessment table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeCurrencyAssessmentDailyCounts/read | Read data from the MAOfficeCurrencyAssessmentDailyCounts table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeDeploymentStatus/read | Read data from the MAOfficeDeploymentStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeMacroHealth/read | Read data from the MAOfficeMacroHealth table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeMacroHealthIssues/read | Read data from the MAOfficeMacroHealthIssues table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeMacroIssueInstanceReadiness/read | Read data from the MAOfficeMacroIssueInstanceReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeMacroIssueReadiness/read | Read data from the MAOfficeMacroIssueReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeMacroSummary/read | Read data from the MAOfficeMacroSummary table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeSuite/read | Read data from the MAOfficeSuite table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAOfficeSuiteInstance/read | Read data from the MAOfficeSuiteInstance table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAProposedPilotDevices/read | Read data from the MAProposedPilotDevices table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAWindowsBuildInfo/read | Read data from the MAWindowsBuildInfo table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAWindowsCurrencyAssessment/read | Read data from the MAWindowsCurrencyAssessment table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAWindowsCurrencyAssessmentDailyCounts/read | Read data from the MAWindowsCurrencyAssessmentDailyCounts table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAWindowsDeploymentStatus/read | Read data from the MAWindowsDeploymentStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/MAWindowsSysReqInstanceReadiness/read | Read data from the MAWindowsSysReqInstanceReadiness table |
> | Action | Microsoft.OperationalInsights/workspaces/query/NetworkMonitoring/read | Read data from the NetworkMonitoring table |
> | Action | Microsoft.OperationalInsights/workspaces/query/OfficeActivity/read | Read data from the OfficeActivity table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Operation/read | Read data from the Operation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/OutboundConnection/read | Read data from the OutboundConnection table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Perf/read | Read data from the Perf table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ProtectionStatus/read | Read data from the ProtectionStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/read | Run queries over the data in the workspace |
> | Action | Microsoft.OperationalInsights/workspaces/query/ReservedAzureCommonFields/read | Read data from the ReservedAzureCommonFields table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ReservedCommonFields/read | Read data from the ReservedCommonFields table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SCCMAssessmentRecommendation/read | Read data from the SCCMAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SCOMAssessmentRecommendation/read | Read data from the SCOMAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SecurityAlert/read | Read data from the SecurityAlert table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SecurityBaseline/read | Read data from the SecurityBaseline table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SecurityBaselineSummary/read | Read data from the SecurityBaselineSummary table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SecurityDetection/read | Read data from the SecurityDetection table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SecurityEvent/read | Read data from the SecurityEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ServiceFabricOperationalEvent/read | Read data from the ServiceFabricOperationalEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ServiceFabricReliableActorEvent/read | Read data from the ServiceFabricReliableActorEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/ServiceFabricReliableServiceEvent/read | Read data from the ServiceFabricReliableServiceEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SfBAssessmentRecommendation/read | Read data from the SfBAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SfBOnlineAssessmentRecommendation/read | Read data from the SfBOnlineAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SharePointOnlineAssessmentRecommendation/read | Read data from the SharePointOnlineAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SigninLogs/read | Read data from the SigninLogs table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SPAssessmentRecommendation/read | Read data from the SPAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SQLAssessmentRecommendation/read | Read data from the SQLAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SQLQueryPerformance/read | Read data from the SQLQueryPerformance table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Syslog/read | Read data from the Syslog table |
> | Action | Microsoft.OperationalInsights/workspaces/query/SysmonEvent/read | Read data from the SysmonEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Tables.Custom/read | Reading data from any custom log |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAApp/read | Read data from the UAApp table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAComputer/read | Read data from the UAComputer table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAComputerRank/read | Read data from the UAComputerRank table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UADriver/read | Read data from the UADriver table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UADriverProblemCodes/read | Read data from the UADriverProblemCodes table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAFeedback/read | Read data from the UAFeedback table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAHardwareSecurity/read | Read data from the UAHardwareSecurity table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAIESiteDiscovery/read | Read data from the UAIESiteDiscovery table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAOfficeAddIn/read | Read data from the UAOfficeAddIn table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAProposedActionPlan/read | Read data from the UAProposedActionPlan table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UASysReqIssue/read | Read data from the UASysReqIssue table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UAUpgradedComputer/read | Read data from the UAUpgradedComputer table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Update/read | Read data from the Update table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UpdateRunProgress/read | Read data from the UpdateRunProgress table |
> | Action | Microsoft.OperationalInsights/workspaces/query/UpdateSummary/read | Read data from the UpdateSummary table |
> | Action | Microsoft.OperationalInsights/workspaces/query/Usage/read | Read data from the Usage table |
> | Action | Microsoft.OperationalInsights/workspaces/query/VMBoundPort/read | Read data from the VMBoundPort table |
> | Action | Microsoft.OperationalInsights/workspaces/query/VMConnection/read | Read data from the VMConnection table |
> | Action | Microsoft.OperationalInsights/workspaces/query/W3CIISLog/read | Read data from the W3CIISLog table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WaaSDeploymentStatus/read | Read data from the WaaSDeploymentStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WaaSInsiderStatus/read | Read data from the WaaSInsiderStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WaaSUpdateStatus/read | Read data from the WaaSUpdateStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WDAVStatus/read | Read data from the WDAVStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WDAVThreat/read | Read data from the WDAVThreat table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WindowsClientAssessmentRecommendation/read | Read data from the WindowsClientAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WindowsEvent/read | Read data from the WindowsEvent table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WindowsFirewall/read | Read data from the WindowsFirewall table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WindowsServerAssessmentRecommendation/read | Read data from the WindowsServerAssessmentRecommendation table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WireData/read | Read data from the WireData table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WorkloadMonitoringPerf/read | Read data from the WorkloadMonitoringPerf table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WUDOAggregatedStatus/read | Read data from the WUDOAggregatedStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/query/WUDOStatus/read | Read data from the WUDOStatus table |
> | Action | Microsoft.OperationalInsights/workspaces/read | Gets an existing workspace |
> | Action | Microsoft.OperationalInsights/workspaces/regeneratesharedkey/action | Regenerates the specified workspace shared key |
> | Action | Microsoft.OperationalInsights/workspaces/savedSearches/delete | Deletes a saved search query |
> | Action | Microsoft.OperationalInsights/workspaces/savedSearches/read | Gets a saved search query |
> | Action | microsoft.operationalinsights/workspaces/savedsearches/results/read | Get saved searches results. Deprecated |
> | Action | Microsoft.OperationalInsights/workspaces/savedSearches/write | Creates a saved search query |
> | Action | Microsoft.OperationalInsights/workspaces/schema/read | Gets the search schema for the workspace.  Search schema includes the exposed fields and their types. |
> | Action | Microsoft.OperationalInsights/workspaces/search/action | Executes a search query |
> | Action | microsoft.operationalinsights/workspaces/search/read | Get search results. Deprecated. |
> | Action | Microsoft.OperationalInsights/workspaces/sharedKeys/action | Retrieves the shared keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/sharedKeys/read | Retrieves the shared keys for the workspace. These keys are used to connect Microsoft Operational Insights agents to the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/storageinsightconfigs/delete | Deletes a storage configuration. This will stop Microsoft Operational Insights from reading data from the storage account. |
> | Action | Microsoft.OperationalInsights/workspaces/storageinsightconfigs/read | Gets a storage configuration. |
> | Action | Microsoft.OperationalInsights/workspaces/storageinsightconfigs/write | Creates a new storage configuration. These configurations are used to pull data from a location in an existing storage account. |
> | Action | Microsoft.OperationalInsights/workspaces/upgradetranslationfailures/read | Get Search Upgrade Translation Failure log for the workspace |
> | Action | Microsoft.OperationalInsights/workspaces/usages/read | Gets usage data for a workspace including the amount of data read by the workspace. |
> | Action | Microsoft.OperationalInsights/workspaces/write | Creates a new workspace or links to an existing workspace by providing the customer id from the existing workspace. |

## Microsoft.OperationsManagement

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.OperationsManagement/managementAssociations/delete | Delete existing Management Association |
> | Action | Microsoft.OperationsManagement/managementAssociations/read | Get Existing Management Association |
> | Action | Microsoft.OperationsManagement/managementAssociations/write | Create a new Management Association |
> | Action | Microsoft.OperationsManagement/managementConfigurations/delete | Delete existing Management Configuratin |
> | Action | Microsoft.OperationsManagement/managementConfigurations/read | Get Existing Management Configuration |
> | Action | Microsoft.OperationsManagement/managementConfigurations/write | Create a new Management Configuration |
> | Action | Microsoft.OperationsManagement/register/action | Register a subscription to a resource provider. |
> | Action | Microsoft.OperationsManagement/solutions/delete | Delete existing OMS solution |
> | Action | Microsoft.OperationsManagement/solutions/read | Get exiting OMS solution |
> | Action | Microsoft.OperationsManagement/solutions/write | Create new OMS solution |

## Microsoft.PolicyInsights

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.PolicyInsights/asyncOperationResults/read | Gets the async operation result. |
> | Action | Microsoft.PolicyInsights/policyEvents/queryResults/action | Query information about policy events. |
> | Action | Microsoft.PolicyInsights/policyEvents/queryResults/read | Query information about policy events. |
> | Action | Microsoft.PolicyInsights/policyStates/queryResults/action | Query information about policy states. |
> | Action | Microsoft.PolicyInsights/policyStates/queryResults/read | Query information about policy states. |
> | Action | Microsoft.PolicyInsights/policyStates/summarize/action | Query summary information about policy latest states. |
> | Action | Microsoft.PolicyInsights/policyStates/summarize/read | Query summary information about policy latest states. |
> | Action | Microsoft.PolicyInsights/policyStates/triggerEvaluation/action | Triggers a new compliance evaluation for the selected scope. |
> | Action | Microsoft.PolicyInsights/policyTrackedResources/queryResults/read | Query information about resources required by DeployIfNotExists policies. |
> | Action | Microsoft.PolicyInsights/register/action | Registers the policy insights resource provider and enables actions on it. |
> | Action | Microsoft.PolicyInsights/remediations/cancel/action | Cancel in-progress policy remediations. |
> | Action | Microsoft.PolicyInsights/remediations/delete | Delete policy remediations. |
> | Action | Microsoft.PolicyInsights/remediations/listDeployments/read | Lists the deployments required by a policy remediation. |
> | Action | Microsoft.PolicyInsights/remediations/read | Get policy remediations. |
> | Action | Microsoft.PolicyInsights/remediations/write | Create or update policy remediations. |

## Microsoft.Portal

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Portal/dashboards/delete | Removes the dashboard from the subscription. |
> | Action | Microsoft.Portal/dashboards/read | Reads the dashboards for the subscription. |
> | Action | Microsoft.Portal/dashboards/write | Add or modify dashboard to a subscription. |

## Microsoft.PowerBIDedicated

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.PowerBIDedicated/capacities/checkNameAvailability/action | Checks that given Power BI Dedicated Capacity name is valid and not in use. |
> | Action | Microsoft.PowerBIDedicated/capacities/delete | Deletes the Power BI Dedicated Capacity. |
> | Action | Microsoft.PowerBIDedicated/capacities/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.PowerBIDedicated/capacities/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.PowerBIDedicated/capacities/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Power BI Dedicated Capacities |
> | Action | Microsoft.PowerBIDedicated/capacities/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Power BI Dedicated Capacity. |
> | Action | Microsoft.PowerBIDedicated/capacities/read | Retrieves the information of the specified Power BI Dedicated Capacity. |
> | Action | Microsoft.PowerBIDedicated/capacities/resume/action | Resumes the Capacity. |
> | Action | Microsoft.PowerBIDedicated/capacities/skus/read | Retrieve available SKU information for the capacity |
> | Action | Microsoft.PowerBIDedicated/capacities/suspend/action | Suspends the Capacity. |
> | Action | Microsoft.PowerBIDedicated/capacities/write | Creates or updates the specified Power BI Dedicated Capacity. |
> | Action | Microsoft.PowerBIDedicated/locations/operationresults/read | Retrieves the information of the specified operation result. |
> | Action | Microsoft.PowerBIDedicated/locations/operationstatuses/read | Retrieves the information of the specified operation status. |
> | Action | Microsoft.PowerBIDedicated/operations/read | Retrieves the information of operations |
> | Action | Microsoft.PowerBIDedicated/register/action | Registers Power BI Dedicated resource provider. |
> | Action | Microsoft.PowerBIDedicated/skus/read | Retrieves the information of Skus |

## Microsoft.RecoveryServices

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.RecoveryServices/locations/allocatedStamp/read | GetAllocatedStamp is internal operation used by service |
> | Action | Microsoft.RecoveryServices/locations/allocateStamp/action | AllocateStamp is internal operation used by service |
> | Action | Microsoft.RecoveryServices/locations/backupPreValidateProtection/action |  |
> | Action | Microsoft.RecoveryServices/locations/backupStatus/action | Check Backup Status for Recovery Services Vaults |
> | Action | Microsoft.RecoveryServices/locations/backupValidateFeatures/action | Validate Features |
> | Action | Microsoft.RecoveryServices/locations/operationStatus/read | Gets Operation Status for a given Operation |
> | Action | Microsoft.RecoveryServices/operations/read | Operation returns the list of Operations for a Resource Provider |
> | Action | Microsoft.RecoveryServices/register/action | Registers subscription for given Resource Provider |
> | Action | Microsoft.RecoveryServices/Vaults/backupconfig/read | Returns Configuration for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupconfig/write | Updates Configuration for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupEngines/read | Returns all the backup management servers registered with vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/backupProtectionIntent/delete | Delete a backup Protection Intent |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/backupProtectionIntent/read | Get a backup Protection Intent |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/backupProtectionIntent/write | Create a backup Protection Intent |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/operationResults/read | Returns status of the operation |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectableContainers/read | Get all protectable containers |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/delete | Deletes the registered Container |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/inquire/action | Do inquiry for workloads within a container |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/items/read | Get all items in a container |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/operationResults/read | Gets result of Operation performed on Protection Container. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/backup/action | Performs Backup for Protected Item. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/delete | Deletes Protected Item |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/operationResults/read | Gets Result of Operation Performed on Protected Items. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/operationsStatus/read | Returns the status of Operation performed on Protected Items. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/read | Returns object details of the Protected Item |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/recoveryPoints/provisionInstantItemRecovery/action | Provision Instant Item Recovery for Protected Item |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/recoveryPoints/read | Get Recovery Points for Protected Items. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/recoveryPoints/restore/action | Restore Recovery Points for Protected Items. |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/recoveryPoints/revokeInstantItemRecovery/action | Revoke Instant Item Recovery for Protected Item |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/protectedItems/write | Create a backup Protected Item |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/read | Returns all registered containers |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/protectionContainers/write | Creates a registered container |
> | Action | Microsoft.RecoveryServices/Vaults/backupFabrics/refreshContainers/action | Refreshes the container list |
> | Action | Microsoft.RecoveryServices/Vaults/backupJobs/cancel/action | Cancel the Job |
> | Action | Microsoft.RecoveryServices/Vaults/backupJobs/operationResults/read | Returns the Result of Job Operation. |
> | Action | Microsoft.RecoveryServices/Vaults/backupJobs/read | Returns all Job Objects |
> | Action | Microsoft.RecoveryServices/Vaults/backupJobsExport/action | Export Jobs |
> | Action | Microsoft.RecoveryServices/Vaults/backupJobsExport/operationResults/read | Returns the Result of Export Job Operation. |
> | Action | Microsoft.RecoveryServices/Vaults/backupManagementMetaData/read | Returns Backup Management Metadata for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupOperationResults/read | Returns Backup Operation Result for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupOperations/read | Returns Backup Operation Status for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupPolicies/delete | Delete a Protection Policy |
> | Action | Microsoft.RecoveryServices/Vaults/backupPolicies/operationResults/read | Get Results of Policy Operation. |
> | Action | Microsoft.RecoveryServices/Vaults/backupPolicies/operations/read | Get Status of Policy Operation. |
> | Action | Microsoft.RecoveryServices/Vaults/backupPolicies/read | Returns all Protection Policies |
> | Action | Microsoft.RecoveryServices/Vaults/backupPolicies/write | Creates Protection Policy |
> | Action | Microsoft.RecoveryServices/Vaults/backupProtectableItems/read | Returns list of all Protectable Items. |
> | Action | Microsoft.RecoveryServices/Vaults/backupProtectedItems/read | Returns the list of all Protected Items. |
> | Action | Microsoft.RecoveryServices/Vaults/backupProtectionContainers/read | Returns all containers belonging to the subscription |
> | Action | Microsoft.RecoveryServices/Vaults/backupProtectionIntents/read | List all backup Protection Intents |
> | Action | Microsoft.RecoveryServices/Vaults/backupSecurityPIN/action | Returns Security PIN Information for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupstorageconfig/read | Returns Storage Configuration for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupstorageconfig/write | Updates Storage Configuration for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/backupUsageSummaries/read | Returns summaries for Protected Items and Protected Servers for a Recovery Services . |
> | Action | Microsoft.RecoveryServices/Vaults/backupValidateOperation/action | Validate Operation on Protected Item |
> | Action | Microsoft.RecoveryServices/Vaults/certificates/write | The Update Resource Certificate operation updates the resource/vault credential certificate. |
> | Action | Microsoft.RecoveryServices/Vaults/delete | The Delete Vault operation deletes the specified Azure resource of type 'vault' |
> | Action | Microsoft.RecoveryServices/Vaults/extendedInformation/delete | The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault? |
> | Action | Microsoft.RecoveryServices/Vaults/extendedInformation/read | The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault? |
> | Action | Microsoft.RecoveryServices/Vaults/extendedInformation/write | The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault? |
> | Action | Microsoft.RecoveryServices/Vaults/monitoringAlerts/read | Gets the alerts for the Recovery services vault. |
> | Action | Microsoft.RecoveryServices/Vaults/monitoringAlerts/write | Resolves the alert. |
> | Action | Microsoft.RecoveryServices/Vaults/monitoringConfigurations/read | Gets the Recovery services vault notification configuration. |
> | Action | Microsoft.RecoveryServices/Vaults/monitoringConfigurations/write | Configures e-mail notifications to Recovery services vault. |
> | Action | Microsoft.RecoveryServices/Vaults/providers/Microsoft.Insights/diagnosticSettings/read | Azure Backup Diagnostics |
> | Action | Microsoft.RecoveryServices/Vaults/providers/Microsoft.Insights/diagnosticSettings/write | Azure Backup Diagnostics |
> | Action | Microsoft.RecoveryServices/Vaults/providers/Microsoft.Insights/logDefinitions/read | Azure Backup Logs |
> | Action | Microsoft.RecoveryServices/Vaults/providers/Microsoft.Insights/metricDefinitions/read | Azure Backup Metrics |
> | Action | Microsoft.RecoveryServices/Vaults/read | The Get Vault operation gets an object representing the Azure resource of type 'vault' |
> | Action | Microsoft.RecoveryServices/Vaults/registeredIdentities/delete | The UnRegister Container operation can be used to unregister a container. |
> | Action | Microsoft.RecoveryServices/Vaults/registeredIdentities/operationResults/read | The Get Operation Results operation can be used get the operation status and result for the asynchronously submitted operation |
> | Action | Microsoft.RecoveryServices/Vaults/registeredIdentities/read | The Get Containers operation can be used get the containers registered for a resource. |
> | Action | Microsoft.RecoveryServices/Vaults/registeredIdentities/write | The Register Service Container operation can be used to register a container with Recovery Service. |
> | Action | Microsoft.RecoveryServices/vaults/replicationAlertSettings/read | Read any Alerts Settings |
> | Action | Microsoft.RecoveryServices/vaults/replicationAlertSettings/write | Create or Update any Alerts Settings |
> | Action | Microsoft.RecoveryServices/vaults/replicationEvents/read | Read any Events |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/checkConsistency/action | Checks Consistency of the Fabric |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/delete | Delete any Fabrics |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/deployProcessServerImage/action | Deploy Process Server Image |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/migratetoaad/action | Migrate Fabric To AAD |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/read | Read any Fabrics |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/reassociateGateway/action | Reassociate Gateway |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/remove/action | Remove Fabric |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/renewcertificate/action | Renew Certificate for Fabric |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationLogicalNetworks/read | Read any Logical Networks |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationNetworks/read | Read any Networks |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationNetworks/replicationNetworkMappings/delete | Delete any Network Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationNetworks/replicationNetworkMappings/read | Read any Network Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationNetworks/replicationNetworkMappings/write | Create or Update any Network Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/discoverProtectableItem/action | Discover Protectable Item |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/read | Read any Protection Containers |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/remove/action | Remove Protection Container |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectableItems/read | Read any Protectable Items |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/applyRecoveryPoint/action | Apply Recovery Point |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/delete | Delete any Protected Items |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/failoverCommit/action | Failover Commit |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/plannedFailover/action | Planned Failover |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/read | Read any Protected Items |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/recoveryPoints/read | Read any Replication Recovery Points |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/remove/action | Remove Protected Item |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/repairReplication/action | Repair replication |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/reProtect/action | ReProtect Protected Item |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/submitFeedback/action | Submit Feedback |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/targetComputeSizes/read | Read any Target Compute Sizes |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/testFailover/action | Test Failover |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/testFailoverCleanup/action | Test Failover Cleanup |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/unplannedFailover/action | Failover |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/updateMobilityService/action | Update Mobility Service |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectedItems/write | Create or Update any Protected Items |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings/delete | Delete any Protection Container Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings/read | Read any Protection Container Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings/remove/action | Remove Protection Container Mapping |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings/write | Create or Update any Protection Container Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/switchprotection/action | Switch Protection Container |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/write | Create or Update any Protection Containers |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders/delete | Delete any Recovery Services Providers |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders/read | Read any Recovery Services Providers |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders/refreshProvider/action | Refresh Provider |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders/remove/action | Remove Recovery Services Provider |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders/write | Create or Update any Recovery Services Providers |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationStorageClassifications/read | Read any Storage Classifications |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationStorageClassifications/replicationStorageClassificationMappings/delete | Delete any Storage Classification Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationStorageClassifications/replicationStorageClassificationMappings/read | Read any Storage Classification Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationStorageClassifications/replicationStorageClassificationMappings/write | Create or Update any Storage Classification Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationvCenters/delete | Delete any vCenters |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationvCenters/read | Read any vCenters |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/replicationvCenters/write | Create or Update any vCenters |
> | Action | Microsoft.RecoveryServices/vaults/replicationFabrics/write | Create or Update any Fabrics |
> | Action | Microsoft.RecoveryServices/vaults/replicationJobs/cancel/action | Cancel Job |
> | Action | Microsoft.RecoveryServices/vaults/replicationJobs/read | Read any Jobs |
> | Action | Microsoft.RecoveryServices/vaults/replicationJobs/restart/action | Restart job |
> | Action | Microsoft.RecoveryServices/vaults/replicationJobs/resume/action | Resume Job |
> | Action | Microsoft.RecoveryServices/vaults/replicationNetworkMappings/read | Read any Network Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationNetworks/read | Read any Networks |
> | Action | Microsoft.RecoveryServices/vaults/replicationPolicies/delete | Delete any Policies |
> | Action | Microsoft.RecoveryServices/vaults/replicationPolicies/read | Read any Policies |
> | Action | Microsoft.RecoveryServices/vaults/replicationPolicies/write | Create or Update any Policies |
> | Action | Microsoft.RecoveryServices/vaults/replicationProtectedItems/read | Read any Protected Items |
> | Action | Microsoft.RecoveryServices/vaults/replicationProtectionContainerMappings/read | Read any Protection Container Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationProtectionContainers/read | Read any Protection Containers |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/delete | Delete any Recovery Plans |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/failoverCommit/action | Failover Commit Recovery Plan |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/plannedFailover/action | Planned Failover Recovery Plan |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/read | Read any Recovery Plans |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/reProtect/action | ReProtect Recovery Plan |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/testFailover/action | Test Failover Recovery Plan |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/testFailoverCleanup/action | Test Failover Cleanup Recovery Plan |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/unplannedFailover/action | Failover Recovery Plan |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryPlans/write | Create or Update any Recovery Plans |
> | Action | Microsoft.RecoveryServices/vaults/replicationRecoveryServicesProviders/read | Read any Recovery Services Providers |
> | Action | Microsoft.RecoveryServices/vaults/replicationStorageClassificationMappings/read | Read any Storage Classification Mappings |
> | Action | Microsoft.RecoveryServices/vaults/replicationStorageClassifications/read | Read any Storage Classifications |
> | Action | Microsoft.RecoveryServices/vaults/replicationUsages/read | Read any Vault Replication Usages |
> | Action | Microsoft.RecoveryServices/vaults/replicationVaultHealth/read | Read any Vault Replication Health |
> | Action | Microsoft.RecoveryServices/vaults/replicationVaultHealth/refresh/action | Refresh Vault Health |
> | Action | Microsoft.RecoveryServices/vaults/replicationvCenters/read | Read any vCenters |
> | Action | Microsoft.RecoveryServices/Vaults/tokenInfo/read | Returns token information for Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/vaults/usages/read | Read any Vault Usages |
> | Action | Microsoft.RecoveryServices/Vaults/usages/read | Returns usage details for a Recovery Services Vault. |
> | Action | Microsoft.RecoveryServices/Vaults/vaultTokens/read | The Vault Token operation can be used to get Vault Token for vault level backend operations. |
> | Action | Microsoft.RecoveryServices/Vaults/write | Create Vault operation creates an Azure resource of type 'vault' |

## Microsoft.Relay

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Relay/checkNameAvailability/action | Checks availability of namespace under given subscription. |
> | Action | Microsoft.Relay/checkNamespaceAvailability/action | Checks availability of namespace under given subscription. This API is deprecated please use CheckNameAvailabiltiy instead. |
> | Action | Microsoft.Relay/namespaces/authorizationRules/action | Updates Namespace Authorization Rule. This API is depricated. Please use a PUT call to update the Namespace Authorization Rule instead.. This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.Relay/namespaces/authorizationRules/delete | Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted.  |
> | Action | Microsoft.Relay/namespaces/authorizationRules/listkeys/action | Get the Connection String to the Namespace |
> | Action | Microsoft.Relay/namespaces/authorizationRules/read | Get the list of Namespaces Authorization Rules description. |
> | Action | Microsoft.Relay/namespaces/authorizationRules/regenerateKeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.Relay/namespaces/authorizationRules/write | Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated. |
> | Action | Microsoft.Relay/namespaces/Delete | Delete Namespace Resource |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/authorizationRules/listkeys/action | Gets the authorization rules keys for the Disaster Recovery primary namespace |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/authorizationRules/read | Get Disaster Recovery Primary Namespace's Authorization Rules |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/breakPairing/action | Disables Disaster Recovery and stops replicating changes from primary to secondary namespaces. |
> | Action | Microsoft.Relay/namespaces/disasterrecoveryconfigs/checkNameAvailability/action | Checks availability of namespace alias under given subscription. |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/delete | Deletes the Disaster Recovery configuration associated with the namespace. This operation can only be invoked via the primary namespace. |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/failover/action | Invokes a GEO DR failover and reconfigures the namespace alias to point to the secondary namespace. |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/read | Gets the Disaster Recovery configuration associated with the namespace. |
> | Action | Microsoft.Relay/namespaces/disasterRecoveryConfigs/write | Creates or Updates the Disaster Recovery configuration associated with the namespace. |
> | Action | Microsoft.Relay/namespaces/HybridConnections/authorizationRules/action | Operation to update HybridConnection. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule. |
> | Action | Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete | Operation to delete HybridConnection Authorization Rules |
> | Action | Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action | Get the Connection String to HybridConnection |
> | Action | Microsoft.Relay/namespaces/HybridConnections/authorizationRules/read |  Get the list of HybridConnection Authorization Rules |
> | Action | Microsoft.Relay/namespaces/HybridConnections/authorizationRules/regeneratekeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write | Create HybridConnection Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated. |
> | Action | Microsoft.Relay/namespaces/HybridConnections/Delete | Operation to delete HybridConnection Resource |
> | Action | Microsoft.Relay/namespaces/HybridConnections/read | Get list of HybridConnection Resource Descriptions |
> | Action | Microsoft.Relay/namespaces/HybridConnections/write | Create or Update HybridConnection properties. |
> | Action | Microsoft.Relay/namespaces/messagingPlan/read | Gets the Messaging Plan for a namespace.<br>This API is deprecated.<br>Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions..<br>This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.Relay/namespaces/messagingPlan/write | Updates the Messaging Plan for a namespace.<br>This API is deprecated.<br>Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions..<br>This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.Relay/namespaces/operationresults/read | Get the status of Namespace operation |
> | Action | Microsoft.Relay/namespaces/providers/Microsoft.Insights/metricDefinitions/read | Get list of Namespace metrics Resource Descriptions |
> | Action | Microsoft.Relay/namespaces/read | Get the list of Namespace Resource Description |
> | Action | Microsoft.Relay/namespaces/removeAcsNamepsace/action | Remove ACS namespace |
> | Action | Microsoft.Relay/namespaces/WcfRelays/authorizationRules/action | Operation to update WcfRelay. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule. |
> | Action | Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete | Operation to delete WcfRelay Authorization Rules |
> | Action | Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action | Get the Connection String to WcfRelay |
> | Action | Microsoft.Relay/namespaces/WcfRelays/authorizationRules/read |  Get the list of WcfRelay Authorization Rules |
> | Action | Microsoft.Relay/namespaces/WcfRelays/authorizationRules/regeneratekeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write | Create WcfRelay Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated. |
> | Action | Microsoft.Relay/namespaces/WcfRelays/Delete | Operation to delete WcfRelay Resource |
> | Action | Microsoft.Relay/namespaces/WcfRelays/read | Get list of WcfRelay Resource Descriptions |
> | Action | Microsoft.Relay/namespaces/WcfRelays/write | Create or Update WcfRelay properties. |
> | Action | Microsoft.Relay/namespaces/write | Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated. |
> | Action | Microsoft.Relay/operations/read | Get Operations |
> | Action | Microsoft.Relay/register/action | Registers the subscription for the Relay resource provider and enables the creation of Relay resources |
> | Action | Microsoft.Relay/unregister/action | Registers the subscription for the Relay resource provider and enables the creation of Relay resources |

## Microsoft.ResourceHealth

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ResourceHealth/AvailabilityStatuses/current/read | Gets the availability status for the specified resource |
> | Action | Microsoft.ResourceHealth/AvailabilityStatuses/read | Gets the availability statuses for all resources in the specified scope |
> | Action | Microsoft.ResourceHealth/events/read | Get Service Health Events for given subscription |
> | Action | Microsoft.Resourcehealth/healthevent/action | Denotes the change in health state for the specified resource |
> | Action | Microsoft.Resourcehealth/healthevent/Activated/action | Denotes the change in health state for the specified resource |
> | Action | Microsoft.Resourcehealth/healthevent/InProgress/action | Denotes the change in health state for the specified resource |
> | Action | Microsoft.Resourcehealth/healthevent/Pending/action | Denotes the change in health state for the specified resource |
> | Action | Microsoft.Resourcehealth/healthevent/Resolved/action | Denotes the change in health state for the specified resource |
> | Action | Microsoft.Resourcehealth/healthevent/Updated/action | Denotes the change in health state for the specified resource |
> | Action | Microsoft.ResourceHealth/impactedResources/read | Get Impacted Resources for given subscription |
> | Action | Microsoft.ResourceHealth/Operations/read | Get the operations available for the Microsoft ResourceHealth |
> | Action | Microsoft.ResourceHealth/register/action | Registers the subscription for the Microsoft ResourceHealth |
> | Action | Microsoft.ResourceHealth/unregister/action | Unregisters the subscription for the Microsoft ResourceHealth |

## Microsoft.Resources

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Resources/checkPolicyCompliance/action | Check the compliance status of a given resource against resource policies. |
> | Action | Microsoft.Resources/checkResourceName/action | Check the resource name for validity. |
> | Action | Microsoft.Resources/deployments/cancel/action | Cancels a deployment. |
> | Action | Microsoft.Resources/deployments/delete | Deletes a deployment. |
> | Action | Microsoft.Resources/deployments/operations/read | Gets or lists deployment operations. |
> | Action | Microsoft.Resources/deployments/read | Gets or lists deployments. |
> | Action | Microsoft.Resources/deployments/validate/action | Validates an deployment. |
> | Action | Microsoft.Resources/deployments/write | Creates or updates an deployment. |
> | Action | Microsoft.Resources/links/delete | Deletes a resource link. |
> | Action | Microsoft.Resources/links/read | Gets or lists resource links. |
> | Action | Microsoft.Resources/links/write | Creates or updates a resource link. |
> | Action | Microsoft.Resources/marketplace/purchase/action | Purchases a resource from the marketplace. |
> | Action | Microsoft.Resources/providers/read | Get the list of providers. |
> | Action | Microsoft.Resources/resources/read | Get the list of resources based upon filters. |
> | Action | Microsoft.Resources/subscriptions/locations/read | Gets the list of locations supported. |
> | Action | Microsoft.Resources/subscriptions/operationresults/read | Get the subscription operation results. |
> | Action | Microsoft.Resources/subscriptions/providers/read | Gets or lists resource providers. |
> | Action | Microsoft.Resources/subscriptions/read | Gets the list of subscriptions. |
> | Action | Microsoft.Resources/subscriptions/resourceGroups/delete | Deletes a resource group and all its resources. |
> | Action | Microsoft.Resources/subscriptions/resourcegroups/deployments/operations/read | Gets or lists deployment operations. |
> | Action | Microsoft.Resources/subscriptions/resourcegroups/deployments/operationstatuses/read | Gets or lists deployment operation statuses. |
> | Action | Microsoft.Resources/subscriptions/resourcegroups/deployments/read | Gets or lists deployments. |
> | Action | Microsoft.Resources/subscriptions/resourcegroups/deployments/write | Creates or updates an deployment. |
> | Action | Microsoft.Resources/subscriptions/resourceGroups/moveResources/action | Moves resources from one resource group to another. |
> | Action | Microsoft.Resources/subscriptions/resourceGroups/read | Gets or lists resource groups. |
> | Action | Microsoft.Resources/subscriptions/resourcegroups/resources/read | Gets the resources for the resource group. |
> | Action | Microsoft.Resources/subscriptions/resourceGroups/validateMoveResources/action | Validate move of resources from one resource group to another. |
> | Action | Microsoft.Resources/subscriptions/resourceGroups/write | Creates or updates a resource group. |
> | Action | Microsoft.Resources/subscriptions/resources/read | Gets resources of a subscription. |
> | Action | Microsoft.Resources/subscriptions/tagNames/delete | Deletes a subscription tag. |
> | Action | Microsoft.Resources/subscriptions/tagNames/read | Gets or lists subscription tags. |
> | Action | Microsoft.Resources/subscriptions/tagNames/tagValues/delete | Deletes a subscription tag value. |
> | Action | Microsoft.Resources/subscriptions/tagNames/tagValues/read | Gets or lists subscription tag values. |
> | Action | Microsoft.Resources/subscriptions/tagNames/tagValues/write | Adds a subscription tag value. |
> | Action | Microsoft.Resources/subscriptions/tagNames/write | Adds a subscription tag. |
> | Action | Microsoft.Resources/tenants/read | Gets the list of tenants. |

## Microsoft.Scheduler

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Scheduler/jobcollections/delete | Deletes job collection. |
> | Action | Microsoft.Scheduler/jobcollections/disable/action | Disables job collection. |
> | Action | Microsoft.Scheduler/jobcollections/enable/action | Enables job collection. |
> | Action | Microsoft.Scheduler/jobcollections/jobs/delete | Deletes job. |
> | Action | Microsoft.Scheduler/jobcollections/jobs/generateLogicAppDefinition/action | Generates Logic App definition based on a Scheduler Job. |
> | Action | Microsoft.Scheduler/jobcollections/jobs/jobhistories/read | Gets job history. |
> | Action | Microsoft.Scheduler/jobcollections/jobs/read | Gets job. |
> | Action | Microsoft.Scheduler/jobcollections/jobs/run/action | Runs job. |
> | Action | Microsoft.Scheduler/jobcollections/jobs/write | Creates or updates job. |
> | Action | Microsoft.Scheduler/jobcollections/read | Get Job Collection |
> | Action | Microsoft.Scheduler/jobcollections/write | Creates or updates job collection. |

## Microsoft.Search

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Search/checkNameAvailability/action | Checks availability of the service name. |
> | Action | Microsoft.Search/operations/read | Lists all of the available operations of the Microsoft.Search provider. |
> | Action | Microsoft.Search/register/action | Registers the subscription for the search resource provider and enables the creation of search services. |
> | Action | Microsoft.Search/searchServices/createQueryKey/action | Creates the query key. |
> | Action | Microsoft.Search/searchServices/delete | Deletes the search service. |
> | Action | Microsoft.Search/searchServices/deleteQueryKey/delete | Deletes the query key. |
> | Action | Microsoft.Search/searchServices/diagnosticSettings/read | Gets the diganostic setting read for the resource |
> | Action | Microsoft.Search/searchServices/diagnosticSettings/write | Creates or updates the diganostic setting for the resource |
> | Action | Microsoft.Search/searchServices/listAdminKeys/action | Reads the admin keys. |
> | Action | Microsoft.Search/searchServices/listQueryKeys/read | Returns the list of query API keys for the given Azure Search service. |
> | Action | Microsoft.Search/searchServices/logDefinitions/read | Gets the available logs for the search service |
> | Action | Microsoft.Search/searchServices/metricDefinitions/read | Gets the available metrics for the search service |
> | Action | Microsoft.Search/searchServices/read | Reads the search service. |
> | Action | Microsoft.Search/searchServices/regenerateAdminKey/action | Regenerates the admin key. |
> | Action | Microsoft.Search/searchServices/start/action | Starts the search service. |
> | Action | Microsoft.Search/searchServices/stop/action | Stops the search service. |
> | Action | Microsoft.Search/searchServices/write | Creates or updates the search service. |

## Microsoft.Security

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Security/advancedThreatProtectionSettings/read | Gets the Advanced Threat Protection Settings for the resource |
> | Action | Microsoft.Security/advancedThreatProtectionSettings/write | Updates the Advanced Threat Protection Settings for the resource |
> | Action | Microsoft.Security/alerts/read | Gets all available security alerts |
> | Action | Microsoft.Security/applicationWhitelistings/read | Gets the application whitelistings |
> | Action | Microsoft.Security/applicationWhitelistings/write | Creates a new application whitelisting or updates an existing one |
> | Action | Microsoft.Security/complianceResults/read | Gets the compliance results for the resource |
> | Action | Microsoft.Security/locations/alerts/activate/action | Activate a security alert |
> | Action | Microsoft.Security/locations/alerts/dismiss/action | Dismiss a security alert |
> | Action | Microsoft.Security/locations/alerts/read | Gets all available security alerts |
> | Action | Microsoft.Security/locations/jitNetworkAccessPolicies/delete | Deletes the just-in-time network access policy |
> | Action | Microsoft.Security/locations/jitNetworkAccessPolicies/initiate/action | Initiates a just-in-time network access policy request |
> | Action | Microsoft.Security/locations/jitNetworkAccessPolicies/read | Gets the just-in-time network access policies |
> | Action | Microsoft.Security/locations/jitNetworkAccessPolicies/write | Creates a new just-in-time network access policy or updates an existing one |
> | Action | Microsoft.Security/locations/read | Gets the security data location |
> | Action | Microsoft.Security/locations/tasks/activate/action | Activate a security recommendation |
> | Action | Microsoft.Security/locations/tasks/dismiss/action | Dismiss a security recommendation |
> | Action | Microsoft.Security/locations/tasks/read | Gets all available security recommendations |
> | Action | Microsoft.Security/locations/tasks/resolve/action | Resolve a security recommendation |
> | Action | Microsoft.Security/locations/tasks/start/action | Start a security recommendation |
> | Action | Microsoft.Security/policies/read | Gets the security policy |
> | Action | Microsoft.Security/policies/write | Updates the security policy |
> | Action | Microsoft.Security/pricings/delete | Deletes the pricing settings for the scope |
> | Action | Microsoft.Security/pricings/read | Gets the pricing settings for the scope |
> | Action | Microsoft.Security/pricings/write | Updates the pricing settings for the scope |
> | Action | Microsoft.Security/register/action | Registers the subscription for Azure Security Center |
> | Action | Microsoft.Security/securityContacts/delete | Deletes the security contact |
> | Action | Microsoft.Security/securityContacts/read | Gets the security contact |
> | Action | Microsoft.Security/securityContacts/write | Updates the security contact |
> | Action | Microsoft.Security/securitySolutions/delete | Deletes a security solution |
> | Action | Microsoft.Security/securitySolutions/read | Gets the security solutions |
> | Action | Microsoft.Security/securitySolutions/write | Creates a new security solution or updates an existing one |
> | Action | Microsoft.Security/securitySolutionsReferenceData/read | Gets the security solutions reference data |
> | Action | Microsoft.Security/securityStatuses/read | Gets the security health statuses for Azure resources |
> | Action | Microsoft.Security/securityStatusesSummaries/read | Gets the security statuses summaries for the scope |
> | Action | Microsoft.Security/tasks/read | Gets all available security recommendations |
> | Action | Microsoft.Security/unregister/action | Unregisters the subscription from Azure Security Center |
> | Action | Microsoft.Security/webApplicationFirewalls/delete | Deletes a web application firewall |
> | Action | Microsoft.Security/webApplicationFirewalls/read | Gets the web application firewalls |
> | Action | Microsoft.Security/webApplicationFirewalls/write | Creates a new web application firewall or updates an existing one |
> | Action | Microsoft.Security/workspaceSettings/connect/action | Change workspace settings reconnection settings |
> | Action | Microsoft.Security/workspaceSettings/delete | Deletes the workspace settings |
> | Action | Microsoft.Security/workspaceSettings/read | Gets the workspace settings |
> | Action | Microsoft.Security/workspaceSettings/write | Updates the workspace settings |

## Microsoft.SecurityGraph

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.SecurityGraph/diagnosticsettings/delete | Deleting a diagnostic setting |
> | Action | Microsoft.SecurityGraph/diagnosticsettings/read | Reading a diagnostic setting |
> | Action | Microsoft.SecurityGraph/diagnosticsettings/write | Writing a diagnostic setting |
> | Action | Microsoft.SecurityGraph/diagnosticsettingscategories/read | Reading a diagnostic setting categories |

## Microsoft.ServiceBus

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ServiceBus/checkNameAvailability/action | Checks availability of namespace under given subscription. |
> | Action | Microsoft.ServiceBus/checkNamespaceAvailability/action | Checks availability of namespace under given subscription. This API is deprecated please use CheckNameAvailabiltiy instead. |
> | Action | Microsoft.ServiceBus/namespaces/authorizationRules/action | Updates Namespace Authorization Rule. This API is depricated. Please use a PUT call to update the Namespace Authorization Rule instead.. This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.ServiceBus/namespaces/authorizationRules/delete | Delete Namespace Authorization Rule. The Default Namespace Authorization Rule cannot be deleted.  |
> | Action | Microsoft.ServiceBus/namespaces/authorizationRules/listkeys/action | Get the Connection String to the Namespace |
> | Action | Microsoft.ServiceBus/namespaces/authorizationRules/read | Get the list of Namespaces Authorization Rules description. |
> | Action | Microsoft.ServiceBus/namespaces/authorizationRules/regenerateKeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.ServiceBus/namespaces/authorizationRules/write | Create a Namespace level Authorization Rules and update its properties. The Authorization Rules Access Rights, the Primary and Secondary Keys can be updated. |
> | Action | Microsoft.ServiceBus/namespaces/Delete | Delete Namespace Resource |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/authorizationRules/listkeys/action | Gets the authorization rules keys for the Disaster Recovery primary namespace |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/authorizationRules/read | Get Disaster Recovery Primary Namespace's Authorization Rules |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/breakPairing/action | Disables Disaster Recovery and stops replicating changes from primary to secondary namespaces. |
> | Action | Microsoft.ServiceBus/namespaces/disasterrecoveryconfigs/checkNameAvailability/action | Checks availability of namespace alias under given subscription. |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/delete | Deletes the Disaster Recovery configuration associated with the namespace. This operation can only be invoked via the primary namespace. |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/failover/action | Invokes a GEO DR failover and reconfigures the namespace alias to point to the secondary namespace. |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/read | Gets the Disaster Recovery configuration associated with the namespace. |
> | Action | Microsoft.ServiceBus/namespaces/disasterRecoveryConfigs/write | Creates or Updates the Disaster Recovery configuration associated with the namespace. |
> | Action | Microsoft.ServiceBus/namespaces/eventGridFilters/delete | Deletes the Event Grid filter associated with the namespace. |
> | Action | Microsoft.ServiceBus/namespaces/eventGridFilters/read | Gets the Event Grid filter associated with the namespace. |
> | Action | Microsoft.ServiceBus/namespaces/eventGridFilters/write | Creates or Updates the Event Grid filter associated with the namespace. |
> | Action | Microsoft.ServiceBus/namespaces/eventhubs/read | Get list of EventHub Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/messagingPlan/read | Gets the Messaging Plan for a namespace.<br>This API is deprecated.<br>Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions..<br>This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.ServiceBus/namespaces/messagingPlan/write | Updates the Messaging Plan for a namespace.<br>This API is deprecated.<br>Properties exposed via the MessagingPlan resource are moved to the (parent) Namespace resource in later API versions..<br>This operation is not supported on API version 2017-04-01. |
> | Action | Microsoft.ServiceBus/namespaces/migrate/action | Migrate namespace operation |
> | Action | Microsoft.ServiceBus/namespaces/operationresults/read | Get the status of Namespace operation |
> | Action | Microsoft.ServiceBus/namespaces/providers/Microsoft.Insights/diagnosticSettings/read | Get list of Namespace diagnostic settings Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/providers/Microsoft.Insights/diagnosticSettings/write | Get list of Namespace diagnostic settings Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/providers/Microsoft.Insights/logDefinitions/read | Get list of Namespace logs Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/providers/Microsoft.Insights/metricDefinitions/read | Get list of Namespace metrics Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/queues/authorizationRules/action | Operation to update Queue. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule. |
> | Action | Microsoft.ServiceBus/namespaces/queues/authorizationRules/delete | Operation to delete Queue Authorization Rules |
> | Action | Microsoft.ServiceBus/namespaces/queues/authorizationRules/listkeys/action | Get the Connection String to Queue |
> | Action | Microsoft.ServiceBus/namespaces/queues/authorizationRules/read |  Get the list of Queue Authorization Rules |
> | Action | Microsoft.ServiceBus/namespaces/queues/authorizationRules/regenerateKeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.ServiceBus/namespaces/queues/authorizationRules/write | Create Queue Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated. |
> | Action | Microsoft.ServiceBus/namespaces/queues/Delete | Operation to delete Queue Resource |
> | Action | Microsoft.ServiceBus/namespaces/queues/read | Get list of Queue Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/queues/write | Create or Update Queue properties. |
> | Action | Microsoft.ServiceBus/namespaces/read | Get the list of Namespace Resource Description |
> | Action | Microsoft.ServiceBus/namespaces/removeAcsNamepsace/action | Remove ACS namespace |
> | Action | Microsoft.ServiceBus/namespaces/topics/authorizationRules/action | Operation to update Topic. This operation is not supported on API version 2017-04-01. Authorization Rules. Please use a PUT call to update Authorization Rule. |
> | Action | Microsoft.ServiceBus/namespaces/topics/authorizationRules/delete | Operation to delete Topic Authorization Rules |
> | Action | Microsoft.ServiceBus/namespaces/topics/authorizationRules/listkeys/action | Get the Connection String to Topic |
> | Action | Microsoft.ServiceBus/namespaces/topics/authorizationRules/read |  Get the list of Topic Authorization Rules |
> | Action | Microsoft.ServiceBus/namespaces/topics/authorizationRules/regenerateKeys/action | Regenerate the Primary or Secondary key to the Resource |
> | Action | Microsoft.ServiceBus/namespaces/topics/authorizationRules/write | Create Topic Authorization Rules and Update its properties. The Authorization Rules Access Rights can be updated. |
> | Action | Microsoft.ServiceBus/namespaces/topics/Delete | Operation to delete Topic Resource |
> | Action | Microsoft.ServiceBus/namespaces/topics/read | Get list of Topic Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/topics/subscriptions/Delete | Operation to delete TopicSubscription Resource |
> | Action | Microsoft.ServiceBus/namespaces/topics/subscriptions/read | Get list of TopicSubscription Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/topics/subscriptions/rules/Delete | Operation to delete Rule Resource |
> | Action | Microsoft.ServiceBus/namespaces/topics/subscriptions/rules/read | Get list of Rule Resource Descriptions |
> | Action | Microsoft.ServiceBus/namespaces/topics/subscriptions/rules/write | Create or Update Rule properties. |
> | Action | Microsoft.ServiceBus/namespaces/topics/subscriptions/write | Create or Update TopicSubscription properties. |
> | Action | Microsoft.ServiceBus/namespaces/topics/write | Create or Update Topic properties. |
> | Action | Microsoft.ServiceBus/namespaces/write | Create a Namespace Resource and Update its properties. Tags and Capacity of the Namespace are the properties which can be updated. |
> | Action | Microsoft.ServiceBus/operations/read | Get Operations |
> | Action | Microsoft.ServiceBus/register/action | Registers the subscription for the ServiceBus resource provider and enables the creation of ServiceBus resources |
> | Action | Microsoft.ServiceBus/sku/read | Get list of Sku Resource Descriptions |
> | Action | Microsoft.ServiceBus/sku/regions/read | Get list of SkuRegions Resource Descriptions |
> | Action | Microsoft.ServiceBus/unregister/action | Registers the subscription for the ServiceBus resource provider and enables the creation of ServiceBus resources |

## Microsoft.ServiceFabric

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.ServiceFabric/clusters/applications/delete | Delete any Application |
> | Action | Microsoft.ServiceFabric/clusters/applications/read | Read any Application |
> | Action | Microsoft.ServiceFabric/clusters/applications/services/delete | Delete any Service |
> | Action | Microsoft.ServiceFabric/clusters/applications/services/partitions/read | Read any Partition |
> | Action | Microsoft.ServiceFabric/clusters/applications/services/partitions/replicas/read | Read any Replica |
> | Action | Microsoft.ServiceFabric/clusters/applications/services/read | Read any Service |
> | Action | Microsoft.ServiceFabric/clusters/applications/services/statuses/read | Read any Service Status |
> | Action | Microsoft.ServiceFabric/clusters/applications/services/write | Create or Update any Service |
> | Action | Microsoft.ServiceFabric/clusters/applications/write | Create or Update any Application |
> | Action | Microsoft.ServiceFabric/clusters/applicationTypes/delete | Delete any Application Type |
> | Action | Microsoft.ServiceFabric/clusters/applicationTypes/read | Read any Application Type |
> | Action | Microsoft.ServiceFabric/clusters/applicationTypes/versions/delete | Delete any Application Type Version |
> | Action | Microsoft.ServiceFabric/clusters/applicationTypes/versions/read | Read any Application Type Version |
> | Action | Microsoft.ServiceFabric/clusters/applicationTypes/versions/write | Create or Update any Application Type Version |
> | Action | Microsoft.ServiceFabric/clusters/applicationTypes/write | Create or Update any Application Type |
> | Action | Microsoft.ServiceFabric/clusters/delete | Delete any Cluster |
> | Action | Microsoft.ServiceFabric/clusters/nodes/read | Read any Node |
> | Action | Microsoft.ServiceFabric/clusters/read | Read any Cluster |
> | Action | Microsoft.ServiceFabric/clusters/statuses/read | Read any Cluster Status |
> | Action | Microsoft.ServiceFabric/clusters/write | Create or Update any Cluster |
> | Action | Microsoft.ServiceFabric/locations/clusterVersions/read | Read any Cluster Version |
> | Action | Microsoft.ServiceFabric/locations/environments/clusterVersions/read | Read any Cluster Version for a specific environment |
> | Action | Microsoft.ServiceFabric/locations/operationresults/read | Read any Operation Results |
> | Action | Microsoft.ServiceFabric/locations/operations/read | Read any Operations by location |
> | Action | Microsoft.ServiceFabric/operations/read | Read any Available Operations |
> | Action | Microsoft.ServiceFabric/register/action | Register any Action |

## Microsoft.SignalRService

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.SignalRService/checknameavailability/action | Checks if a name is available for use with a new SignalR service |
> | Action | Microsoft.SignalRService/register/action | Registers the 'Microsoft.SignalRService' resource provider with a subscription |
> | Action | Microsoft.SignalRService/SignalR/delete | Delete the entire SignalR |
> | Action | Microsoft.SignalRService/SignalR/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.SignalRService/SignalR/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.SignalRService/SignalR/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for SignalR |
> | Action | Microsoft.SignalRService/SignalR/read | View the SignalR's settings and configurations in the management portal or through API |
> | Action | Microsoft.SignalRService/SignalR/write | Modify the SignalR's settings and configurations in the management portal or through API |
> | Action | Microsoft.SignalRService/unregister/action | Unregisters the 'Microsoft.SignalRService' resource provider with a subscription |

## Microsoft.Solutions

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Solutions/applicationDefinitions/delete | Removes an application definition. |
> | Action | Microsoft.Solutions/applicationDefinitions/read | Retrieves a list of application definitions. |
> | Action | Microsoft.Solutions/applicationDefinitions/write | Add or modify an application definition. |
> | Action | Microsoft.Solutions/applications/delete | Removes an application. |
> | Action | Microsoft.Solutions/applications/read | Retrieves a list of applications. |
> | Action | Microsoft.Solutions/applications/write | Creates an application. |
> | Action | Microsoft.Solutions/jitRequests/delete | Remove a JitRequest |
> | Action | Microsoft.Solutions/jitRequests/read | Retrieves a list of JitRequests |
> | Action | Microsoft.Solutions/jitRequests/write | Creates a JitRequest |
> | Action | Microsoft.Solutions/locations/operationStatuses/read | Reads the operation status for the resource. |
> | Action | Microsoft.Solutions/register/action | Register to Solutions. |

## Microsoft.Sql

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Sql/checkNameAvailability/action | Verify whether given server name is available for provisioning worldwide for a given subscription. |
> | Action | Microsoft.Sql/locations/auditingSettingsAzureAsyncOperation/read | Retrieve result of the extended server blob auditing policy Set operation |
> | Action | Microsoft.Sql/locations/auditingSettingsOperationResults/read | Retrieve result of the server blob auditing policy Set operation |
> | Action | Microsoft.Sql/locations/capabilities/read | Gets the capabilities for this subscription in a given location |
> | Action | Microsoft.Sql/locations/databaseAzureAsyncOperation/read | Gets the status of a database operation. |
> | Action | Microsoft.Sql/locations/databaseOperationResults/read | Gets the status of a database operation. |
> | Action | Microsoft.Sql/locations/deletedServerAsyncOperation/read | Gets in-progress operations on deleted server |
> | Action | Microsoft.Sql/locations/deletedServerOperationResults/read | Gets in-progress operations on deleted server |
> | Action | Microsoft.Sql/locations/deletedServers/read | Return the list of deleted servers or gets the properties for the specified deleted server. |
> | Action | Microsoft.Sql/locations/deletedServers/recover/action | Recover a deleted server |
> | Action | Microsoft.Sql/locations/deleteVirtualNetworkOrSubnets/action | Deletes Virtual network rules associated to a virtual network or subnet |
> | Action | Microsoft.Sql/locations/elasticPoolAzureAsyncOperation/read | Gets the azure async operation for an elastic pool async operation |
> | Action | Microsoft.Sql/locations/elasticPoolOperationResults/read | Gets the result of an elastic pool operation. |
> | Action | Microsoft.Sql/locations/extendedAuditingSettingsAzureAsyncOperation/read | Retrieve result of the extended server blob auditing policy Set operation |
> | Action | Microsoft.Sql/locations/extendedAuditingSettingsOperationResults/read | Retrieve result of the extended server blob auditing policy Set operation |
> | Action | Microsoft.Sql/locations/instanceFailoverGroups/delete | Deletes an existing instance failover group. |
> | Action | Microsoft.Sql/locations/instanceFailoverGroups/failover/action | Executes planned failover in an existing instance failover group. |
> | Action | Microsoft.Sql/locations/instanceFailoverGroups/forceFailoverAllowDataLoss/action | Executes forced failover in an existing instance failover group. |
> | Action | Microsoft.Sql/locations/instanceFailoverGroups/read | Returns the list of instance failover groups or gets the properties for the specified instance failover group. |
> | Action | Microsoft.Sql/locations/instanceFailoverGroups/write | Creates a instance failover group with the specified parameters or updates the properties or tags for the specified instance failover group. |
> | Action | Microsoft.Sql/locations/interfaceEndpointProfileAzureAsyncOperation/read | Returns the details of a specific interface endpoint Azure async operation |
> | Action | Microsoft.Sql/locations/interfaceEndpointProfileOperationResults/read | Returns the details of the specified interface endpoint profile operation |
> | Action | Microsoft.Sql/locations/jobAgentAzureAsyncOperation/read | Gets the status of an job agent operation. |
> | Action | Microsoft.Sql/locations/jobAgentOperationResults/read | Gets the result of an job agent operation. |
> | Action | Microsoft.Sql/locations/longTermRetentionBackups/read | Lists the long term retention backups for every database on every server in a location |
> | Action | Microsoft.Sql/locations/longTermRetentionServers/longTermRetentionBackups/read | Lists the long term retention backups for every database on a server |
> | Action | Microsoft.Sql/locations/longTermRetentionServers/longTermRetentionDatabases/longTermRetentionBackups/delete | Deletes a long term retention backup |
> | Action | Microsoft.Sql/locations/longTermRetentionServers/longTermRetentionDatabases/longTermRetentionBackups/read | Lists the long term retention backups for a database |
> | Action | Microsoft.Sql/locations/managedDatabaseRestoreAzureAsyncOperation/completeRestore/action | Completes managed database restore operation |
> | Action | Microsoft.Sql/locations/managedTransparentDataEncryptionAzureAsyncOperation/read | Gets in-progress operations on managed database transparent data encryption |
> | Action | Microsoft.Sql/locations/managedTransparentDataEncryptionOperationResults/read | Gets in-progress operations on managed database transparent data encryption |
> | Action | Microsoft.Sql/locations/read | Gets the available locations for a given subscription |
> | Action | Microsoft.Sql/locations/syncAgentOperationResults/read | Retrieve result of the sync agent resource operation |
> | Action | Microsoft.Sql/locations/syncDatabaseIds/read | Retrieve the sync database ids for a particular region and subscription |
> | Action | Microsoft.Sql/locations/syncGroupOperationResults/read | Retrieve result of the sync group resource operation |
> | Action | Microsoft.Sql/locations/syncMemberOperationResults/read | Retrieve result of the sync member resource operation |
> | Action | Microsoft.Sql/locations/usages/read | Gets a collection of usage metrics for this subscription in a location |
> | Action | Microsoft.Sql/locations/virtualNetworkRulesAzureAsyncOperation/read | Returns the details of the specified virtual network rules azure async operation  |
> | Action | Microsoft.Sql/locations/virtualNetworkRulesOperationResults/read | Returns the details of the specified virtual network rules operation  |
> | Action | Microsoft.Sql/managedInstances/administrators/delete | Deletes an existing administrator of managed instance. |
> | Action | Microsoft.Sql/managedInstances/administrators/read | Gets a list of managed instance administrators. |
> | Action | Microsoft.Sql/managedInstances/administrators/write | Creates or updates managed instance administrator with the specified parameters. |
> | Action | Microsoft.Sql/managedInstances/databases/backupShortTermRetentionPolicies/read | Gets a short term retention policy for a managed database |
> | Action | Microsoft.Sql/managedInstances/databases/backupShortTermRetentionPolicies/write | Updates a short term retention policy for a managed database |
> | Action | Microsoft.Sql/managedInstances/databases/delete | Deletes an existing managed database |
> | Action | Microsoft.Sql/managedInstances/databases/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Sql/managedInstances/databases/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Sql/managedInstances/databases/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for managed instance databases |
> | Action | Microsoft.Sql/managedInstances/databases/read | Gets existing managed database |
> | Action | Microsoft.Sql/managedInstances/databases/securityAlertPolicies/read | Retrieve details of the database threat detection policy configured on a given managed database |
> | Action | Microsoft.Sql/managedInstances/databases/securityAlertPolicies/write | Change the database threat detection policy for a given managed database |
> | Action | Microsoft.Sql/managedInstances/databases/securityEvents/read | Retrieves the managed database security events |
> | Action | Microsoft.Sql/managedInstances/databases/transparentDataEncryption/read | Retrieve details of the database Transparent Data Encryption on a given managed database |
> | Action | Microsoft.Sql/managedInstances/databases/transparentDataEncryption/write | Change the database Transparent Data Encryption for a given managed database |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/delete | Remove the vulnerability assessment for a given database |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/read | Retrieve details of the vulnerability assessment configured on a given database |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/rules/baselines/delete | Remove the vulnerability assessment rule baseline for a given database |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/rules/baselines/read | Get the vulnerability assessment rule baseline for a given database |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/rules/baselines/write | Change the vulnerability assessment rule baseline for a given database |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/scans/export/action | Convert an existing scan result to a human readable format. If already exists nothing happens |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/scans/initiateScan/action | Execute vulnerability assessment database scan. |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/scans/read | Return the list of database vulnerability assessment scan records or get the scan record for the specified scan ID. |
> | Action | Microsoft.Sql/managedInstances/databases/vulnerabilityAssessments/write | Change the vulnerability assessment for a given database |
> | Action | Microsoft.Sql/managedInstances/databases/write | Creates a new database or updates an existing database. |
> | Action | Microsoft.Sql/managedInstances/delete | Deletes an existing  managed instance. |
> | Action | Microsoft.Sql/managedInstances/encryptionProtector/read | Returns a list of server encryption protectors or gets the properties for the specified server encryption protector. |
> | Action | Microsoft.Sql/managedInstances/encryptionProtector/write | Update the properties for the specified Server Encryption Protector. |
> | Action | Microsoft.Sql/managedInstances/keys/delete | Deletes an existing Azure SQL Managed Instance  key. |
> | Action | Microsoft.Sql/managedInstances/keys/read | Return the list of managed instance keys or gets the properties for the specified managed instance key. |
> | Action | Microsoft.Sql/managedInstances/keys/write | Creates a key with the specified parameters or update the properties or tags for the specified managed instance key. |
> | Action | Microsoft.Sql/managedInstances/metricDefinitions/read | Get managed instance metric definitions |
> | Action | Microsoft.Sql/managedInstances/metrics/read | Get managed instance metrics |
> | Action | Microsoft.Sql/managedInstances/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Sql/managedInstances/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Sql/managedInstances/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for managed instances |
> | Action | Microsoft.Sql/managedInstances/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for managed instances |
> | Action | Microsoft.Sql/managedInstances/read | Return the list of managed instances or gets the properties for the specified managed instance. |
> | Action | Microsoft.Sql/managedInstances/restorableDroppedDatabases/backupShortTermRetentionPolicies/read | Gets a short term retention policy for a dropped managed database |
> | Action | Microsoft.Sql/managedInstances/restorableDroppedDatabases/backupShortTermRetentionPolicies/write | Updates a short term retention policy for a dropped managed database |
> | Action | Microsoft.Sql/managedInstances/restorableDroppedDatabases/read | Returns a list of restorable dropped managed databases. |
> | Action | Microsoft.Sql/managedInstances/securityAlertPolicies/read | Retrieve details of the managed server threat detection policy configured on a given managed server |
> | Action | Microsoft.Sql/managedInstances/securityAlertPolicies/write | Change the managed server threat detection policy for a given managed server |
> | Action | Microsoft.Sql/managedInstances/tdeCertificates/action | Create/Update TDE certificate |
> | Action | Microsoft.Sql/managedInstances/vulnerabilityAssessments/delete | Remove the vulnerability assessment for a given managed instance |
> | Action | Microsoft.Sql/managedInstances/vulnerabilityAssessments/read | Retrieve details of the vulnerability assessment configured on a given managed instance |
> | Action | Microsoft.Sql/managedInstances/vulnerabilityAssessments/write | Change the vulnerability assessment for a given managed instance |
> | Action | Microsoft.Sql/managedInstances/write | Creates a managed instance with the specified parameters or update the properties or tags for the specified managed instance. |
> | Action | Microsoft.Sql/operations/read | Gets available REST operations |
> | Action | Microsoft.Sql/register/action | Registers the subscription for the Microsoft SQL Database resource provider and enables the creation of Microsoft SQL Databases. |
> | Action | Microsoft.Sql/servers/administratorOperationResults/read | Gets in-progress operations on server administrators |
> | Action | Microsoft.Sql/servers/administrators/delete | Delete server administrator |
> | Action | Microsoft.Sql/servers/administrators/read | Retrieve server administrator details |
> | Action | Microsoft.Sql/servers/administrators/write | Create or update server administrator |
> | Action | Microsoft.Sql/servers/advisors/read | Returns list of advisors available for the server |
> | Action | Microsoft.Sql/servers/advisors/recommendedActions/read | Returns list of recommended actions of specified advisor for the server |
> | Action | Microsoft.Sql/servers/advisors/recommendedActions/write | Apply the recommended action on the server |
> | Action | Microsoft.Sql/servers/advisors/write | Updates auto-execute status of an advisor on server level. |
> | Action | Microsoft.Sql/servers/auditingPolicies/read | Retrieve details of the default server table auditing policy configured on a given server |
> | Action | Microsoft.Sql/servers/auditingPolicies/write | Change the default server table auditing for a given server |
> | Action | Microsoft.Sql/servers/auditingSettings/operationResults/read | Retrieve result of the server blob auditing policy Set operation |
> | Action | Microsoft.Sql/servers/auditingSettings/read | Retrieve details of the server blob auditing policy configured on a given server |
> | Action | Microsoft.Sql/servers/auditingSettings/write | Change the server blob auditing for a given server |
> | Action | Microsoft.Sql/servers/automaticTuning/read | Returns automatic tuning settings for the server |
> | Action | Microsoft.Sql/servers/automaticTuning/write | Updates automatic tuning settings for the server and returns updated settings |
> | Action | Microsoft.Sql/servers/backupLongTermRetentionVaults/delete | Deletes an existing backup archival vault. |
> | Action | Microsoft.Sql/servers/backupLongTermRetentionVaults/read | This operation is used to get a backup long term retention vault. It returns information about the vault registered to this server |
> | Action | Microsoft.Sql/servers/backupLongTermRetentionVaults/write | This operation is used to register a backup long term retention vault to a server |
> | Action | Microsoft.Sql/servers/communicationLinks/delete | Deletes an existing server communication link. |
> | Action | Microsoft.Sql/servers/communicationLinks/read | Return the list of communication links of a specified server. |
> | Action | Microsoft.Sql/servers/communicationLinks/write | Create or update a server communication link. |
> | Action | Microsoft.Sql/servers/connectionPolicies/read | Return the list of server connection policies of a specified server. |
> | Action | Microsoft.Sql/servers/connectionPolicies/write | Create or update a server connection policy. |
> | Action | Microsoft.Sql/servers/databases/advisors/read | Returns list of advisors available for the database |
> | Action | Microsoft.Sql/servers/databases/advisors/recommendedActions/read | Returns list of recommended actions of specified advisor for the database |
> | Action | Microsoft.Sql/servers/databases/advisors/recommendedActions/write | Apply the recommended action on the database |
> | Action | Microsoft.Sql/servers/databases/advisors/write | Update auto-execute status of an advisor on database level. |
> | Action | Microsoft.Sql/servers/databases/auditingPolicies/read | Retrieve details of the table auditing policy configured on a given database |
> | Action | Microsoft.Sql/servers/databases/auditingPolicies/write | Change the table auditing policy for a given database |
> | Action | Microsoft.Sql/servers/databases/auditingSettings/read | Retrieve details of the blob auditing policy configured on a given database |
> | Action | Microsoft.Sql/servers/databases/auditingSettings/write | Change the blob auditing policy for a given database |
> | Action | Microsoft.Sql/servers/databases/auditRecords/read | Retrieve the database blob audit records |
> | Action | Microsoft.Sql/servers/databases/automaticTuning/read | Returns automatic tuning settings for a database |
> | Action | Microsoft.Sql/servers/databases/automaticTuning/write | Updates automatic tuning settings for a database and returns updated settings |
> | Action | Microsoft.Sql/servers/databases/azureAsyncOperation/read | Gets the status of a database operation. |
> | Action | Microsoft.Sql/servers/databases/backupLongTermRetentionPolicies/read | Return the list of backup archival policies of a specified database. |
> | Action | Microsoft.Sql/servers/databases/backupLongTermRetentionPolicies/write | Create or update a database backup archival policy. |
> | Action | Microsoft.Sql/servers/databases/connectionPolicies/read | Retrieve details of the connection policy configured on a given database |
> | Action | Microsoft.Sql/servers/databases/connectionPolicies/write | Change connection policy for a given database |
> | Action | Microsoft.Sql/servers/databases/dataMaskingPolicies/read | Return the list of database data masking policies. |
> | Action | Microsoft.Sql/servers/databases/dataMaskingPolicies/rules/delete | Delete data masking policy rule for a given database |
> | Action | Microsoft.Sql/servers/databases/dataMaskingPolicies/rules/read | Retrieve details of the data masking policy rule configured on a given database |
> | Action | Microsoft.Sql/servers/databases/dataMaskingPolicies/rules/write | Change data masking policy rule for a given database |
> | Action | Microsoft.Sql/servers/databases/dataMaskingPolicies/write | Change data masking policy for a given database |
> | Action | Microsoft.Sql/servers/databases/dataWarehouseQueries/dataWarehouseQuerySteps/read | Returns the distributed query step information of data warehouse query for selected step ID |
> | Action | Microsoft.Sql/servers/databases/dataWarehouseQueries/read | Returns the data warehouse distribution query information for selected query ID |
> | Action | Microsoft.Sql/servers/databases/dataWarehouseUserActivities/read | Retrieves the user activities of a SQL Data Warehouse instance which includes running and suspended queries |
> | Action | Microsoft.Sql/servers/databases/delete | Deletes an existing database. |
> | Action | Microsoft.Sql/servers/databases/export/action | Export Azure SQL Database |
> | Action | Microsoft.Sql/servers/databases/extendedAuditingSettings/read | Retrieve details of the extended blob auditing policy configured on a given database |
> | Action | Microsoft.Sql/servers/databases/extendedAuditingSettings/write | Change the extended blob auditing policy for a given database |
> | Action | Microsoft.Sql/servers/databases/extensions/read | Gets a collection of extensions for the database. |
> | Action | Microsoft.Sql/servers/databases/extensions/write | Change the extension for a given database |
> | Action | Microsoft.Sql/servers/databases/geoBackupPolicies/read | Retrieve geo backup policies for a given database |
> | Action | Microsoft.Sql/servers/databases/geoBackupPolicies/write | Create or update a database geobackup policy |
> | Action | Microsoft.Sql/servers/databases/importExportOperationResults/read | Gets in-progress import/export operations |
> | Action | Microsoft.Sql/servers/databases/maintenanceWindowOptions/read | Gets a list of available maintenance windows for a selected database. |
> | Action | Microsoft.Sql/servers/databases/maintenanceWindows/read | Gets maintenance windows settings for a selected database. |
> | Action | Microsoft.Sql/servers/databases/maintenanceWindows/write | Sets maintenance windows settings for a selected database. |
> | Action | Microsoft.Sql/servers/databases/metricDefinitions/read | Return types of metrics that are available for databases |
> | Action | Microsoft.Sql/servers/databases/metrics/read | Return metrics for databases |
> | Action | Microsoft.Sql/servers/databases/move/action | Rename Azure SQL Database |
> | Action | Microsoft.Sql/servers/databases/operationResults/read | Gets the status of a database operation. |
> | Action | Microsoft.Sql/servers/databases/operations/cancel/action | Cancels Azure SQL Database pending asynchronous operation that is not finished yet. |
> | Action | Microsoft.Sql/servers/databases/operations/read | Return the list of operations performed on the database |
> | Action | Microsoft.Sql/servers/databases/pause/action | Pause Azure SQL Datawarehouse Database |
> | Action | Microsoft.Sql/servers/databases/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Sql/servers/databases/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Sql/servers/databases/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for databases |
> | Action | Microsoft.Sql/servers/databases/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for databases |
> | Action | Microsoft.Sql/servers/databases/queryStore/queryTexts/read | Returns the collection of query texts that correspond to the specified parameters. |
> | Action | Microsoft.Sql/servers/databases/queryStore/read | Returns current values of Query Store settings for the database. |
> | Action | Microsoft.Sql/servers/databases/queryStore/write | Updates Query Store setting for the database |
> | Action | Microsoft.Sql/servers/databases/read | Return the list of databases or gets the properties for the specified database. |
> | Action | Microsoft.Sql/servers/databases/replicationLinks/delete | Terminate the replication relationship forcefully and with potential data loss |
> | Action | Microsoft.Sql/servers/databases/replicationLinks/failover/action | Failover after synchronizing all changes from the primary, making this database into the replication relationship\u0027s primary and making the remote primary into a secondary |
> | Action | Microsoft.Sql/servers/databases/replicationLinks/forceFailoverAllowDataLoss/action | Failover immediately with potential data loss, making this database into the replication relationship\u0027s primary and making the remote primary into a secondary |
> | Action | Microsoft.Sql/servers/databases/replicationLinks/read | Return the list of replication links or gets the properties for the specified replication links. |
> | Action | Microsoft.Sql/servers/databases/replicationLinks/unlink/action | Terminate the replication relationship forcefully or after synchronizing with the partner |
> | Action | Microsoft.Sql/servers/databases/replicationLinks/updateReplicationMode/action | Update replication mode for link to synchronous or asynchronous mode |
> | Action | Microsoft.Sql/servers/databases/restorePoints/action | Creates a new restore point |
> | Action | Microsoft.Sql/servers/databases/restorePoints/delete | Deletes a restore point for the database. |
> | Action | Microsoft.Sql/servers/databases/restorePoints/read | Returns restore points for the database. |
> | Action | Microsoft.Sql/servers/databases/resume/action | Resume Azure SQL Datawarehouse Database |
> | Action | Microsoft.Sql/servers/databases/schemas/read | Retrieve list of schemas of a database |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/columns/read | Retrieve list of columns of a table |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/columns/sensitivityLabels/delete | Delete the sensitivity label of a given column |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/columns/sensitivityLabels/read | Get the sensitivity label of a given column |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/columns/sensitivityLabels/write | Create or update the sensitivity label of a given column |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/read | Retrieve list of tables of a database |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/recommendedIndexes/read | Retrieve list of index recommendations on a database |
> | Action | Microsoft.Sql/servers/databases/schemas/tables/recommendedIndexes/write | Apply index recommendation |
> | Action | Microsoft.Sql/servers/databases/securityAlertPolicies/read | Retrieve details of the threat detection policy configured on a given database |
> | Action | Microsoft.Sql/servers/databases/securityAlertPolicies/write | Change the threat detection policy for a given database |
> | Action | Microsoft.Sql/servers/databases/securityMetrics/read | Gets a collection of database security metrics |
> | Action | Microsoft.Sql/servers/databases/sensitivityLabels/read | List sensitivity labels of a given database |
> | Action | Microsoft.Sql/servers/databases/serviceTierAdvisors/read | Return suggestion about scaling database up or down based on query execution statistics to improve performance or reduce cost |
> | Action | Microsoft.Sql/servers/databases/skus/read | Gets a collection of skus available for a database |
> | Action | Microsoft.Sql/servers/databases/syncGroups/cancelSync/action | Cancel sync group synchronization |
> | Action | Microsoft.Sql/servers/databases/syncGroups/delete | Deletes an existing sync group. |
> | Action | Microsoft.Sql/servers/databases/syncGroups/hubSchemas/read | Return the list of sync hub database schemas |
> | Action | Microsoft.Sql/servers/databases/syncGroups/logs/read | Return the list of sync group logs |
> | Action | Microsoft.Sql/servers/databases/syncGroups/read | Return the list of sync groups or gets the properties for the specified sync group. |
> | Action | Microsoft.Sql/servers/databases/syncGroups/refreshHubSchema/action | Refresh sync hub database schema |
> | Action | Microsoft.Sql/servers/databases/syncGroups/refreshHubSchemaOperationResults/read | Retrieve result of the sync hub schema refresh operation |
> | Action | Microsoft.Sql/servers/databases/syncGroups/syncMembers/delete | Deletes an existing sync member. |
> | Action | Microsoft.Sql/servers/databases/syncGroups/syncMembers/read | Return the list of sync members or gets the properties for the specified sync member. |
> | Action | Microsoft.Sql/servers/databases/syncGroups/syncMembers/refreshSchema/action | Refresh sync member schema |
> | Action | Microsoft.Sql/servers/databases/syncGroups/syncMembers/refreshSchemaOperationResults/read | Retrieve result of the sync member schema refresh operation |
> | Action | Microsoft.Sql/servers/databases/syncGroups/syncMembers/schemas/read | Return the list of sync member database schemas |
> | Action | Microsoft.Sql/servers/databases/syncGroups/syncMembers/write | Creates a sync member with the specified parameters or update the properties for the specified sync member. |
> | Action | Microsoft.Sql/servers/databases/syncGroups/triggerSync/action | Trigger sync group synchronization |
> | Action | Microsoft.Sql/servers/databases/syncGroups/write | Creates a sync group with the specified parameters or update the properties for the specified sync group. |
> | Action | Microsoft.Sql/servers/databases/topQueries/queryText/action | Returns the Transact-SQL text for selected query ID |
> | Action | Microsoft.Sql/servers/databases/topQueries/read | Returns aggregated runtime statistics for selected query in selected time period |
> | Action | Microsoft.Sql/servers/databases/topQueries/statistics/read | Returns aggregated runtime statistics for selected query in selected time period |
> | Action | Microsoft.Sql/servers/databases/transparentDataEncryption/operationResults/read | Gets in-progress operations on transparent data encryption |
> | Action | Microsoft.Sql/servers/databases/transparentDataEncryption/read | Retrieve status and details of transparent data encryption security feature for a given database |
> | Action | Microsoft.Sql/servers/databases/transparentDataEncryption/write | Change transparent data encryption state |
> | Action | Microsoft.Sql/servers/databases/upgradeDataWarehouse/action | Upgrade Azure SQL Datawarehouse Database |
> | Action | Microsoft.Sql/servers/databases/usages/read | Gets the Azure SQL Database usages information |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/delete | Remove the vulnerability assessment for a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/read | Retrieve details of the vulnerability assessment configured on a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/rules/baselines/delete | Remove the vulnerability assessment rule baseline for a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/rules/baselines/read | Get the vulnerability assessment rule baseline for a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/rules/baselines/write | Change the vulnerability assessment rule baseline for a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/scans/export/action | Convert an existing scan result to a human readable format. If already exists nothing happens |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/scans/initiateScan/action | Execute vulnerability assessment database scan. |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/scans/read | Return the list of database vulnerability assessment scan records or get the scan record for the specified scan ID. |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessments/write | Change the vulnerability assessment for a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessmentScans/action | Execute vulnerability assessment database scan. |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessmentScans/operationResults/read | Retrieve the result of the database vulnerability assessment scan Execute operation |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessmentSettings/read | Retrieve details of the vulnerability assessment configured on a given database |
> | Action | Microsoft.Sql/servers/databases/vulnerabilityAssessmentSettings/write | Change the vulnerability assessment for a given database |
> | Action | Microsoft.Sql/servers/databases/write | Creates a database with the specified parameters or update the properties or tags for the specified database. |
> | Action | Microsoft.Sql/servers/delete | Deletes an existing server. |
> | Action | Microsoft.Sql/servers/disasterRecoveryConfiguration/delete | Deletes an existing disaster recovery configurations for a given server |
> | Action | Microsoft.Sql/servers/disasterRecoveryConfiguration/failover/action | Failover a DisasterRecoveryConfiguration |
> | Action | Microsoft.Sql/servers/disasterRecoveryConfiguration/forceFailoverAllowDataLoss/action | Force Failover a DisasterRecoveryConfiguration |
> | Action | Microsoft.Sql/servers/disasterRecoveryConfiguration/read | Gets a collection of disaster recovery configurations that include this server |
> | Action | Microsoft.Sql/servers/disasterRecoveryConfiguration/write | Change server disaster recovery configuration |
> | Action | Microsoft.Sql/servers/elasticPoolEstimates/read | Returns list of elastic pool estimates already created for this server |
> | Action | Microsoft.Sql/servers/elasticPoolEstimates/write | Creates new elastic pool estimate for list of databases provided |
> | Action | Microsoft.Sql/servers/elasticPools/advisors/read | Returns list of advisors available for the elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/advisors/recommendedActions/read | Returns list of recommended actions of specified advisor for the elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/advisors/recommendedActions/write | Apply the recommended action on the elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/advisors/write | Update auto-execute status of an advisor on elastic pool level. |
> | Action | Microsoft.Sql/servers/elasticPools/databases/read | Gets a list of databases for an elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/delete | Delete existing elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/elasticPoolActivity/read | Retrieve activities and details on a given elastic database pool |
> | Action | Microsoft.Sql/servers/elasticPools/elasticPoolDatabaseActivity/read | Retrieve activities and details on a given database that is part of elastic database pool |
> | Action | Microsoft.Sql/servers/elasticPools/metricDefinitions/read | Return types of metrics that are available for elastic database pools |
> | Action | Microsoft.Sql/servers/elasticPools/metrics/read | Return metrics for elastic database pools |
> | Action | Microsoft.Sql/servers/elasticPools/operations/cancel/action | Cancels Azure SQL elastic pool pending asynchronous operation that is not finished yet. |
> | Action | Microsoft.Sql/servers/elasticPools/operations/read | Return the list of operations performed on the elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.Sql/servers/elasticPools/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Sql/servers/elasticPools/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for elastic database pools |
> | Action | Microsoft.Sql/servers/elasticPools/read | Retrieve details of elastic pool on a given server |
> | Action | Microsoft.Sql/servers/elasticPools/skus/read | Gets a collection of skus available for an elastic pool |
> | Action | Microsoft.Sql/servers/elasticPools/write | Create a new or change properties of existing elastic pool |
> | Action | Microsoft.Sql/servers/encryptionProtector/read | Returns a list of server encryption protectors or gets the properties for the specified server encryption protector. |
> | Action | Microsoft.Sql/servers/encryptionProtector/write | Update the properties for the specified Server Encryption Protector. |
> | Action | Microsoft.Sql/servers/extendedAuditingSettings/read | Retrieve details of the extended server blob auditing policy configured on a given server |
> | Action | Microsoft.Sql/servers/extendedAuditingSettings/write | Change the extended server blob auditing for a given server |
> | Action | Microsoft.Sql/servers/failoverGroups/delete | Deletes an existing failover group. |
> | Action | Microsoft.Sql/servers/failoverGroups/failover/action | Executes planned failover in an existing failover group. |
> | Action | Microsoft.Sql/servers/failoverGroups/forceFailoverAllowDataLoss/action | Executes forced failover in an existing failover group. |
> | Action | Microsoft.Sql/servers/failoverGroups/read | Returns the list of failover groups or gets the properties for the specified failover group. |
> | Action | Microsoft.Sql/servers/failoverGroups/write | Creates a failover group with the specified parameters or updates the properties or tags for the specified failover group. |
> | Action | Microsoft.Sql/servers/firewallRules/delete | Deletes an existing server firewall rule. |
> | Action | Microsoft.Sql/servers/firewallRules/read | Return the list of server firewall rules or gets the properties for the specified server firewall rule. |
> | Action | Microsoft.Sql/servers/firewallRules/write | Creates a server firewall rule with the specified parameters, update the properties for the specified rule or overwrite all existing rules with new server firewall rule(s). |
> | Action | Microsoft.Sql/servers/import/action | Create a new database on the server and deploy schema and data from a DacPac package |
> | Action | Microsoft.Sql/servers/importExportOperationResults/read | Gets in-progress import/export operations |
> | Action | Microsoft.Sql/servers/interfaceEndpointProfiles/delete | Deletes the specified interface endpoint profile |
> | Action | Microsoft.Sql/servers/interfaceEndpointProfiles/read | Returns the properties for the specified interface endpoint profile |
> | Action | Microsoft.Sql/servers/interfaceEndpointProfiles/write | Creates a interface endpoint profile with the specified parameters or updates the properties or tags for the specified interface endpoint |
> | Action | Microsoft.Sql/servers/jobAgents/delete | Deletes an Azure SQL DB job agent |
> | Action | Microsoft.Sql/servers/jobAgents/read | Gets an Azure SQL DB job agent |
> | Action | Microsoft.Sql/servers/jobAgents/write | Creates or updates an Azure SQL DB job agent |
> | Action | Microsoft.Sql/servers/keys/delete | Deletes an existing server key. |
> | Action | Microsoft.Sql/servers/keys/read | Return the list of server keys or gets the properties for the specified server key. |
> | Action | Microsoft.Sql/servers/keys/write | Creates a key with the specified parameters or update the properties or tags for the specified server key. |
> | Action | Microsoft.Sql/servers/operationResults/read | Gets in-progress server operations |
> | Action | Microsoft.Sql/servers/providers/Microsoft.Insights/metricDefinitions/read | Return types of metrics that are available for servers |
> | Action | Microsoft.Sql/servers/read | Return the list of servers or gets the properties for the specified server. |
> | Action | Microsoft.Sql/servers/recommendedElasticPools/databases/read | Retrieve metrics for recommended elastic database pools for a given server |
> | Action | Microsoft.Sql/servers/recommendedElasticPools/read | Retrieve recommendation for elastic database pools to reduce cost or improve performance based on historica resource utilization |
> | Action | Microsoft.Sql/servers/recoverableDatabases/read | This operation is used for disaster recovery of live database to restore database to last-known good backup point. It returns information about the last good backup but it doesn\u0027t actually restore the database. |
> | Action | Microsoft.Sql/servers/replicationLinks/read | Return the list of replication links or gets the properties for the specified replication links. |
> | Action | Microsoft.Sql/servers/restorableDroppedDatabases/read | Get a list of databases that were dropped on a given server that are still within retention policy. |
> | Action | Microsoft.Sql/servers/securityAlertPolicies/operationResults/read | Retrieve results of the server threat detection policy write operation |
> | Action | Microsoft.Sql/servers/securityAlertPolicies/read | Retrieve details of the server threat detection policy configured on a given server |
> | Action | Microsoft.Sql/servers/securityAlertPolicies/write | Change the server threat detection policy for a given server |
> | Action | Microsoft.Sql/servers/serviceObjectives/read | Retrieve list of service level objectives (also known as performance tiers) available on a given server |
> | Action | Microsoft.Sql/servers/syncAgents/delete | Deletes an existing sync agent. |
> | Action | Microsoft.Sql/servers/syncAgents/generateKey/action | Generate sync agent registeration key |
> | Action | Microsoft.Sql/servers/syncAgents/linkedDatabases/read | Return the list of sync agent linked databases |
> | Action | Microsoft.Sql/servers/syncAgents/read | Return the list of sync agents or gets the properties for the specified sync agent. |
> | Action | Microsoft.Sql/servers/syncAgents/write | Creates a sync agent with the specified parameters or update the properties for the specified sync agent. |
> | Action | Microsoft.Sql/servers/tdeCertificates/action | Create/Update TDE certificate |
> | Action | Microsoft.Sql/servers/usages/read | Return server DTU quota and current DTU consuption by all databases within the server |
> | Action | Microsoft.Sql/servers/virtualNetworkRules/delete | Deletes an existing Virtual Network Rule |
> | Action | Microsoft.Sql/servers/virtualNetworkRules/read | Return the list of virtual network rules or gets the properties for the specified virtual network rule. |
> | Action | Microsoft.Sql/servers/virtualNetworkRules/write | Creates a virtual network rule with the specified parameters or update the properties or tags for the specified virtual network rule. |
> | Action | Microsoft.Sql/servers/vulnerabilityAssessments/delete | Remove the vulnerability assessment for a given server |
> | Action | Microsoft.Sql/servers/vulnerabilityAssessments/read | Retrieve details of the vulnerability assessment configured on a given server |
> | Action | Microsoft.Sql/servers/vulnerabilityAssessments/write | Change the vulnerability assessment for a given server |
> | Action | Microsoft.Sql/servers/write | Creates a server with the specified parameters or update the properties or tags for the specified server. |
> | Action | Microsoft.Sql/unregister/action | UnRegisters the subscription for the Microsoft SQL Database resource provider and enables the creation of Microsoft SQL Databases. |
> | Action | Microsoft.Sql/virtualClusters/read | Return the list of virtual clusters or gets the properties for the specified virtual cluster. |
> | Action | Microsoft.Sql/virtualClusters/write | Updates virtual cluster tags. |

## Microsoft.Storage

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Storage/checknameavailability/read | Checks that account name is valid and is not in use. |
> | Action | Microsoft.Storage/locations/deleteVirtualNetworkOrSubnets/action | Notifies Microsoft.Storage that virtual network or subnet is being deleted |
> | Action | Microsoft.Storage/locations/usages/read | Returns the limit and the current usage count for resources in the specified subscription |
> | Action | Microsoft.Storage/operations/read | Polls the status of an asynchronous operation. |
> | Action | Microsoft.Storage/register/action | Registers the subscription for the storage resource provider and enables the creation of storage accounts. |
> | Action | Microsoft.Storage/skus/read | Lists the Skus supported by Microsoft.Storage. |
> | DataAction | Microsoft.Storage/storageAccounts/blobServices/containers/blobs/add/action | Returns the result of adding blob content |
> | DataAction | Microsoft.Storage/storageAccounts/blobServices/containers/blobs/delete | Returns the result of deleting a blob |
> | DataAction | Microsoft.Storage/storageAccounts/blobServices/containers/blobs/deleteAutomaticSnapshot/action | Returns the result of deleting an automatic snapshot |
> | DataAction | Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read | Returns a blob or a list of blobs |
> | DataAction | Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write | Returns the result of writing a blob |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/clearLegalHold/action | Clear blob container legal hold |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/delete | Returns the result of deleting a container |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/immutabilityPolicies/delete | Delete blob container immutability policy |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/immutabilityPolicies/extend/action | Extend blob container immutability policy |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/immutabilityPolicies/lock/action | Lock blob container immutability policy |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/immutabilityPolicies/read | Get blob container immutability policy |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/immutabilityPolicies/write | Put blob container immutability policy |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/read | Returns a container or a list of containers |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/setLegalHold/action | Set blob container legal hold |
> | Action | Microsoft.Storage/storageAccounts/blobServices/containers/write | Returns the result of put or lease blob container |
> | Action | Microsoft.Storage/storageAccounts/blobServices/generateUserDelegationKey/action | Returns a user delegation key for the blob service |
> | Action | Microsoft.Storage/storageAccounts/blobServices/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/blobServices/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/blobServices/providers/Microsoft.Insights/logDefinitions/read | Gets the log definition for Blob |
> | Action | Microsoft.Storage/storageAccounts/blobServices/providers/Microsoft.Insights/metricDefinitions/read | Get list of Microsoft Storage Metrics definitions. |
> | Action | Microsoft.Storage/storageAccounts/blobServices/read | Returns blob service properties or statistics |
> | Action | Microsoft.Storage/storageAccounts/blobServices/write | Returns the result of put blob service properties |
> | Action | Microsoft.Storage/storageAccounts/delete | Deletes an existing storage account. |
> | Action | Microsoft.Storage/storageAccounts/fileServices/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/fileServices/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/fileServices/providers/Microsoft.Insights/logDefinitions/read | Gets the log definition for File |
> | Action | Microsoft.Storage/storageAccounts/fileServices/providers/Microsoft.Insights/metricDefinitions/read | Get list of Microsoft Storage Metrics definitions. |
> | Action | Microsoft.Storage/storageAccounts/lastsynctime/read | Returns storage account's last sync time |
> | Action | Microsoft.Storage/storageAccounts/listAccountSas/action | Returns the Account SAS token for the specified storage account. |
> | Action | Microsoft.Storage/storageAccounts/listkeys/action | Returns the access keys for the specified storage account. |
> | Action | Microsoft.Storage/storageAccounts/listServiceSas/action | Returns the Service SAS token for the specified storage account. |
> | Action | Microsoft.Storage/storageAccounts/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/providers/Microsoft.Insights/metricDefinitions/read | Get list of Microsoft Storage Metrics definitions. |
> | Action | Microsoft.Storage/storageAccounts/queueServices/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/queueServices/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/queueServices/providers/Microsoft.Insights/logDefinitions/read | Gets the log definition for Queue |
> | Action | Microsoft.Storage/storageAccounts/queueServices/providers/Microsoft.Insights/metricDefinitions/read | Get list of Microsoft Storage Metrics definitions. |
> | Action | Microsoft.Storage/storageAccounts/queueServices/queues/delete | Returns the result of deleting a queue |
> | DataAction | Microsoft.Storage/storageAccounts/queueServices/queues/messages/add/action | Returns the result of adding a message |
> | DataAction | Microsoft.Storage/storageAccounts/queueServices/queues/messages/delete | Returns the result of deleting a message |
> | DataAction | Microsoft.Storage/storageAccounts/queueServices/queues/messages/process/action | Returns the result of processing a message |
> | DataAction | Microsoft.Storage/storageAccounts/queueServices/queues/messages/read | Returns a message |
> | DataAction | Microsoft.Storage/storageAccounts/queueServices/queues/messages/write | Returns the result of writing a message |
> | Action | Microsoft.Storage/storageAccounts/queueServices/queues/read | Returns a queue or a list of queues. |
> | Action | Microsoft.Storage/storageAccounts/queueServices/queues/write | Returns the result of writing a queue |
> | Action | Microsoft.Storage/storageAccounts/queueServices/read | Returns queue service properties or statistics. |
> | Action | Microsoft.Storage/storageAccounts/queueServices/write | Returns the result of setting queue service properties |
> | Action | Microsoft.Storage/storageAccounts/read | Returns the list of storage accounts or gets the properties for the specified storage account. |
> | Action | Microsoft.Storage/storageAccounts/regeneratekey/action | Regenerates the access keys for the specified storage account. |
> | Action | Microsoft.Storage/storageAccounts/revokeUserDelegationKeys/action | Revokes all the user delegation keys for the specified storage account. |
> | Action | Microsoft.Storage/storageAccounts/services/diagnosticSettings/write | Create/Update storage account diagnostic settings. |
> | Action | Microsoft.Storage/storageAccounts/tableServices/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/tableServices/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource. |
> | Action | Microsoft.Storage/storageAccounts/tableServices/providers/Microsoft.Insights/logDefinitions/read | Gets the log definition for Table |
> | Action | Microsoft.Storage/storageAccounts/tableServices/providers/Microsoft.Insights/metricDefinitions/read | Get list of Microsoft Storage Metrics definitions. |
> | Action | Microsoft.Storage/storageAccounts/write | Creates a storage account with the specified parameters or update the properties or tags or adds custom domain for the specified storage account. |
> | Action | Microsoft.Storage/usages/read | Returns the limit and the current usage count for resources in the specified subscription |

## Microsoft.StorageSync

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | microsoft.storagesync/locations/checkNameAvailability/action | Checks that storage sync service name is valid and is not in use. |
> | Action | microsoft.storagesync/locations/workflows/operations/read | Gets the status of an asynchronous operation |
> | Action | microsoft.storagesync/storageSyncServices/delete | Delete any Storage Sync Services |
> | Action | microsoft.storagesync/storageSyncServices/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Storage Sync Services |
> | Action | microsoft.storagesync/storageSyncServices/read | Read any Storage Sync Services |
> | Action | microsoft.storagesync/storageSyncServices/registeredServers/delete | Delete any Registered Server |
> | Action | microsoft.storagesync/storageSyncServices/registeredServers/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Registered Server |
> | Action | microsoft.storagesync/storageSyncServices/registeredServers/read | Read any Registered Server |
> | Action | microsoft.storagesync/storageSyncServices/registeredServers/write | Create or Update any Registered Server |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/delete | Delete any Cloud Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/operationresults/read | Gets the status of an asynchronous backup/restore operation |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/postbackup/action | Call this action after backup |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/postrestore/action | Call this action after restore |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/prebackup/action | Call this action before backup |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/prerestore/action | Call this action before restore |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/read | Read any Cloud Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/restoreheartbeat/action | Restore heartbeat |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/cloudEndpoints/write | Create or Update any Cloud Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/delete | Delete any Sync Groups |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Sync Groups |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/read | Read any Sync Groups |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/serverEndpoints/delete | Delete any Server Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/serverEndpoints/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for Server Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/serverEndpoints/read | Read any Server Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/serverEndpoints/recallAction/action | Call this action to recall files to a server |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/serverEndpoints/write | Create or Update any Server Endpoints |
> | Action | microsoft.storagesync/storageSyncServices/syncGroups/write | Create or Update any Sync Groups |
> | Action | microsoft.storagesync/storageSyncServices/workflows/operationresults/read | Gets the status of an asynchronous operation |
> | Action | microsoft.storagesync/storageSyncServices/workflows/operations/read | Gets the status of an asynchronous operation |
> | Action | microsoft.storagesync/storageSyncServices/workflows/read | Read Workflows |
> | Action | microsoft.storagesync/storageSyncServices/write | Create or Update any Storage Sync Services |

## Microsoft.StorSimple

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.StorSimple/managers/accessControlRecords/delete | Deletes the Access Control Records |
> | Action | Microsoft.StorSimple/managers/accessControlRecords/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/accessControlRecords/read | Lists or gets the Access Control Records |
> | Action | Microsoft.StorSimple/managers/accessControlRecords/write | Create or update the Access Control Records |
> | Action | Microsoft.StorSimple/managers/alerts/read | Lists or gets the Alerts |
> | Action | Microsoft.StorSimple/managers/backups/read | Lists or gets the Backup Set |
> | Action | Microsoft.StorSimple/managers/bandwidthSettings/delete | Deletes an existing Bandwidth Settings (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/bandwidthSettings/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/bandwidthSettings/read | List the Bandwidth Settings (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/bandwidthSettings/write | Creates a new or updates Bandwidth Settings (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/certificates/write | Create or update the Certificates |
> | Action | Microsoft.StorSimple/Managers/certificates/write | The Update Resource Certificate operation updates the resource/vault credential certificate. |
> | Action | Microsoft.StorSimple/managers/clearAlerts/action | Clear all the alerts associated with the device manager. |
> | Action | Microsoft.StorSimple/managers/cloudApplianceConfigurations/read | List the Cloud Appliance Supported Configurations |
> | Action | Microsoft.StorSimple/managers/configureDevice/action | Configures a device |
> | Action | Microsoft.StorSimple/managers/delete | Deletes the Device Managers |
> | Action | Microsoft.StorSimple/Managers/delete | The Delete Vault operation deletes the specified Azure resource of type 'vault' |
> | Action | Microsoft.StorSimple/managers/devices/alertSettings/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/alertSettings/read | Lists or gets the Alert Settings |
> | Action | Microsoft.StorSimple/managers/devices/alertSettings/write | Create or update the Alert Settings |
> | Action | Microsoft.StorSimple/managers/devices/authorizeForServiceEncryptionKeyRollover/action | Authorize for Service Encryption Key Rollover of Devices |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/backup/action | Take a manual backup to create an on-demand backup of all the volumes protected by the policy. |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/delete | Deletes an existing Backup Polices (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/read | List the Backup Polices (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/schedules/delete | Deletes an existing Schedules |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/schedules/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/schedules/read | List the Schedules |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/schedules/write | Creates a new or updates Schedules |
> | Action | Microsoft.StorSimple/managers/devices/backupPolicies/write | Creates a new or updates Backup Polices (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/devices/backups/delete | Deletes the Backup Set |
> | Action | Microsoft.StorSimple/managers/devices/backups/elements/clone/action | Clone a share or volume using a backup element. |
> | Action | Microsoft.StorSimple/managers/devices/backups/elements/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/backups/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/backups/read | Lists or gets the Backup Set |
> | Action | Microsoft.StorSimple/managers/devices/backups/restore/action | Restore all the volumes from a backup set. |
> | Action | Microsoft.StorSimple/managers/devices/backupScheduleGroups/delete | Deletes the Backup Schedule Groups |
> | Action | Microsoft.StorSimple/managers/devices/backupScheduleGroups/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/backupScheduleGroups/read | Lists or gets the Backup Schedule Groups |
> | Action | Microsoft.StorSimple/managers/devices/backupScheduleGroups/write | Create or update the Backup Schedule Groups |
> | Action | Microsoft.StorSimple/managers/devices/chapSettings/delete | Deletes the Chap Settings |
> | Action | Microsoft.StorSimple/managers/devices/chapSettings/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/chapSettings/read | Lists or gets the Chap Settings |
> | Action | Microsoft.StorSimple/managers/devices/chapSettings/write | Create or update the Chap Settings |
> | Action | Microsoft.StorSimple/managers/devices/deactivate/action | Deactivates a device. |
> | Action | Microsoft.StorSimple/managers/devices/delete | Deletes the Devices |
> | Action | Microsoft.StorSimple/managers/devices/disks/read | Lists or gets the Disks |
> | Action | Microsoft.StorSimple/managers/devices/download/action | Dowload updates for a device. |
> | Action | Microsoft.StorSimple/managers/devices/failover/action | Failover of the device. |
> | Action | Microsoft.StorSimple/managers/devices/failover/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/failoverTargets/read | Lists or gets the Failover targets of the devices |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/backup/action | Take backup of an File Server. |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/delete | Deletes the File Servers |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/metrics/read | Lists or gets the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/metricsDefinitions/read | Lists or gets the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/read | Lists or gets the File Servers |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/shares/delete | Deletes the Shares |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/shares/metrics/read | Lists or gets the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/shares/metricsDefinitions/read | Lists or gets the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/shares/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/shares/read | Lists or gets the Shares |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/shares/write | Create or update the Shares |
> | Action | Microsoft.StorSimple/managers/devices/fileservers/write | Create or update the File Servers |
> | Action | Microsoft.StorSimple/managers/devices/hardwareComponentGroups/changeControllerPowerState/action | Change controller power state of hardware component groups |
> | Action | Microsoft.StorSimple/managers/devices/hardwareComponentGroups/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/hardwareComponentGroups/read | List the Hardware Component Groups |
> | Action | Microsoft.StorSimple/managers/devices/install/action | Install updates on a device. |
> | Action | Microsoft.StorSimple/managers/devices/installUpdates/action | Installs updates on the devices (8000 Series Only). |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/backup/action | Take backup of an iSCSI server. |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/delete | Deletes the iSCSI Servers |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/disks/delete | Deletes the Disks |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/disks/metrics/read | Lists or gets the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/disks/metricsDefinitions/read | Lists or gets the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/disks/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/disks/read | Lists or gets the Disks |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/disks/write | Create or update the Disks |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/metrics/read | Lists or gets the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/metricsDefinitions/read | Lists or gets the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/read | Lists or gets the iSCSI Servers |
> | Action | Microsoft.StorSimple/managers/devices/iscsiservers/write | Create or update the iSCSI Servers |
> | Action | Microsoft.StorSimple/managers/devices/jobs/cancel/action | Cancel a running job |
> | Action | Microsoft.StorSimple/managers/devices/jobs/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/jobs/read | Lists or gets the Jobs |
> | Action | Microsoft.StorSimple/managers/devices/listFailoverSets/action | List the failover sets for an existing device (8000 Series Only). |
> | Action | Microsoft.StorSimple/managers/devices/listFailoverTargets/action | List failover targets of the devices (8000 Series Only). |
> | Action | Microsoft.StorSimple/managers/devices/metrics/read | Lists or gets the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/metricsDefinitions/read | Lists or gets the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/confirmMigration/action | Confirms a successful migration and commit it. |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/confirmMigrationStatus/read | List the Confirm Migration Status |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/fetchConfirmMigrationStatus/action | Fetch the confirm status of migration. |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/fetchMigrationEstimate/action | Fetch the status for the migration estimation job. |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/fetchMigrationStatus/action | Fetch the status for the migration. |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/import/action | Import source configurations for migration |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/migrationEstimate/read | List the Migration Estimate |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/migrationStatus/read | List the Migration Status |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/startMigration/action | Start migration using source configurations |
> | Action | Microsoft.StorSimple/managers/devices/migrationSourceConfigurations/startMigrationEstimate/action | Start a job to estimate the duration of the migration process. |
> | Action | Microsoft.StorSimple/managers/devices/networkSettings/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/networkSettings/read | Lists or gets the Network Settings |
> | Action | Microsoft.StorSimple/managers/devices/networkSettings/write | Creates a new or updates Network Settings |
> | Action | Microsoft.StorSimple/managers/devices/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/publicEncryptionKey/action | List public encryption key of the device manager |
> | Action | Microsoft.StorSimple/managers/devices/publishSupportPackage/action | Publish support package of a device for Microsoft Support troubleshooting. |
> | Action | Microsoft.StorSimple/managers/devices/read | Lists or gets the Devices |
> | Action | Microsoft.StorSimple/managers/devices/scanForUpdates/action | Scan for updates in a device. |
> | Action | Microsoft.StorSimple/managers/devices/securitySettings/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/securitySettings/read | List the Security Settings |
> | Action | Microsoft.StorSimple/managers/devices/securitySettings/syncRemoteManagementCertificate/action | Synchronize the remote management certificate for a device. |
> | Action | Microsoft.StorSimple/managers/devices/securitySettings/update/action | Update the security settings. |
> | Action | Microsoft.StorSimple/managers/devices/securitySettings/write | Creates a new or updates Security Settings |
> | Action | Microsoft.StorSimple/managers/devices/sendTestAlertEmail/action | Send test alert email to configured email recipients. |
> | Action | Microsoft.StorSimple/managers/devices/shares/read | Lists or gets the Shares |
> | Action | Microsoft.StorSimple/managers/devices/timeSettings/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/timeSettings/read | Lists or gets the Time Settings |
> | Action | Microsoft.StorSimple/managers/devices/timeSettings/write | Creates a new or updates Time Settings |
> | Action | Microsoft.StorSimple/managers/devices/updates/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/updateSummary/read | Lists or gets the Update Summary |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/delete | Deletes an existing Volume Containers (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/metrics/read | List the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/metricsDefinitions/read | List the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/read | List the Volume Containers (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/volumes/delete | Deletes an existing Volumes |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/volumes/metrics/read | List the Metrics |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/volumes/metricsDefinitions/read | List the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/volumes/operationResults/read | List the Operation Results |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/volumes/read | List the Volumes |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/volumes/write | Creates a new or updates Volumes |
> | Action | Microsoft.StorSimple/managers/devices/volumeContainers/write | Creates a new or updates Volume Containers (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/devices/volumes/read | List the Volumes |
> | Action | Microsoft.StorSimple/managers/devices/write | Create or update the Devices |
> | Action | Microsoft.StorSimple/managers/encryptionSettings/read | Lists or gets the Encryption Settings |
> | Action | Microsoft.StorSimple/managers/extendedInformation/delete | Deletes the Extended Vault Information |
> | Action | Microsoft.StorSimple/Managers/extendedInformation/delete | The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault? |
> | Action | Microsoft.StorSimple/managers/extendedInformation/read | Lists or gets the Extended Vault Information |
> | Action | Microsoft.StorSimple/Managers/extendedInformation/read | The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault? |
> | Action | Microsoft.StorSimple/managers/extendedInformation/write | Create or update the Extended Vault Information |
> | Action | Microsoft.StorSimple/Managers/extendedInformation/write | The Get Extended Info operation gets an object's Extended Info representing the Azure resource of type ?vault? |
> | Action | Microsoft.StorSimple/managers/features/read | List the Features |
> | Action | Microsoft.StorSimple/managers/fileservers/read | Lists or gets the File Servers |
> | Action | Microsoft.StorSimple/managers/getActivationKey/action | Get activation key for the device manager. |
> | Action | Microsoft.StorSimple/managers/getEncryptionKey/action | Get encryption key for the device manager. |
> | Action | Microsoft.StorSimple/managers/iscsiservers/read | Lists or gets the iSCSI Servers |
> | Action | Microsoft.StorSimple/managers/jobs/read | Lists or gets the Jobs |
> | Action | Microsoft.StorSimple/managers/listActivationKey/action | Gets the activation key of the StorSimple Device Manager. |
> | Action | Microsoft.StorSimple/managers/listPublicEncryptionKey/action | List public encryption keys of a StorSimple Device Manager. |
> | Action | Microsoft.StorSimple/managers/metrics/read | Lists or gets the Metrics |
> | Action | Microsoft.StorSimple/managers/metricsDefinitions/read | Lists or gets the Metrics Definitions |
> | Action | Microsoft.StorSimple/managers/migrateClassicToResourceManager/action | Migrate Classic To Resource Manager of Mangers |
> | Action | Microsoft.StorSimple/managers/migrationSourceConfigurations/read | List the Migration Source Configurations (8000 Series Only) |
> | Action | Microsoft.StorSimple/managers/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/provisionCloudAppliance/action | Create a new cloud appliance. |
> | Action | Microsoft.StorSimple/managers/read | Lists or gets the Device Managers |
> | Action | Microsoft.StorSimple/Managers/read | The Get Vault operation gets an object representing the Azure resource of type 'vault' |
> | Action | Microsoft.StorSimple/managers/regenarateRegistationCertificate/action | Regenerate registration certificate for the device managers. |
> | Action | Microsoft.StorSimple/managers/regenerateActivationKey/action | Regenerate activation key for the device manager. |
> | Action | Microsoft.StorSimple/managers/storageAccountCredentials/delete | Deletes the Storage Account Credentials |
> | Action | Microsoft.StorSimple/managers/storageAccountCredentials/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/storageAccountCredentials/read | Lists or gets the Storage Account Credentials |
> | Action | Microsoft.StorSimple/managers/storageAccountCredentials/write | Create or update the Storage Account Credentials |
> | Action | Microsoft.StorSimple/managers/storageDomains/delete | Deletes the Storage Domains |
> | Action | Microsoft.StorSimple/managers/storageDomains/operationResults/read | Lists or gets the Operation Results |
> | Action | Microsoft.StorSimple/managers/storageDomains/read | Lists or gets the Storage Domains |
> | Action | Microsoft.StorSimple/managers/storageDomains/write | Create or update the Storage Domains |
> | Action | Microsoft.StorSimple/managers/write | Create or update the Device Managers |
> | Action | Microsoft.StorSimple/Managers/write | Create Vault operation creates an Azure resource of type 'vault' |
> | Action | Microsoft.StorSimple/operations/read | Lists or gets the Operations |
> | Action | Microsoft.StorSimple/register/action | Register Provider Microsoft.StorSimple |

## Microsoft.StreamAnalytics

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.StreamAnalytics/locations/quotas/Read | Read Stream Analytics Subscription Quota |
> | Action | Microsoft.StreamAnalytics/operations/Read | Read Stream Analytics Operations |
> | Action | Microsoft.StreamAnalytics/Register/action | Register subscription with Stream Analytics Resource Provider |
> | Action | Microsoft.StreamAnalytics/streamingjobs/Delete | Delete Stream Analytics Job |
> | Action | Microsoft.StreamAnalytics/streamingjobs/functions/Delete | Delete Stream Analytics Job Function |
> | Action | Microsoft.StreamAnalytics/streamingjobs/functions/operationresults/Read | Read operation results for Stream Analytics Job Function |
> | Action | Microsoft.StreamAnalytics/streamingjobs/functions/Read | Read Stream Analytics Job Function |
> | Action | Microsoft.StreamAnalytics/streamingjobs/functions/RetrieveDefaultDefinition/action | Retrieve Default Definition of a Stream Analytics Job Function |
> | Action | Microsoft.StreamAnalytics/streamingjobs/functions/Test/action | Test Stream Analytics Job Function |
> | Action | Microsoft.StreamAnalytics/streamingjobs/functions/Write | Write Stream Analytics Job Function |
> | Action | Microsoft.StreamAnalytics/streamingjobs/inputs/Delete | Delete Stream Analytics Job Input |
> | Action | Microsoft.StreamAnalytics/streamingjobs/inputs/operationresults/Read | Read operation results for Stream Analytics Job Input |
> | Action | Microsoft.StreamAnalytics/streamingjobs/inputs/Read | Read Stream Analytics Job Input |
> | Action | Microsoft.StreamAnalytics/streamingjobs/inputs/Sample/action | Sample Stream Analytics Job Input |
> | Action | Microsoft.StreamAnalytics/streamingjobs/inputs/Test/action | Test Stream Analytics Job Input |
> | Action | Microsoft.StreamAnalytics/streamingjobs/inputs/Write | Write Stream Analytics Job Input |
> | Action | Microsoft.StreamAnalytics/streamingjobs/metricdefinitions/Read | Read Metric Definitions |
> | Action | Microsoft.StreamAnalytics/streamingjobs/operationresults/Read | Read operation results for Stream Analytics Job |
> | Action | Microsoft.StreamAnalytics/streamingjobs/outputs/Delete | Delete Stream Analytics Job Output |
> | Action | Microsoft.StreamAnalytics/streamingjobs/outputs/operationresults/Read | Read operation results for Stream Analytics Job Output |
> | Action | Microsoft.StreamAnalytics/streamingjobs/outputs/Read | Read Stream Analytics Job Output |
> | Action | Microsoft.StreamAnalytics/streamingjobs/outputs/Test/action | Test Stream Analytics Job Output |
> | Action | Microsoft.StreamAnalytics/streamingjobs/outputs/Write | Write Stream Analytics Job Output |
> | Action | Microsoft.StreamAnalytics/streamingjobs/providers/Microsoft.Insights/diagnosticSettings/read | Read diagnostic setting. |
> | Action | Microsoft.StreamAnalytics/streamingjobs/providers/Microsoft.Insights/diagnosticSettings/write | Write diagnostic setting. |
> | Action | Microsoft.StreamAnalytics/streamingjobs/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for streamingjobs |
> | Action | Microsoft.StreamAnalytics/streamingjobs/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for streamingjobs |
> | Action | Microsoft.StreamAnalytics/streamingjobs/Read | Read Stream Analytics Job |
> | Action | Microsoft.StreamAnalytics/streamingjobs/Start/action | Start Stream Analytics Job |
> | Action | Microsoft.StreamAnalytics/streamingjobs/Stop/action | Stop Stream Analytics Job |
> | Action | Microsoft.StreamAnalytics/streamingjobs/transformations/Delete | Delete Stream Analytics Job Transformation |
> | Action | Microsoft.StreamAnalytics/streamingjobs/transformations/Read | Read Stream Analytics Job Transformation |
> | Action | Microsoft.StreamAnalytics/streamingjobs/transformations/Write | Write Stream Analytics Job Transformation |
> | Action | Microsoft.StreamAnalytics/streamingjobs/Write | Write Stream Analytics Job |

## Microsoft.Subscription

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Subscription/CreateSubscription/action | Create an Azure subscription |
> | Action | Microsoft.Subscription/SubscriptionDefinitions/read | Get an Azure subscription definition within a management group. |
> | Action | Microsoft.Subscription/SubscriptionDefinitions/write | Create an Azure subscription definition |

## Microsoft.Support

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.Support/register/action | Registers to Support Resource Provider |
> | Action | Microsoft.Support/supportTickets/read | Gets Support Ticket details (including status, severity, contact details and communications) or gets the list of Support Tickets across subscriptions. |
> | Action | Microsoft.Support/supportTickets/write | Creates or Updates a Support Ticket. You can create a Support Ticket for Technical, Billing, Quotas or Subscription Management related issues. You can update severity, contact details and communications for existing support tickets. |

## Microsoft.TimeSeriesInsights

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.TimeSeriesInsights/environments/accesspolicies/delete | Deletes the access policy. |
> | Action | Microsoft.TimeSeriesInsights/environments/accesspolicies/read | Get the properties of an access policy. |
> | Action | Microsoft.TimeSeriesInsights/environments/accesspolicies/write | Creates a new access policy for an environment, or updates an existing access policy. |
> | Action | Microsoft.TimeSeriesInsights/environments/delete | Deletes the environment. |
> | Action | Microsoft.TimeSeriesInsights/environments/eventsources/delete | Deletes the event source. |
> | Action | Microsoft.TimeSeriesInsights/environments/eventsources/eventsources/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.TimeSeriesInsights/environments/eventsources/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.TimeSeriesInsights/environments/eventsources/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for eventsources |
> | Action | Microsoft.TimeSeriesInsights/environments/eventsources/read | Get the properties of an event source. |
> | Action | Microsoft.TimeSeriesInsights/environments/eventsources/write | Creates a new event source for an environment, or updates an existing event source. |
> | Action | Microsoft.TimeSeriesInsights/environments/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | Microsoft.TimeSeriesInsights/environments/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.TimeSeriesInsights/environments/providers/Microsoft.Insights/metricDefinitions/read | Gets the available metrics for environments |
> | Action | Microsoft.TimeSeriesInsights/environments/read | Get the properties of an environment. |
> | Action | Microsoft.TimeSeriesInsights/environments/referencedatasets/delete | Deletes the reference data set. |
> | Action | Microsoft.TimeSeriesInsights/environments/referencedatasets/read | Get the properties of a reference data set. |
> | Action | Microsoft.TimeSeriesInsights/environments/referencedatasets/write | Creates a new reference data set for an environment, or updates an existing reference data set. |
> | Action | Microsoft.TimeSeriesInsights/environments/status/read | Get the status of the environment, state of its associated operations like ingress. |
> | Action | Microsoft.TimeSeriesInsights/environments/write | Creates a new environment, or updates an existing environment. |
> | Action | Microsoft.TimeSeriesInsights/register/action | Registers the subscription for the Time Series Insights resource provider and enables the creation of Time Series Insights environments. |

## Microsoft.VisualStudio

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.VisualStudio/Account/Delete | Delete Account |
> | Action | Microsoft.VisualStudio/Account/Extension/Read | Read Account/Extension |
> | Action | Microsoft.VisualStudio/Account/Project/Read | Read Account/Project |
> | Action | Microsoft.VisualStudio/Account/Project/Write | Set Account/Project |
> | Action | Microsoft.VisualStudio/Account/Read | Read Account |
> | Action | Microsoft.VisualStudio/Account/Write | Set Account |
> | Action | Microsoft.VisualStudio/Extension/Delete | Delete Extension |
> | Action | Microsoft.VisualStudio/Extension/Read | Read Extension |
> | Action | Microsoft.VisualStudio/Extension/Write | Set Extension |
> | Action | Microsoft.VisualStudio/Project/Delete | Delete Project |
> | Action | Microsoft.VisualStudio/Project/Read | Read Project |
> | Action | Microsoft.VisualStudio/Project/Write | Set Project |
> | Action | Microsoft.VisualStudio/Register/Action | Register Azure Subscription with Microsoft.VisualStudio provider |

## microsoft.web

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | microsoft.web/apimanagementaccounts/apiacls/read | Get Api Management Accounts Apiacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/apiacls/delete | Delete Api Management Accounts APIs Apiacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/apiacls/read | Get Api Management Accounts APIs Apiacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/apiacls/write | Update Api Management Accounts APIs Apiacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/connectionacls/read | Get Api Management Accounts APIs Connectionacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/confirmconsentcode/action | Confirm Consent Code Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/connectionacls/delete | Delete Api Management Accounts APIs Connections Connectionacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/connectionacls/read | Get Api Management Accounts APIs Connections Connectionacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/connectionacls/write | Update Api Management Accounts APIs Connections Connectionacls. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/delete | Delete Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/getconsentlinks/action | Get Consent Links for Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/listconnectionkeys/action | List Connection Keys Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/listsecrets/action | List Secrets Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/read | Get Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/connections/write | Update Api Management Accounts APIs Connections. |
> | Action | microsoft.web/apimanagementaccounts/apis/delete | Delete Api Management Accounts APIs. |
> | Action | microsoft.web/apimanagementaccounts/apis/localizeddefinitions/delete | Delete Api Management Accounts APIs Localized Definitions. |
> | Action | microsoft.web/apimanagementaccounts/apis/localizeddefinitions/read | Get Api Management Accounts APIs Localized Definitions. |
> | Action | microsoft.web/apimanagementaccounts/apis/localizeddefinitions/write | Update Api Management Accounts APIs Localized Definitions. |
> | Action | microsoft.web/apimanagementaccounts/apis/read | Get Api Management Accounts APIs. |
> | Action | microsoft.web/apimanagementaccounts/apis/write | Update Api Management Accounts APIs. |
> | Action | microsoft.web/apimanagementaccounts/connectionacls/read | Get Api Management Accounts Connectionacls. |
> | Action | microsoft.web/availablestacks/read | Get Available Stacks. |
> | Action | microsoft.web/billingmeters/read | Get list of billing meters. |
> | Action | Microsoft.Web/certificates/Delete | Delete an existing certificate. |
> | Action | Microsoft.Web/certificates/Read | Get the list of certificates. |
> | Action | Microsoft.Web/certificates/Write | Add a new certificate or update an existing one. |
> | Action | microsoft.web/checknameavailability/read | Check if resource name is available. |
> | Action | microsoft.web/classicmobileservices/read | Get Classic Mobile Services. |
> | Action | Microsoft.Web/connectionGateways/Delete | Deletes a Connection Gateway. |
> | Action | Microsoft.Web/connectionGateways/Join/Action | Joins a Connection Gateway. |
> | Action | Microsoft.Web/connectionGateways/ListStatus/Action | Lists status of a Connection Gateway. |
> | Action | Microsoft.Web/connectionGateways/Move/Action | Moves a Connection Gateway. |
> | Action | Microsoft.Web/connectionGateways/Read | Get the list of Connection Gateways. |
> | Action | Microsoft.Web/connectionGateways/Write | Creates or updates a Connection Gateway. |
> | Action | microsoft.web/connections/confirmconsentcode/action | Confirm Connections Consent Code. |
> | Action | Microsoft.Web/connections/Delete | Deletes a Connection. |
> | Action | Microsoft.Web/connections/Join/Action | Joins a Connection. |
> | Action | microsoft.web/connections/listconsentlinks/action | List Consent Links for Connections. |
> | Action | Microsoft.Web/connections/Move/Action | Moves a Connection. |
> | Action | Microsoft.Web/connections/Read | Get the list of Connections. |
> | Action | Microsoft.Web/connections/Write | Creates or updates a Connection. |
> | Action | Microsoft.Web/customApis/Delete | Deletes a Custom API. |
> | Action | Microsoft.Web/customApis/extractApiDefinitionFromWsdl/Action | Extracts API definition from a WSDL. |
> | Action | Microsoft.Web/customApis/Join/Action | Joins a Custom API. |
> | Action | Microsoft.Web/customApis/listWsdlInterfaces/Action | Lists WSDL interfaces for a Custom API. |
> | Action | Microsoft.Web/customApis/Move/Action | Moves a Custom API. |
> | Action | Microsoft.Web/customApis/Read | Get the list of Custom API. |
> | Action | Microsoft.Web/customApis/Write | Creates or updates a Custom API. |
> | Action | Microsoft.Web/deletedSites/Read | Get the properties of a Deleted Web App |
> | Action | microsoft.web/deploymentlocations/read | Get Deployment Locations. |
> | Action | Microsoft.Web/geoRegions/Read | Get the list of Geo regions. |
> | Action | microsoft.web/hostingenvironments/capacities/read | Get Hosting Environments Capacities. |
> | Action | Microsoft.Web/hostingEnvironments/Delete | Delete an App Service Environment |
> | Action | microsoft.web/hostingenvironments/detectors/read | Get Hosting Environments Detectors. |
> | Action | microsoft.web/hostingenvironments/diagnostics/read | Get Hosting Environments Diagnostics. |
> | Action | microsoft.web/hostingenvironments/inboundnetworkdependenciesendpoints/read | Get the network endpoints of all inbound dependencies. |
> | Action | microsoft.web/hostingenvironments/metricdefinitions/read | Get Hosting Environments Metric Definitions. |
> | Action | microsoft.web/hostingenvironments/multirolepools/metricdefinitions/read | Get Hosting Environments MultiRole Pools Metric Definitions. |
> | Action | microsoft.web/hostingenvironments/multirolepools/metrics/read | Get Hosting Environments MultiRole Pools Metrics. |
> | Action | Microsoft.Web/hostingEnvironments/multiRolePools/providers/Microsoft.Insights/metricDefinitions/Read | Gets the available metrics for App Service Environment MultiRole |
> | Action | Microsoft.Web/hostingEnvironments/multiRolePools/Read | Get the properties of a FrontEnd Pool in an App Service Environment |
> | Action | microsoft.web/hostingenvironments/multirolepools/skus/read | Get Hosting Environments MultiRole Pools SKUs. |
> | Action | microsoft.web/hostingenvironments/multirolepools/usages/read | Get Hosting Environments MultiRole Pools Usages. |
> | Action | Microsoft.Web/hostingEnvironments/multiRolePools/Write | Create a new FrontEnd Pool in an App Service Environment or update an existing one |
> | Action | microsoft.web/hostingenvironments/operations/read | Get Hosting Environments Operations. |
> | Action | microsoft.web/hostingenvironments/outboundnetworkdependenciesendpoints/read | Get the network endpoints of all outbound dependencies. |
> | Action | microsoft.web/hostingenvironments/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | microsoft.web/hostingenvironments/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Web/hostingEnvironments/Read | Get the properties of an App Service Environment |
> | Action | Microsoft.Web/hostingEnvironments/reboot/Action | Reboot all machines in an App Service Environment |
> | Action | microsoft.web/hostingenvironments/resume/action | Resume Hosting Environments. |
> | Action | microsoft.web/hostingenvironments/serverfarms/read | Get Hosting Environments App Service Plans. |
> | Action | microsoft.web/hostingenvironments/sites/read | Get Hosting Environments Web Apps. |
> | Action | microsoft.web/hostingenvironments/suspend/action | Suspend Hosting Environments. |
> | Action | microsoft.web/hostingenvironments/usages/read | Get Hosting Environments Usages. |
> | Action | microsoft.web/hostingenvironments/workerpools/metricdefinitions/read | Get Hosting Environments Workerpools Metric Definitions. |
> | Action | microsoft.web/hostingenvironments/workerpools/metrics/read | Get Hosting Environments Workerpools Metrics. |
> | Action | Microsoft.Web/hostingEnvironments/workerPools/providers/Microsoft.Insights/metricDefinitions/Read | Gets the available metrics for App Service Environment WorkerPool |
> | Action | Microsoft.Web/hostingEnvironments/workerPools/Read | Get the properties of a Worker Pool in an App Service Environment |
> | Action | microsoft.web/hostingenvironments/workerpools/skus/read | Get Hosting Environments Workerpools SKUs. |
> | Action | microsoft.web/hostingenvironments/workerpools/usages/read | Get Hosting Environments Workerpools Usages. |
> | Action | Microsoft.Web/hostingEnvironments/workerPools/Write | Create a new Worker Pool in an App Service Environment or update an existing one |
> | Action | Microsoft.Web/hostingEnvironments/Write | Create a new App Service Environment or update existing one |
> | Action | microsoft.web/ishostingenvironmentnameavailable/read | Get if Hosting Environment Name is available. |
> | Action | microsoft.web/ishostnameavailable/read | Check if Hostname is Available. |
> | Action | microsoft.web/isusernameavailable/read | Check if Username is available. |
> | Action | Microsoft.Web/listSitesAssignedToHostName/Read | Get names of sites assigned to hostname. |
> | Action | microsoft.web/locations/apioperations/read | Get Locations API Operations. |
> | Action | microsoft.web/locations/connectiongatewayinstallations/read | Get Locations Connection Gateway Installations. |
> | Action | microsoft.web/locations/extractapidefinitionfromwsdl/action | Extract Api Definition from WSDL for Locations. |
> | Action | microsoft.web/locations/listwsdlinterfaces/action | List WSDL Interfaces for Locations. |
> | Action | microsoft.web/locations/managedapis/apioperations/read | Get Locations Managed API Operations. |
> | Action | Microsoft.Web/locations/managedapis/Join/Action | Joins a Managed API. |
> | Action | microsoft.web/locations/managedapis/read | Get Locations Managed APIs. |
> | Action | microsoft.web/operations/read | Get Operations. |
> | Action | microsoft.web/publishingusers/read | Get Publishing Users. |
> | Action | microsoft.web/publishingusers/write | Update Publishing Users. |
> | Action | Microsoft.Web/recommendations/Read | Get the list of recommendations for subscriptions. |
> | Action | microsoft.web/register/action | Register Microsoft.Web resource provider for the subscription. |
> | Action | microsoft.web/resourcehealthmetadata/read | Get Resource Health Metadata. |
> | Action | microsoft.web/serverfarms/capabilities/read | Get App Service Plans Capabilities. |
> | Action | Microsoft.Web/serverfarms/Delete | Delete an existing App Service Plan |
> | Action | microsoft.web/serverfarms/firstpartyapps/settings/delete | Delete App Service Plans First Party Apps Settings. |
> | Action | microsoft.web/serverfarms/firstpartyapps/settings/read | Get App Service Plans First Party Apps Settings. |
> | Action | microsoft.web/serverfarms/firstpartyapps/settings/write | Update App Service Plans First Party Apps Settings. |
> | Action | microsoft.web/serverfarms/hybridconnectionnamespaces/relays/delete | Delete App Service Plans Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/serverfarms/hybridconnectionnamespaces/relays/read | Get App Service Plans Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/serverfarms/hybridconnectionnamespaces/relays/sites/read | Get App Service Plans Hybrid Connection Namespaces Relays Web Apps. |
> | Action | microsoft.web/serverfarms/hybridconnectionplanlimits/read | Get App Service Plans Hybrid Connection Plan Limits. |
> | Action | microsoft.web/serverfarms/hybridconnectionrelays/read | Get App Service Plans Hybrid Connection Relays. |
> | Action | microsoft.web/serverfarms/metricdefinitions/read | Get App Service Plans Metric Definitions. |
> | Action | microsoft.web/serverfarms/metrics/read | Get App Service Plans Metrics. |
> | Action | microsoft.web/serverfarms/operationresults/read | Get App Service Plans Operation Results. |
> | Action | microsoft.web/serverfarms/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | microsoft.web/serverfarms/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | Microsoft.Web/serverfarms/providers/Microsoft.Insights/metricDefinitions/Read | Gets the available metrics for App Service Plan |
> | Action | Microsoft.Web/serverfarms/Read | Get the properties on an App Service Plan |
> | Action | Microsoft.Web/serverfarms/restartSites/Action | Restart all Web Apps in an App Service Plan |
> | Action | microsoft.web/serverfarms/sites/read | Get App Service Plans Web Apps. |
> | Action | microsoft.web/serverfarms/skus/read | Get App Service Plans SKUs. |
> | Action | microsoft.web/serverfarms/usages/read | Get App Service Plans Usages. |
> | Action | microsoft.web/serverfarms/virtualnetworkconnections/gateways/write | Update App Service Plans Virtual Network Connections Gateways. |
> | Action | microsoft.web/serverfarms/virtualnetworkconnections/read | Get App Service Plans Virtual Network Connections. |
> | Action | microsoft.web/serverfarms/virtualnetworkconnections/routes/delete | Delete App Service Plans Virtual Network Connections Routes. |
> | Action | microsoft.web/serverfarms/virtualnetworkconnections/routes/read | Get App Service Plans Virtual Network Connections Routes. |
> | Action | microsoft.web/serverfarms/virtualnetworkconnections/routes/write | Update App Service Plans Virtual Network Connections Routes. |
> | Action | microsoft.web/serverfarms/workers/reboot/action | Reboot App Service Plans Workers. |
> | Action | Microsoft.Web/serverfarms/Write | Create a new App Service Plan or update an existing one |
> | Action | microsoft.web/sites/analyzecustomhostname/read | Analyze Custom Hostname. |
> | Action | Microsoft.Web/sites/applySlotConfig/Action | Apply web app slot configuration from target slot to the current web app |
> | Action | Microsoft.Web/sites/backup/Action | Create a new web app backup |
> | Action | microsoft.web/sites/backup/read | Get Web Apps Backup. |
> | Action | microsoft.web/sites/backup/write | Update Web Apps Backup. |
> | Action | microsoft.web/sites/backups/action | Discovers an existing app backup that can be restored from a blob in Azure storage. |
> | Action | microsoft.web/sites/backups/delete | Delete Web Apps Backups. |
> | Action | microsoft.web/sites/backups/list/action | List Web Apps Backups. |
> | Action | Microsoft.Web/sites/backups/Read | Get the properties of a web app's backup |
> | Action | microsoft.web/sites/backups/restore/action | Restore Web Apps Backups. |
> | Action | microsoft.web/sites/backups/write | Update Web Apps Backups. |
> | Action | microsoft.web/sites/config/delete | Delete Web Apps Config. |
> | Action | Microsoft.Web/sites/config/list/Action | List Web App's security sensitive settings, such as publishing credentials, app settings and connection strings |
> | Action | Microsoft.Web/sites/config/Read | Get Web App configuration settings |
> | Action | microsoft.web/sites/config/snapshots/read | Get Web Apps Config Snapshots. |
> | Action | Microsoft.Web/sites/config/Write | Update Web App's configuration settings |
> | Action | microsoft.web/sites/containerlogs/action | Get Zipped Container Logs for Web App. |
> | Action | microsoft.web/sites/continuouswebjobs/delete | Delete Web Apps Continuous Web Jobs. |
> | Action | microsoft.web/sites/continuouswebjobs/read | Get Web Apps Continuous Web Jobs. |
> | Action | microsoft.web/sites/continuouswebjobs/start/action | Start Web Apps Continuous Web Jobs. |
> | Action | microsoft.web/sites/continuouswebjobs/stop/action | Stop Web Apps Continuous Web Jobs. |
> | Action | Microsoft.Web/sites/Delete | Delete an existing Web App |
> | Action | microsoft.web/sites/deployments/delete | Delete Web Apps Deployments. |
> | Action | microsoft.web/sites/deployments/log/read | Get Web Apps Deployments Log. |
> | Action | microsoft.web/sites/deployments/read | Get Web Apps Deployments. |
> | Action | microsoft.web/sites/deployments/write | Update Web Apps Deployments. |
> | Action | microsoft.web/sites/detectors/read | Get Web Apps Detectors. |
> | Action | microsoft.web/sites/diagnostics/analyses/execute/Action | Run Web Apps Diagnostics Analysis. |
> | Action | microsoft.web/sites/diagnostics/analyses/read | Get Web Apps Diagnostics Analysis. |
> | Action | microsoft.web/sites/diagnostics/aspnetcore/read | Get Web Apps Diagnostics for ASP.NET Core app. |
> | Action | microsoft.web/sites/diagnostics/autoheal/read | Get Web Apps Diagnostics Autoheal. |
> | Action | microsoft.web/sites/diagnostics/deployment/read | Get Web Apps Diagnostics Deployment. |
> | Action | microsoft.web/sites/diagnostics/deployments/read | Get Web Apps Diagnostics Deployments. |
> | Action | microsoft.web/sites/diagnostics/detectors/execute/Action | Run Web Apps Diagnostics Detector. |
> | Action | microsoft.web/sites/diagnostics/detectors/read | Get Web Apps Diagnostics Detector. |
> | Action | microsoft.web/sites/diagnostics/failedrequestsperuri/read | Get Web Apps Diagnostics Failed Requests Per Uri. |
> | Action | microsoft.web/sites/diagnostics/frebanalysis/read | Get Web Apps Diagnostics FREB Analysis. |
> | Action | microsoft.web/sites/diagnostics/loganalyzer/read | Get Web Apps Diagnostics Log Analyzer. |
> | Action | microsoft.web/sites/diagnostics/read | Get Web Apps Diagnostics Categories. |
> | Action | microsoft.web/sites/diagnostics/runtimeavailability/read | Get Web Apps Diagnostics Runtime Availability. |
> | Action | microsoft.web/sites/diagnostics/servicehealth/read | Get Web Apps Diagnostics Service Health. |
> | Action | microsoft.web/sites/diagnostics/sitecpuanalysis/read | Get Web Apps Diagnostics Site CPU Analysis. |
> | Action | microsoft.web/sites/diagnostics/sitecrashes/read | Get Web Apps Diagnostics Site Crashes. |
> | Action | microsoft.web/sites/diagnostics/sitelatency/read | Get Web Apps Diagnostics Site Latency. |
> | Action | microsoft.web/sites/diagnostics/sitememoryanalysis/read | Get Web Apps Diagnostics Site Memory Analysis. |
> | Action | microsoft.web/sites/diagnostics/siterestartsettingupdate/read | Get Web Apps Diagnostics Site Restart Setting Update. |
> | Action | microsoft.web/sites/diagnostics/siterestartuserinitiated/read | Get Web Apps Diagnostics Site Restart User Initiated. |
> | Action | microsoft.web/sites/diagnostics/siteswap/read | Get Web Apps Diagnostics Site Swap. |
> | Action | microsoft.web/sites/diagnostics/threadcount/read | Get Web Apps Diagnostics Thread Count. |
> | Action | microsoft.web/sites/diagnostics/workeravailability/read | Get Web Apps Diagnostics Workeravailability. |
> | Action | microsoft.web/sites/diagnostics/workerprocessrecycle/read | Get Web Apps Diagnostics Worker Process Recycle. |
> | Action | microsoft.web/sites/domainownershipidentifiers/read | Get Web Apps Domain Ownership Identifiers. |
> | Action | microsoft.web/sites/domainownershipidentifiers/write | Update Web Apps Domain Ownership Identifiers. |
> | Action | microsoft.web/sites/functions/action | Functions Web Apps. |
> | Action | microsoft.web/sites/functions/delete | Delete Web Apps Functions. |
> | Action | microsoft.web/sites/functions/listsecrets/action | List Secrets Web Apps Functions. |
> | Action | microsoft.web/sites/functions/masterkey/read | Get Web Apps Functions Masterkey. |
> | Action | microsoft.web/sites/functions/read | Get Web Apps Functions. |
> | Action | microsoft.web/sites/functions/token/read | Get Web Apps Functions Token. |
> | Action | microsoft.web/sites/functions/write | Update Web Apps Functions. |
> | Action | microsoft.web/sites/hostnamebindings/delete | Delete Web Apps Hostname Bindings. |
> | Action | microsoft.web/sites/hostnamebindings/read | Get Web Apps Hostname Bindings. |
> | Action | microsoft.web/sites/hostnamebindings/write | Update Web Apps Hostname Bindings. |
> | Action | Microsoft.Web/sites/hostruntime/host/_master/read | Get Function App's master key for admin operations |
> | Action | Microsoft.Web/sites/hostruntime/host/action | Perform Function App runtime action like sync triggers, add functions, invoke functions, delete functions etc. |
> | Action | microsoft.web/sites/hybridconnection/delete | Delete Web Apps Hybrid Connection. |
> | Action | microsoft.web/sites/hybridconnection/read | Get Web Apps Hybrid Connection. |
> | Action | microsoft.web/sites/hybridconnection/write | Update Web Apps Hybrid Connection. |
> | Action | microsoft.web/sites/hybridconnectionnamespaces/relays/delete | Delete Web Apps Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/sites/hybridconnectionnamespaces/relays/listkeys/action | List Keys Web Apps Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/sites/hybridconnectionnamespaces/relays/read | Get Web Apps Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/sites/hybridconnectionnamespaces/relays/write | Update Web Apps Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/sites/hybridconnectionrelays/read | Get Web Apps Hybrid Connection Relays. |
> | Action | microsoft.web/sites/instances/deployments/delete | Delete Web Apps Instances Deployments. |
> | Action | microsoft.web/sites/instances/deployments/read | Get Web Apps Instances Deployments. |
> | Action | microsoft.web/sites/instances/extensions/log/read | Get Web Apps Instances Extensions Log. |
> | Action | microsoft.web/sites/instances/extensions/read | Get Web Apps Instances Extensions. |
> | Action | microsoft.web/sites/instances/processes/delete | Delete Web Apps Instances Processes. |
> | Action | microsoft.web/sites/instances/processes/read | Get Web Apps Instances Processes. |
> | Action | microsoft.web/sites/instances/processes/threads/read | Get Web Apps Instances Processes Threads. |
> | Action | microsoft.web/sites/instances/read | Get Web Apps Instances. |
> | Action | microsoft.web/sites/listsyncfunctiontriggerstatus/action | List Sync Function Trigger Status Web Apps. |
> | Action | microsoft.web/sites/metricdefinitions/read | Get Web Apps Metric Definitions. |
> | Action | microsoft.web/sites/metrics/read | Get Web Apps Metrics. |
> | Action | microsoft.web/sites/metricsdefinitions/read | Get Web Apps Metrics Definitions. |
> | Action | microsoft.web/sites/migratemysql/action | Migrate MySql Web Apps. |
> | Action | microsoft.web/sites/migratemysql/read | Get Web Apps Migrate MySql. |
> | Action | microsoft.web/sites/networktrace/action | Network Trace Web Apps. |
> | Action | microsoft.web/sites/newpassword/action | Newpassword Web Apps. |
> | Action | microsoft.web/sites/operationresults/read | Get Web Apps Operation Results. |
> | Action | microsoft.web/sites/operations/read | Get Web Apps Operations. |
> | Action | microsoft.web/sites/perfcounters/read | Get Web Apps Performance Counters. |
> | Action | microsoft.web/sites/premieraddons/delete | Delete Web Apps Premier Addons. |
> | Action | microsoft.web/sites/premieraddons/read | Get Web Apps Premier Addons. |
> | Action | microsoft.web/sites/premieraddons/write | Update Web Apps Premier Addons. |
> | Action | microsoft.web/sites/privateaccess/read | Get data around private site access enablement and authorized Virtual Networks that can access the site. |
> | Action | microsoft.web/sites/processes/read | Get Web Apps Processes. |
> | Action | microsoft.web/sites/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | microsoft.web/sites/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | microsoft.web/sites/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Web App |
> | Action | Microsoft.Web/sites/providers/Microsoft.Insights/metricDefinitions/Read | Gets the available metrics for Web App |
> | Action | microsoft.web/sites/publiccertificates/delete | Delete Web Apps Public Certificates. |
> | Action | microsoft.web/sites/publiccertificates/read | Get Web Apps Public Certificates. |
> | Action | microsoft.web/sites/publiccertificates/write | Update Web Apps Public Certificates. |
> | Action | Microsoft.Web/sites/publish/Action | Publish a Web App |
> | Action | Microsoft.Web/sites/publishxml/Action | Get publishing profile xml for a Web App |
> | Action | microsoft.web/sites/publishxml/read | Get Web Apps Publishing XML. |
> | Action | Microsoft.Web/sites/Read | Get the properties of a Web App |
> | Action | microsoft.web/sites/recommendationhistory/read | Get Web Apps Recommendation History. |
> | Action | microsoft.web/sites/recommendations/disable/action | Disable Web Apps Recommendations. |
> | Action | Microsoft.Web/sites/recommendations/Read | Get the list of recommendations for web app. |
> | Action | microsoft.web/sites/recover/action | Recover Web Apps. |
> | Action | Microsoft.Web/sites/resetSlotConfig/Action | Reset web app configuration |
> | Action | microsoft.web/sites/resourcehealthmetadata/read | Get Web Apps Resource Health Metadata. |
> | Action | Microsoft.Web/sites/restart/Action | Restart a Web App |
> | Action | microsoft.web/sites/restore/read | Get Web Apps Restore. |
> | Action | microsoft.web/sites/restore/write | Restore Web Apps. |
> | Action | microsoft.web/sites/restorefrombackupblob/action | Restore Web App From Backup Blob. |
> | Action | microsoft.web/sites/restorefromdeletedwebapp/action | Restore Web Apps From Deleted App. |
> | Action | microsoft.web/sites/restoresnapshot/action | Restore Web Apps Snapshots. |
> | Action | microsoft.web/sites/siteextensions/delete | Delete Web Apps Site Extensions. |
> | Action | microsoft.web/sites/siteextensions/read | Get Web Apps Site Extensions. |
> | Action | microsoft.web/sites/siteextensions/write | Update Web Apps Site Extensions. |
> | Action | microsoft.web/sites/slots/analyzecustomhostname/read | Get Web Apps Slots Analyze Custom Hostname. |
> | Action | Microsoft.Web/sites/slots/applySlotConfig/Action | Apply web app slot configuration from target slot to the current slot. |
> | Action | Microsoft.Web/sites/slots/backup/Action | Create new Web App Slot backup. |
> | Action | microsoft.web/sites/slots/backup/read | Get Web Apps Slots Backup. |
> | Action | microsoft.web/sites/slots/backup/write | Update Web Apps Slots Backup. |
> | Action | microsoft.web/sites/slots/backups/action | Discover Web Apps Slots Backups. |
> | Action | microsoft.web/sites/slots/backups/delete | Delete Web Apps Slots Backups. |
> | Action | microsoft.web/sites/slots/backups/list/action | List Web Apps Slots Backups. |
> | Action | Microsoft.Web/sites/slots/backups/Read | Get the properties of a web app slots' backup |
> | Action | microsoft.web/sites/slots/backups/restore/action | Restore Web Apps Slots Backups. |
> | Action | microsoft.web/sites/slots/config/delete | Delete Web Apps Slots Config. |
> | Action | Microsoft.Web/sites/slots/config/list/Action | List Web App Slot's security sensitive settings, such as publishing credentials, app settings and connection strings |
> | Action | Microsoft.Web/sites/slots/config/Read | Get Web App Slot's configuration settings |
> | Action | Microsoft.Web/sites/slots/config/Write | Update Web App Slot's configuration settings |
> | Action | microsoft.web/sites/slots/containerlogs/action | Get Zipped Container Logs for Web App Slot. |
> | Action | microsoft.web/sites/slots/continuouswebjobs/delete | Delete Web Apps Slots Continuous Web Jobs. |
> | Action | microsoft.web/sites/slots/continuouswebjobs/read | Get Web Apps Slots Continuous Web Jobs. |
> | Action | microsoft.web/sites/slots/continuouswebjobs/start/action | Start Web Apps Slots Continuous Web Jobs. |
> | Action | microsoft.web/sites/slots/continuouswebjobs/stop/action | Stop Web Apps Slots Continuous Web Jobs. |
> | Action | Microsoft.Web/sites/slots/Delete | Delete an existing Web App Slot |
> | Action | microsoft.web/sites/slots/deployments/delete | Delete Web Apps Slots Deployments. |
> | Action | microsoft.web/sites/slots/deployments/log/read | Get Web Apps Slots Deployments Log. |
> | Action | microsoft.web/sites/slots/deployments/read | Get Web Apps Slots Deployments. |
> | Action | microsoft.web/sites/slots/deployments/write | Update Web Apps Slots Deployments. |
> | Action | microsoft.web/sites/slots/detectors/read | Get Web Apps Slots Detectors. |
> | Action | microsoft.web/sites/slots/diagnostics/analyses/execute/Action | Run Web Apps Slots Diagnostics Analysis. |
> | Action | microsoft.web/sites/slots/diagnostics/analyses/read | Get Web Apps Slots Diagnostics Analysis. |
> | Action | microsoft.web/sites/slots/diagnostics/aspnetcore/read | Get Web Apps Slots Diagnostics for ASP.NET Core app. |
> | Action | microsoft.web/sites/slots/diagnostics/autoheal/read | Get Web Apps Slots Diagnostics Autoheal. |
> | Action | microsoft.web/sites/slots/diagnostics/deployment/read | Get Web Apps Slots Diagnostics Deployment. |
> | Action | microsoft.web/sites/slots/diagnostics/deployments/read | Get Web Apps Slots Diagnostics Deployments. |
> | Action | microsoft.web/sites/slots/diagnostics/detectors/execute/Action | Run Web Apps Slots Diagnostics Detector. |
> | Action | microsoft.web/sites/slots/diagnostics/detectors/read | Get Web Apps Slots Diagnostics Detector. |
> | Action | microsoft.web/sites/slots/diagnostics/frebanalysis/read | Get Web Apps Slots Diagnostics FREB Analysis. |
> | Action | microsoft.web/sites/slots/diagnostics/loganalyzer/read | Get Web Apps Slots Diagnostics Log Analyzer. |
> | Action | microsoft.web/sites/slots/diagnostics/read | Get Web Apps Slots Diagnostics. |
> | Action | microsoft.web/sites/slots/diagnostics/runtimeavailability/read | Get Web Apps Slots Diagnostics Runtime Availability. |
> | Action | microsoft.web/sites/slots/diagnostics/servicehealth/read | Get Web Apps Slots Diagnostics Service Health. |
> | Action | microsoft.web/sites/slots/diagnostics/sitecpuanalysis/read | Get Web Apps Slots Diagnostics Site CPU Analysis. |
> | Action | microsoft.web/sites/slots/diagnostics/sitecrashes/read | Get Web Apps Slots Diagnostics Site Crashes. |
> | Action | microsoft.web/sites/slots/diagnostics/sitelatency/read | Get Web Apps Slots Diagnostics Site Latency. |
> | Action | microsoft.web/sites/slots/diagnostics/sitememoryanalysis/read | Get Web Apps Slots Diagnostics Site Memory Analysis. |
> | Action | microsoft.web/sites/slots/diagnostics/siterestartsettingupdate/read | Get Web Apps Slots Diagnostics Site Restart Setting Update. |
> | Action | microsoft.web/sites/slots/diagnostics/siterestartuserinitiated/read | Get Web Apps Slots Diagnostics Site Restart User Initiated. |
> | Action | microsoft.web/sites/slots/diagnostics/siteswap/read | Get Web Apps Slots Diagnostics Site Swap. |
> | Action | microsoft.web/sites/slots/diagnostics/threadcount/read | Get Web Apps Slots Diagnostics Thread Count. |
> | Action | microsoft.web/sites/slots/diagnostics/workeravailability/read | Get Web Apps Slots Diagnostics Workeravailability. |
> | Action | microsoft.web/sites/slots/diagnostics/workerprocessrecycle/read | Get Web Apps Slots Diagnostics Worker Process Recycle. |
> | Action | microsoft.web/sites/slots/domainownershipidentifiers/read | Get Web Apps Slots Domain Ownership Identifiers. |
> | Action | microsoft.web/sites/slots/functions/read | Get Web Apps Slots Functions. |
> | Action | microsoft.web/sites/slots/hostnamebindings/delete | Delete Web Apps Slots Hostname Bindings. |
> | Action | microsoft.web/sites/slots/hostnamebindings/read | Get Web Apps Slots Hostname Bindings. |
> | Action | microsoft.web/sites/slots/hostnamebindings/write | Update Web Apps Slots Hostname Bindings. |
> | Action | microsoft.web/sites/slots/hybridconnection/delete | Delete Web Apps Slots Hybrid Connection. |
> | Action | microsoft.web/sites/slots/hybridconnection/read | Get Web Apps Slots Hybrid Connection. |
> | Action | microsoft.web/sites/slots/hybridconnection/write | Update Web Apps Slots Hybrid Connection. |
> | Action | microsoft.web/sites/slots/hybridconnectionnamespaces/relays/delete | Delete Web Apps Slots Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/sites/slots/hybridconnectionnamespaces/relays/write | Update Web Apps Slots Hybrid Connection Namespaces Relays. |
> | Action | microsoft.web/sites/slots/hybridconnectionrelays/read | Get Web Apps Slots Hybrid Connection Relays. |
> | Action | microsoft.web/sites/slots/instances/deployments/read | Get Web Apps Slots Instances Deployments. |
> | Action | microsoft.web/sites/slots/instances/processes/delete | Delete Web Apps Slots Instances Processes. |
> | Action | microsoft.web/sites/slots/instances/processes/read | Get Web Apps Slots Instances Processes. |
> | Action | microsoft.web/sites/slots/instances/read | Get Web Apps Slots Instances. |
> | Action | microsoft.web/sites/slots/metricdefinitions/read | Get Web Apps Slots Metric Definitions. |
> | Action | microsoft.web/sites/slots/metrics/read | Get Web Apps Slots Metrics. |
> | Action | microsoft.web/sites/slots/migratemysql/read | Get Web Apps Slots Migrate MySql. |
> | Action | microsoft.web/sites/slots/networktrace/action | Network Trace Web Apps Slots. |
> | Action | microsoft.web/sites/slots/newpassword/action | Newpassword Web Apps Slots. |
> | Action | microsoft.web/sites/slots/operationresults/read | Get Web Apps Slots Operation Results. |
> | Action | microsoft.web/sites/slots/operations/read | Get Web Apps Slots Operations. |
> | Action | microsoft.web/sites/slots/perfcounters/read | Get Web Apps Slots Performance Counters. |
> | Action | microsoft.web/sites/slots/phplogging/read | Get Web Apps Slots Phplogging. |
> | Action | microsoft.web/sites/slots/premieraddons/delete | Delete Web Apps Slots Premier Addons. |
> | Action | microsoft.web/sites/slots/premieraddons/read | Get Web Apps Slots Premier Addons. |
> | Action | microsoft.web/sites/slots/premieraddons/write | Update Web Apps Slots Premier Addons. |
> | Action | microsoft.web/sites/slots/providers/Microsoft.Insights/diagnosticSettings/read | Gets the diagnostic setting for the resource |
> | Action | microsoft.web/sites/slots/providers/Microsoft.Insights/diagnosticSettings/write | Creates or updates the diagnostic setting for the resource |
> | Action | microsoft.web/sites/slots/providers/Microsoft.Insights/logDefinitions/read | Gets the available logs for Web App slots |
> | Action | Microsoft.Web/sites/slots/providers/Microsoft.Insights/metricDefinitions/Read | Gets the available metrics for Web App Slot |
> | Action | microsoft.web/sites/slots/publiccertificates/delete | Delete Web Apps Slots Public Certificates. |
> | Action | microsoft.web/sites/slots/publiccertificates/read | Get Web Apps Slots Public Certificates. |
> | Action | microsoft.web/sites/slots/publiccertificates/write | Create or Update Web Apps Slots Public Certificates. |
> | Action | Microsoft.Web/sites/slots/publish/Action | Publish a Web App Slot |
> | Action | Microsoft.Web/sites/slots/publishxml/Action | Get publishing profile xml for Web App Slot |
> | Action | Microsoft.Web/sites/slots/Read | Get the properties of a Web App deployment slot |
> | Action | microsoft.web/sites/slots/recover/action | Recover Web Apps Slots. |
> | Action | Microsoft.Web/sites/slots/resetSlotConfig/Action | Reset web app slot configuration |
> | Action | microsoft.web/sites/slots/resourcehealthmetadata/read | Get Web Apps Slots Resource Health Metadata. |
> | Action | Microsoft.Web/sites/slots/restart/Action | Restart a Web App Slot |
> | Action | microsoft.web/sites/slots/restore/read | Get Web Apps Slots Restore. |
> | Action | microsoft.web/sites/slots/restore/write | Restore Web Apps Slots. |
> | Action | microsoft.web/sites/slots/restorefrombackupblob/action | Restore Web Apps Slot From Backup Blob. |
> | Action | microsoft.web/sites/slots/restorefromdeletedwebapp/action | Restore Web App Slots From Deleted App. |
> | Action | microsoft.web/sites/slots/restoresnapshot/action | Restore Web Apps Slots Snapshots. |
> | Action | microsoft.web/sites/slots/siteextensions/delete | Delete Web Apps Slots Site Extensions. |
> | Action | microsoft.web/sites/slots/siteextensions/read | Get Web Apps Slots Site Extensions. |
> | Action | microsoft.web/sites/slots/siteextensions/write | Update Web Apps Slots Site Extensions. |
> | Action | Microsoft.Web/sites/slots/slotsdiffs/Action | Get differences in configuration between web app and slots |
> | Action | Microsoft.Web/sites/slots/slotsswap/Action | Swap Web App deployment slots |
> | Action | microsoft.web/sites/slots/snapshots/read | Get Web Apps Slots Snapshots. |
> | Action | Microsoft.Web/sites/slots/sourcecontrols/Delete | Delete Web App Slot's source control configuration settings |
> | Action | Microsoft.Web/sites/slots/sourcecontrols/Read | Get Web App Slot's source control configuration settings |
> | Action | Microsoft.Web/sites/slots/sourcecontrols/Write | Update Web App Slot's source control configuration settings |
> | Action | Microsoft.Web/sites/slots/start/Action | Start a Web App Slot |
> | Action | Microsoft.Web/sites/slots/stop/Action | Stop a Web App Slot |
> | Action | microsoft.web/sites/slots/sync/action | Sync Web Apps Slots. |
> | Action | microsoft.web/sites/slots/triggeredwebjobs/delete | Delete Web Apps Slots Triggered WebJobs. |
> | Action | microsoft.web/sites/slots/triggeredwebjobs/read | Get Web Apps Slots Triggered WebJobs. |
> | Action | microsoft.web/sites/slots/triggeredwebjobs/run/action | Run Web Apps Slots Triggered WebJobs. |
> | Action | microsoft.web/sites/slots/usages/read | Get Web Apps Slots Usages. |
> | Action | microsoft.web/sites/slots/virtualnetworkconnections/delete | Delete Web Apps Slots Virtual Network Connections. |
> | Action | microsoft.web/sites/slots/virtualnetworkconnections/gateways/write | Update Web Apps Slots Virtual Network Connections Gateways. |
> | Action | microsoft.web/sites/slots/virtualnetworkconnections/read | Get Web Apps Slots Virtual Network Connections. |
> | Action | microsoft.web/sites/slots/virtualnetworkconnections/write | Update Web Apps Slots Virtual Network Connections. |
> | Action | microsoft.web/sites/slots/webjobs/read | Get Web Apps Slots WebJobs. |
> | Action | Microsoft.Web/sites/slots/Write | Create a new Web App Slot or update an existing one |
> | Action | Microsoft.Web/sites/slotsdiffs/Action | Get differences in configuration between web app and slots |
> | Action | Microsoft.Web/sites/slotsswap/Action | Swap Web App deployment slots |
> | Action | microsoft.web/sites/snapshots/read | Get Web Apps Snapshots. |
> | Action | Microsoft.Web/sites/sourcecontrols/Delete | Delete Web App's source control configuration settings |
> | Action | Microsoft.Web/sites/sourcecontrols/Read | Get Web App's source control configuration settings |
> | Action | Microsoft.Web/sites/sourcecontrols/Write | Update Web App's source control configuration settings |
> | Action | Microsoft.Web/sites/start/Action | Start a Web App |
> | Action | Microsoft.Web/sites/stop/Action | Stop a Web App |
> | Action | microsoft.web/sites/sync/action | Sync Web Apps. |
> | Action | microsoft.web/sites/syncfunctiontriggers/action | Sync Function Triggers for Web Apps. |
> | Action | microsoft.web/sites/triggeredwebjobs/delete | Delete Web Apps Triggered WebJobs. |
> | Action | microsoft.web/sites/triggeredwebjobs/history/read | Get Web Apps Triggered WebJobs History. |
> | Action | microsoft.web/sites/triggeredwebjobs/read | Get Web Apps Triggered WebJobs. |
> | Action | microsoft.web/sites/triggeredwebjobs/run/action | Run Web Apps Triggered WebJobs. |
> | Action | microsoft.web/sites/usages/read | Get Web Apps Usages. |
> | Action | microsoft.web/sites/virtualnetworkconnections/delete | Delete Web Apps Virtual Network Connections. |
> | Action | microsoft.web/sites/virtualnetworkconnections/gateways/read | Get Web Apps Virtual Network Connections Gateways. |
> | Action | microsoft.web/sites/virtualnetworkconnections/gateways/write | Update Web Apps Virtual Network Connections Gateways. |
> | Action | microsoft.web/sites/virtualnetworkconnections/read | Get Web Apps Virtual Network Connections. |
> | Action | microsoft.web/sites/virtualnetworkconnections/write | Update Web Apps Virtual Network Connections. |
> | Action | microsoft.web/sites/webjobs/read | Get Web Apps WebJobs. |
> | Action | Microsoft.Web/sites/Write | Create a new Web App or update an existing one |
> | Action | microsoft.web/skus/read | Get SKUs. |
> | Action | microsoft.web/sourcecontrols/read | Get Source Controls. |
> | Action | microsoft.web/sourcecontrols/write | Update Source Controls. |
> | Action | microsoft.web/unregister/action | Unregister Microsoft.Web resource provider for the subscription. |
> | Action | microsoft.web/validate/action | Validate . |
> | Action | microsoft.web/verifyhostingenvironmentvnet/action | Verify Hosting Environment Vnet. |

## Microsoft.WorkloadMonitor

> [!div class="mx-tdCol2BreakAll"]
> | Action Type | Operation | Description |
> | --- | --- | --- |
> | Action | Microsoft.WorkloadMonitor/components/read | Gets components for the resource |
> | Action | Microsoft.WorkloadMonitor/componentsSummary/read | Gets summary of components |
> | Action | Microsoft.WorkloadMonitor/monitorInstances/read | Gets instances of monitors for the resource |
> | Action | Microsoft.WorkloadMonitor/monitorInstancesSummary/read | Gets summary of monitor instances |
> | Action | Microsoft.WorkloadMonitor/monitors/read | Gets monitors for the resource |
> | Action | Microsoft.WorkloadMonitor/monitors/write | Configure monitor for the resource |
> | Action | Microsoft.WorkloadMonitor/notificationSettings/read | Gets notification settings for the resource |
> | Action | Microsoft.WorkloadMonitor/notificationSettings/write | Configure notification settings for the resource |
> | Action | Microsoft.WorkloadMonitor/operations/read | Gets the supported operations |

## Next steps

- [Custom roles](custom-roles.md)
- [Built-in roles](built-in-roles.md)
