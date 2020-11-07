---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 468abd4edc2e60ec0e13c80d345bafdac7ad2be5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757243"
---
# <span data-ttu-id="7a199-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="7a199-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="7a199-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a199-102">SYNOPSIS</span></span>
<span data-ttu-id="7a199-103">Anger egenskaper för en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="7a199-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a199-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a199-104">SYNTAX</span></span>

### <span data-ttu-id="7a199-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="7a199-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>][-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a199-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]] [[-AzureOperationalInsightsEndpoint] <String>] 
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [-Scope <ContextModificationScope>] 
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a199-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a199-107">DESCRIPTION</span></span>
<span data-ttu-id="7a199-108">Med Set-AzureRMEnvironment cmdlet anges slut punkter och metadata för anslutning till en instans av Azure.</span><span class="sxs-lookup"><span data-stu-id="7a199-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="7a199-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a199-109">EXAMPLES</span></span>

### <span data-ttu-id="7a199-110">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="7a199-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
```

<span data-ttu-id="7a199-111">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzureRmEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="7a199-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="7a199-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a199-112">PARAMETERS</span></span>

### <span data-ttu-id="7a199-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="7a199-114">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="7a199-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7a199-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="7a199-116">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="7a199-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="7a199-117">-AdTenant</span></span>
<span data-ttu-id="7a199-118">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a199-118">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-119">-ARMEndpoint</span></span>
<span data-ttu-id="7a199-120">Slut punkten för Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7a199-120">The Azure Resource Manager endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7a199-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="7a199-122">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="7a199-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7a199-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="7a199-124">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="7a199-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="7a199-125">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="7a199-125">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7a199-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="7a199-127">Anger domän namn för viktiga valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="7a199-127">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7a199-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="7a199-129">Anger mål gruppen för de åtkomsttoken som tillåter begäran om nyckel valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="7a199-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="7a199-130">-DataLakeAudience</span></span>
<span data-ttu-id="7a199-131">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="7a199-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a199-132">-DefaultProfile</span></span>
<span data-ttu-id="7a199-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a199-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="7a199-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="7a199-135">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="7a199-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-136">-GalleryEndpoint</span></span>
<span data-ttu-id="7a199-137">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="7a199-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="7a199-138">-GraphAudience</span></span>
<span data-ttu-id="7a199-139">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="7a199-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-140">-GraphEndpoint</span></span>
<span data-ttu-id="7a199-141">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="7a199-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="7a199-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="7a199-143">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="7a199-143">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a199-144">-Name</span></span>
<span data-ttu-id="7a199-145">Anger namnet på den miljö som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="7a199-145">Specifies the name of the environment to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="7a199-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="7a199-147">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="7a199-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="7a199-149">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="7a199-149">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-150">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="7a199-150">-Scope</span></span>
<span data-ttu-id="7a199-151">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="7a199-151">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-152">-ServiceEndpoint</span></span>
<span data-ttu-id="7a199-153">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="7a199-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7a199-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="7a199-155">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="7a199-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-156">-StorageEndpoint</span></span>
<span data-ttu-id="7a199-157">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="7a199-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7a199-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="7a199-159">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="7a199-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-160">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7a199-160">-BatchEndpointResourceId</span></span>
<span data-ttu-id="7a199-161">Resurs-ID för Azure Batch-tjänsten som är mottagaren av den begärda token</span><span class="sxs-lookup"><span data-stu-id="7a199-161">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-162">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="7a199-162">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="7a199-163">Anger slut punkten för funktionen för användnings frågor.</span><span class="sxs-lookup"><span data-stu-id="7a199-163">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-164">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7a199-164">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="7a199-165">Anger mål grupp för de åtkomsttoken som ger begäran om tjänster för drifts Insights.</span><span class="sxs-lookup"><span data-stu-id="7a199-165">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-166">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a199-166">-Confirm</span></span>
<span data-ttu-id="7a199-167">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a199-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a199-168">-WhatIf</span></span>
<span data-ttu-id="7a199-169">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a199-169">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a199-170">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a199-170">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a199-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a199-171">CommonParameters</span></span>
<span data-ttu-id="7a199-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a199-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a199-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a199-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a199-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a199-174">INPUTS</span></span>

### <span data-ttu-id="7a199-175">Ingen</span><span class="sxs-lookup"><span data-stu-id="7a199-175">None</span></span>
<span data-ttu-id="7a199-176">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7a199-176">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a199-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a199-177">OUTPUTS</span></span>

### <span data-ttu-id="7a199-178">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7a199-178">PSAzureEnvironment</span></span>

## <span data-ttu-id="7a199-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a199-179">NOTES</span></span>

## <span data-ttu-id="7a199-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a199-180">RELATED LINKS</span></span>

[<span data-ttu-id="7a199-181">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7a199-181">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="7a199-182">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7a199-182">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="7a199-183">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7a199-183">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

