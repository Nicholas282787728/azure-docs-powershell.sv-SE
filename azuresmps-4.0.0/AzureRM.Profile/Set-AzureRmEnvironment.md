---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571519"
---
# <span data-ttu-id="e66a3-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e66a3-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="e66a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e66a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e66a3-103">Anger egenskaper för en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="e66a3-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="e66a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e66a3-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e66a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e66a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e66a3-106">Med Set-AzureRMEnvironment cmdlet anges slut punkter och metadata för anslutning till en instans av Azure.</span><span class="sxs-lookup"><span data-stu-id="e66a3-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="e66a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e66a3-107">EXAMPLES</span></span>

### <span data-ttu-id="e66a3-108">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="e66a3-108">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="e66a3-109">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzureRmEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="e66a3-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="e66a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e66a3-110">PARAMETERS</span></span>

### <span data-ttu-id="e66a3-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e66a3-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="e66a3-112">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="e66a3-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e66a3-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="e66a3-114">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="e66a3-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="e66a3-115">-AdTenant</span></span>
<span data-ttu-id="e66a3-116">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e66a3-116">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e66a3-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="e66a3-118">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="e66a3-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e66a3-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="e66a3-120">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="e66a3-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="e66a3-121">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="e66a3-121">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e66a3-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="e66a3-123">Anger domän namn för viktiga valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="e66a3-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="e66a3-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e66a3-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="e66a3-125">Anger mål gruppen för de åtkomsttoken som tillåter begäran om nyckel valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="e66a3-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="e66a3-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="e66a3-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="e66a3-127">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="e66a3-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e66a3-128">-GalleryEndpoint</span></span>
<span data-ttu-id="e66a3-129">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="e66a3-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="e66a3-130">-GraphAudience</span></span>
<span data-ttu-id="e66a3-131">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="e66a3-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="e66a3-132">-GraphEndpoint</span></span>
<span data-ttu-id="e66a3-133">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="e66a3-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="e66a3-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="e66a3-135">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="e66a3-135">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="e66a3-136">-Name</span></span>
<span data-ttu-id="e66a3-137">Anger namnet på den miljö som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="e66a3-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="e66a3-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="e66a3-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="e66a3-139">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="e66a3-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e66a3-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="e66a3-141">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="e66a3-141">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e66a3-142">-ServiceEndpoint</span></span>
<span data-ttu-id="e66a3-143">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="e66a3-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e66a3-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="e66a3-145">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="e66a3-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="e66a3-146">-StorageEndpoint</span></span>
<span data-ttu-id="e66a3-147">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="e66a3-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="e66a3-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e66a3-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="e66a3-149">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="e66a3-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e66a3-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e66a3-150">-Confirm</span></span>
<span data-ttu-id="e66a3-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e66a3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e66a3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e66a3-152">-WhatIf</span></span>
<span data-ttu-id="e66a3-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e66a3-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e66a3-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e66a3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e66a3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e66a3-155">CommonParameters</span></span>
<span data-ttu-id="e66a3-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e66a3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e66a3-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e66a3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e66a3-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e66a3-158">INPUTS</span></span>

## <span data-ttu-id="e66a3-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e66a3-159">OUTPUTS</span></span>

### <span data-ttu-id="e66a3-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e66a3-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="e66a3-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e66a3-161">NOTES</span></span>

## <span data-ttu-id="e66a3-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e66a3-162">RELATED LINKS</span></span>

[<span data-ttu-id="e66a3-163">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e66a3-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="e66a3-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e66a3-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="e66a3-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="e66a3-165">Remove-AzureRMEnvironment</span></span>]()

