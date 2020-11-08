---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: ba5a398e21543bc4b19c09309884ceb11fed3197
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261495"
---
# <span data-ttu-id="d9092-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9092-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="d9092-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9092-102">SYNOPSIS</span></span>
<span data-ttu-id="d9092-103">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d9092-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="d9092-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9092-104">SYNTAX</span></span>

### <span data-ttu-id="d9092-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="d9092-105">Name (Default)</span></span>
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
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9092-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9092-107">Identifierings</span><span class="sxs-lookup"><span data-stu-id="d9092-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9092-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9092-108">DESCRIPTION</span></span>
<span data-ttu-id="d9092-109">Add-AzEnvironment cmdlet lägger till slut punkter och metadata för att aktivera Azure Resource Manager-cmdlets för att ansluta till en ny instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d9092-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="d9092-110">De inbyggda miljöerna AzureCloud och AzureChinaCloud är befintliga offentliga instanser av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d9092-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="d9092-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9092-111">EXAMPLES</span></span>

### <span data-ttu-id="d9092-112">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="d9092-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="d9092-113">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="d9092-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="d9092-114">Exempel 2: upptäcka en ny miljö via URI</span><span class="sxs-lookup"><span data-stu-id="d9092-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="d9092-115">I det här exemplet upptäcker vi att en ny Azure-miljö från https://configuredmetadata.net URI: n.</span><span class="sxs-lookup"><span data-stu-id="d9092-115">In this example, we are discovering a new Azure environment from the https://configuredmetadata.net Uri.</span></span>

## <span data-ttu-id="d9092-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9092-116">PARAMETERS</span></span>

### <span data-ttu-id="d9092-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="d9092-118">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="d9092-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="d9092-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="d9092-120">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="d9092-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="d9092-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="d9092-121">-AdTenant</span></span>
<span data-ttu-id="d9092-122">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9092-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="d9092-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-123">-ARMEndpoint</span></span>
<span data-ttu-id="d9092-124">Azure Resource Manager slut punkt</span><span class="sxs-lookup"><span data-stu-id="d9092-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="d9092-125">-Upptäck automatiskt</span><span class="sxs-lookup"><span data-stu-id="d9092-125">-AutoDiscover</span></span>
<span data-ttu-id="d9092-126">Upptäck miljöer via standard eller konfigurerad slut punkt.</span><span class="sxs-lookup"><span data-stu-id="d9092-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="d9092-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="d9092-128">Resurs-ID för Azure Analysis Services-resursen.</span><span class="sxs-lookup"><span data-stu-id="d9092-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="d9092-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="d9092-130">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="d9092-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="d9092-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="d9092-132">Resurs-ID för Azure attestering-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="d9092-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="d9092-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="d9092-134">DNS-suffix för Azure attestering-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d9092-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="d9092-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="d9092-136">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="d9092-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="d9092-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="d9092-138">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="d9092-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="d9092-139">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="d9092-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="d9092-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="d9092-141">DNS-suffix för Azure Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d9092-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="d9092-142">Exempel är vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="d9092-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="d9092-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="d9092-144">Resurs-ID för Azure Key Vault data-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="d9092-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="d9092-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="d9092-146">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="d9092-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="d9092-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="d9092-148">Mål gruppen för tokens som autentiserar med Azure logganalys-API: t.</span><span class="sxs-lookup"><span data-stu-id="d9092-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="d9092-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="d9092-150">Resurs-ID för Azure Synapse Analytics som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="d9092-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="d9092-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="d9092-152">DNS-suffix för Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d9092-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="d9092-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9092-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="d9092-154">Resurs-ID för Azure Batch-tjänsten som är mottagaren av den begärda token</span><span class="sxs-lookup"><span data-stu-id="d9092-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="d9092-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="d9092-155">-DataLakeAudience</span></span>
<span data-ttu-id="d9092-156">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="d9092-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="d9092-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9092-157">-DefaultProfile</span></span>
<span data-ttu-id="d9092-158">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d9092-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9092-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9092-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="d9092-160">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="d9092-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="d9092-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-161">-GalleryEndpoint</span></span>
<span data-ttu-id="d9092-162">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="d9092-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="d9092-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="d9092-163">-GraphAudience</span></span>
<span data-ttu-id="d9092-164">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="d9092-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="d9092-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-165">-GraphEndpoint</span></span>
<span data-ttu-id="d9092-166">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="d9092-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="d9092-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="d9092-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="d9092-168">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="d9092-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="d9092-169">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9092-169">-Name</span></span>
<span data-ttu-id="d9092-170">Anger namnet på den miljö som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="d9092-170">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="d9092-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="d9092-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="d9092-172">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="d9092-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="d9092-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="d9092-174">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="d9092-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="d9092-175">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="d9092-175">-Scope</span></span>
<span data-ttu-id="d9092-176">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="d9092-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d9092-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-177">-ServiceEndpoint</span></span>
<span data-ttu-id="d9092-178">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="d9092-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="d9092-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="d9092-180">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="d9092-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="d9092-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9092-181">-StorageEndpoint</span></span>
<span data-ttu-id="d9092-182">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="d9092-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="d9092-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d9092-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="d9092-184">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="d9092-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="d9092-185">-URI</span><span class="sxs-lookup"><span data-stu-id="d9092-185">-Uri</span></span>
<span data-ttu-id="d9092-186">Anger URI för Internet resursen för att hämta miljöer.</span><span class="sxs-lookup"><span data-stu-id="d9092-186">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="d9092-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9092-187">-Confirm</span></span>
<span data-ttu-id="d9092-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9092-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9092-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9092-189">-WhatIf</span></span>
<span data-ttu-id="d9092-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9092-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9092-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9092-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9092-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9092-192">CommonParameters</span></span>
<span data-ttu-id="d9092-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9092-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9092-194">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9092-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9092-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9092-195">INPUTS</span></span>

### <span data-ttu-id="d9092-196">System. String</span><span class="sxs-lookup"><span data-stu-id="d9092-196">System.String</span></span>

### <span data-ttu-id="d9092-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9092-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9092-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9092-198">OUTPUTS</span></span>

### <span data-ttu-id="d9092-199">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9092-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="d9092-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9092-200">NOTES</span></span>

## <span data-ttu-id="d9092-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9092-201">RELATED LINKS</span></span>

[<span data-ttu-id="d9092-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9092-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="d9092-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9092-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="d9092-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9092-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

