---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 92a8c816f1c5a76b0f3725b70a627b798b9de2b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523371"
---
# <span data-ttu-id="52ebb-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="52ebb-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="52ebb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="52ebb-103">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="52ebb-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="52ebb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52ebb-104">SYNTAX</span></span>

### <span data-ttu-id="52ebb-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="52ebb-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52ebb-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ebb-107">Identifierings</span><span class="sxs-lookup"><span data-stu-id="52ebb-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ebb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52ebb-108">DESCRIPTION</span></span>
<span data-ttu-id="52ebb-109">Add-AzEnvironment cmdlet lägger till slut punkter och metadata för att aktivera Azure Resource Manager-cmdlets för att ansluta till en ny instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="52ebb-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="52ebb-110">De inbyggda miljöerna AzureCloud och AzureChinaCloud är befintliga offentliga instanser av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="52ebb-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="52ebb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52ebb-111">EXAMPLES</span></span>

### <span data-ttu-id="52ebb-112">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="52ebb-112">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="52ebb-113">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="52ebb-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="52ebb-114">Exempel 2: upptäcka en ny miljö via URI</span><span class="sxs-lookup"><span data-stu-id="52ebb-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="52ebb-115">I det här exemplet upptäcker vi att en ny Azure-miljö från `https://configuredmetadata.net` URI: n.</span><span class="sxs-lookup"><span data-stu-id="52ebb-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="52ebb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52ebb-116">PARAMETERS</span></span>

### <span data-ttu-id="52ebb-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="52ebb-118">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="52ebb-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="52ebb-120">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="52ebb-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="52ebb-121">-AdTenant</span></span>
<span data-ttu-id="52ebb-122">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="52ebb-122">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-123">-ARMEndpoint</span></span>
<span data-ttu-id="52ebb-124">Azure Resource Manager slut punkt</span><span class="sxs-lookup"><span data-stu-id="52ebb-124">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-125">-Upptäck automatiskt</span><span class="sxs-lookup"><span data-stu-id="52ebb-125">-AutoDiscover</span></span>
<span data-ttu-id="52ebb-126">Upptäck miljöer via standard eller konfigurerad slut punkt.</span><span class="sxs-lookup"><span data-stu-id="52ebb-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="52ebb-128">Resurs-ID för Azure Analysis Services-resursen.</span><span class="sxs-lookup"><span data-stu-id="52ebb-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="52ebb-130">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="52ebb-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="52ebb-132">Resurs-ID för Azure attestering-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="52ebb-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="52ebb-134">DNS-suffix för Azure attestering-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="52ebb-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="52ebb-136">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="52ebb-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="52ebb-138">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="52ebb-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="52ebb-139">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="52ebb-139">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="52ebb-141">DNS-suffix för Azure Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="52ebb-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="52ebb-142">Exempel är vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="52ebb-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="52ebb-144">Resurs-ID för Azure Key Vault data-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="52ebb-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="52ebb-146">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="52ebb-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="52ebb-148">Mål gruppen för tokens som autentiserar med Azure logganalys-API: t.</span><span class="sxs-lookup"><span data-stu-id="52ebb-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="52ebb-150">Resurs-ID för Azure Synapse Analytics som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="52ebb-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="52ebb-152">DNS-suffix för Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="52ebb-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="52ebb-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="52ebb-154">Resurs-ID för Azure Batch-tjänsten som är mottagaren av den begärda token</span><span class="sxs-lookup"><span data-stu-id="52ebb-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="52ebb-156">Suffix för Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="52ebb-156">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="52ebb-157">-DataLakeAudience</span></span>
<span data-ttu-id="52ebb-158">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="52ebb-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ebb-159">-DefaultProfile</span></span>
<span data-ttu-id="52ebb-160">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="52ebb-160">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="52ebb-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="52ebb-162">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="52ebb-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-163">-GalleryEndpoint</span></span>
<span data-ttu-id="52ebb-164">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="52ebb-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="52ebb-165">-GraphAudience</span></span>
<span data-ttu-id="52ebb-166">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="52ebb-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-167">-GraphEndpoint</span></span>
<span data-ttu-id="52ebb-168">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="52ebb-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="52ebb-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="52ebb-170">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="52ebb-170">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-171">-Namn</span><span class="sxs-lookup"><span data-stu-id="52ebb-171">-Name</span></span>
<span data-ttu-id="52ebb-172">Anger namnet på den miljö som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="52ebb-172">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="52ebb-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="52ebb-174">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="52ebb-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="52ebb-176">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="52ebb-176">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-177">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="52ebb-177">-Scope</span></span>
<span data-ttu-id="52ebb-178">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="52ebb-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-179">-ServiceEndpoint</span></span>
<span data-ttu-id="52ebb-180">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="52ebb-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="52ebb-182">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="52ebb-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="52ebb-183">-StorageEndpoint</span></span>
<span data-ttu-id="52ebb-184">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="52ebb-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="52ebb-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="52ebb-186">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="52ebb-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-187">-URI</span><span class="sxs-lookup"><span data-stu-id="52ebb-187">-Uri</span></span>
<span data-ttu-id="52ebb-188">Anger URI för Internet resursen för att hämta miljöer.</span><span class="sxs-lookup"><span data-stu-id="52ebb-188">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-189">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52ebb-189">-Confirm</span></span>
<span data-ttu-id="52ebb-190">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52ebb-190">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ebb-191">-WhatIf</span></span>
<span data-ttu-id="52ebb-192">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52ebb-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52ebb-193">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52ebb-193">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ebb-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ebb-194">CommonParameters</span></span>
<span data-ttu-id="52ebb-195">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ebb-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ebb-196">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52ebb-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ebb-197">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52ebb-197">INPUTS</span></span>

### <span data-ttu-id="52ebb-198">System. String</span><span class="sxs-lookup"><span data-stu-id="52ebb-198">System.String</span></span>

### <span data-ttu-id="52ebb-199">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52ebb-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52ebb-200">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52ebb-200">OUTPUTS</span></span>

### <span data-ttu-id="52ebb-201">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="52ebb-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="52ebb-202">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52ebb-202">NOTES</span></span>

## <span data-ttu-id="52ebb-203">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52ebb-203">RELATED LINKS</span></span>

[<span data-ttu-id="52ebb-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="52ebb-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="52ebb-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="52ebb-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="52ebb-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="52ebb-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

