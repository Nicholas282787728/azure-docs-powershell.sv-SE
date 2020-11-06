---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ed50d8e25dca0998e7e3e026783fe4ec78e6ce7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572684"
---
# <span data-ttu-id="ef0f7-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="ef0f7-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="ef0f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0f7-103">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef0f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef0f7-104">SYNTAX</span></span>

### <span data-ttu-id="ef0f7-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="ef0f7-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0f7-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef0f7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef0f7-107">DESCRIPTION</span></span>
<span data-ttu-id="ef0f7-108">Add-AzureRmEnvironment cmdlet lägger till slut punkter och metadata för att aktivera Azure Resource Manager-cmdlets för att ansluta till en ny instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="ef0f7-109">De inbyggda miljöerna AzureCloud och AzureChinaCloud är befintliga offentliga instanser av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="ef0f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef0f7-110">EXAMPLES</span></span>

### <span data-ttu-id="ef0f7-111">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="ef0f7-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment `
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.
```

## <span data-ttu-id="ef0f7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef0f7-112">PARAMETERS</span></span>

### <span data-ttu-id="ef0f7-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="ef0f7-114">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="ef0f7-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0f7-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="ef0f7-116">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="ef0f7-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="ef0f7-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="ef0f7-117">-AdTenant</span></span>
<span data-ttu-id="ef0f7-118">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="ef0f7-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-119">-ARMEndpoint</span></span>
<span data-ttu-id="ef0f7-120">Azure Resource Manager slut punkt</span><span class="sxs-lookup"><span data-stu-id="ef0f7-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="ef0f7-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ef0f7-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="ef0f7-122">DNS-suffix för Azure Analysis Services-tjänstens slut punkter</span><span class="sxs-lookup"><span data-stu-id="ef0f7-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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


### <span data-ttu-id="ef0f7-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ef0f7-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="ef0f7-124">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="ef0f7-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="ef0f7-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ef0f7-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="ef0f7-126">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="ef0f7-127">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="ef0f7-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="ef0f7-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="ef0f7-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="ef0f7-129">Anger domän namn för viktiga valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-129">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0f7-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="ef0f7-131">Anger mål gruppen för de åtkomsttoken som tillåter begäran om nyckel valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="ef0f7-133">Anger slut punkten för funktionen för användnings frågor.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0f7-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="ef0f7-135">Anger mål grupp för de åtkomsttoken som ger begäran om tjänster för drifts Insights.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0f7-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="ef0f7-137">Resurs-ID för Azure Batch-tjänsten som är mottagaren av den begärda token</span><span class="sxs-lookup"><span data-stu-id="ef0f7-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="ef0f7-138">-DataLakeAudience</span></span>
<span data-ttu-id="ef0f7-139">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0f7-140">-DefaultProfile</span></span>
<span data-ttu-id="ef0f7-141">Credeetnails, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ef0f7-141">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="ef0f7-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="ef0f7-143">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="ef0f7-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-144">-GalleryEndpoint</span></span>
<span data-ttu-id="ef0f7-145">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="ef0f7-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="ef0f7-146">-GraphAudience</span></span>
<span data-ttu-id="ef0f7-147">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="ef0f7-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-148">-GraphEndpoint</span></span>
<span data-ttu-id="ef0f7-149">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="ef0f7-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="ef0f7-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="ef0f7-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="ef0f7-151">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="ef0f7-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef0f7-152">-Name</span></span>
<span data-ttu-id="ef0f7-153">Anger namnet på den miljö som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-153">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="ef0f7-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="ef0f7-155">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="ef0f7-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="ef0f7-157">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="ef0f7-158">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="ef0f7-158">-Scope</span></span>
<span data-ttu-id="ef0f7-159">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ef0f7-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-160">-ServiceEndpoint</span></span>
<span data-ttu-id="ef0f7-161">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="ef0f7-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="ef0f7-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="ef0f7-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="ef0f7-163">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="ef0f7-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef0f7-164">-StorageEndpoint</span></span>
<span data-ttu-id="ef0f7-165">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="ef0f7-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0f7-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="ef0f7-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="ef0f7-167">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="ef0f7-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef0f7-168">-Confirm</span></span>
<span data-ttu-id="ef0f7-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0f7-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0f7-170">-WhatIf</span></span>
<span data-ttu-id="ef0f7-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef0f7-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0f7-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0f7-173">CommonParameters</span></span>
<span data-ttu-id="ef0f7-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0f7-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0f7-175">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef0f7-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0f7-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef0f7-176">INPUTS</span></span>

### <span data-ttu-id="ef0f7-177">System. String</span><span class="sxs-lookup"><span data-stu-id="ef0f7-177">System.String</span></span>

### <span data-ttu-id="ef0f7-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef0f7-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ef0f7-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef0f7-179">OUTPUTS</span></span>

### <span data-ttu-id="ef0f7-180">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ef0f7-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="ef0f7-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef0f7-181">NOTES</span></span>

## <span data-ttu-id="ef0f7-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef0f7-182">RELATED LINKS</span></span>

[<span data-ttu-id="ef0f7-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ef0f7-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="ef0f7-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ef0f7-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="ef0f7-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ef0f7-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

