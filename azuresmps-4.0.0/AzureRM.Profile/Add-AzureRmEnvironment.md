---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571411"
---
# <span data-ttu-id="6b3f1-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="6b3f1-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="6b3f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3f1-103">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="6b3f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b3f1-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b3f1-105">DESCRIPTION</span></span>
<span data-ttu-id="6b3f1-106">Add-AzureRmEnvironment cmdlet lägger till slut punkter och metadata för att aktivera Azure Resource Manager-cmdlets för att ansluta till en ny instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="6b3f1-107">De inbyggda miljöerna AzureCloud och AzureChinaCloud är befintliga offentliga instanser av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="6b3f1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b3f1-108">EXAMPLES</span></span>

### <span data-ttu-id="6b3f1-109">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="6b3f1-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="6b3f1-110">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzureRmEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="6b3f1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b3f1-111">PARAMETERS</span></span>

### <span data-ttu-id="6b3f1-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b3f1-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="6b3f1-113">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="6b3f1-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3f1-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="6b3f1-115">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="6b3f1-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="6b3f1-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="6b3f1-116">-AdTenant</span></span>
<span data-ttu-id="6b3f1-117">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-117">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="6b3f1-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6b3f1-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="6b3f1-119">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="6b3f1-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="6b3f1-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6b3f1-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="6b3f1-121">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="6b3f1-122">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="6b3f1-122">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="6b3f1-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="6b3f1-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="6b3f1-124">Anger domän namn för viktiga valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-124">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="6b3f1-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="6b3f1-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="6b3f1-126">Anger mål gruppen för de åtkomsttoken som tillåter begäran om nyckel valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="6b3f1-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="6b3f1-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="6b3f1-128">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="6b3f1-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b3f1-129">-GalleryEndpoint</span></span>
<span data-ttu-id="6b3f1-130">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="6b3f1-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="6b3f1-131">-GraphAudience</span></span>
<span data-ttu-id="6b3f1-132">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="6b3f1-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b3f1-133">-GraphEndpoint</span></span>
<span data-ttu-id="6b3f1-134">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="6b3f1-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="6b3f1-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="6b3f1-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="6b3f1-136">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-136">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="6b3f1-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b3f1-137">-Name</span></span>
<span data-ttu-id="6b3f1-138">Anger namnet på den miljö som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-138">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="6b3f1-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="6b3f1-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="6b3f1-140">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="6b3f1-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b3f1-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="6b3f1-142">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-142">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="6b3f1-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b3f1-143">-ServiceEndpoint</span></span>
<span data-ttu-id="6b3f1-144">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="6b3f1-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="6b3f1-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="6b3f1-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="6b3f1-146">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="6b3f1-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b3f1-147">-StorageEndpoint</span></span>
<span data-ttu-id="6b3f1-148">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="6b3f1-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="6b3f1-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="6b3f1-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="6b3f1-150">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="6b3f1-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b3f1-151">-Confirm</span></span>
<span data-ttu-id="6b3f1-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3f1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3f1-153">-WhatIf</span></span>
<span data-ttu-id="6b3f1-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b3f1-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b3f1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3f1-156">CommonParameters</span></span>
<span data-ttu-id="6b3f1-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3f1-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b3f1-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3f1-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b3f1-159">INPUTS</span></span>

## <span data-ttu-id="6b3f1-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b3f1-160">OUTPUTS</span></span>

### <span data-ttu-id="6b3f1-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6b3f1-161">PSAzureEnvironment</span></span>
<span data-ttu-id="6b3f1-162">Denna cmdlet returnerar den uppsättning slut punkter och metadata som behövs för att kommunicera med en instans av Azure.</span><span class="sxs-lookup"><span data-stu-id="6b3f1-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="6b3f1-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b3f1-163">NOTES</span></span>

## <span data-ttu-id="6b3f1-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b3f1-164">RELATED LINKS</span></span>

[<span data-ttu-id="6b3f1-165">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="6b3f1-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="6b3f1-166">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="6b3f1-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="6b3f1-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="6b3f1-167">Set-AzureRMEnvironment</span></span>]()

