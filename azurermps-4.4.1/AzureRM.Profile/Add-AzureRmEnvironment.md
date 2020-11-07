---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757768"
---
# <span data-ttu-id="be991-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="be991-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="be991-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be991-102">SYNOPSIS</span></span>
<span data-ttu-id="be991-103">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="be991-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be991-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be991-104">SYNTAX</span></span>

### <span data-ttu-id="be991-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="be991-105">Name (Default)</span></span>
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
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be991-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be991-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be991-107">DESCRIPTION</span></span>
<span data-ttu-id="be991-108">Add-AzureRmEnvironment cmdlet lägger till slut punkter och metadata för att aktivera Azure Resource Manager-cmdlets för att ansluta till en ny instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="be991-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="be991-109">De inbyggda miljöerna AzureCloud och AzureChinaCloud är befintliga offentliga instanser av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="be991-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="be991-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be991-110">EXAMPLES</span></span>

### <span data-ttu-id="be991-111">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="be991-111">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="be991-112">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzureRmEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="be991-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="be991-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be991-113">PARAMETERS</span></span>

### <span data-ttu-id="be991-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="be991-115">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="be991-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="be991-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="be991-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="be991-117">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="be991-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="be991-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="be991-118">-AdTenant</span></span>
<span data-ttu-id="be991-119">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be991-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="be991-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-120">-ARMEndpoint</span></span>
<span data-ttu-id="be991-121">Azure Resource Manager slut punkt</span><span class="sxs-lookup"><span data-stu-id="be991-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="be991-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="be991-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="be991-123">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="be991-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="be991-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="be991-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="be991-125">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="be991-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="be991-126">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="be991-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="be991-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="be991-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="be991-128">Anger domän namn för viktiga valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="be991-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="be991-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="be991-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="be991-130">Anger mål gruppen för de åtkomsttoken som tillåter begäran om nyckel valv tjänster.</span><span class="sxs-lookup"><span data-stu-id="be991-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be991-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="be991-131">-DataLakeAudience</span></span>
<span data-ttu-id="be991-132">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="be991-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="be991-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be991-133">-DefaultProfile</span></span>
<span data-ttu-id="be991-134">Credeetnails, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="be991-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be991-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="be991-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="be991-136">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="be991-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="be991-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-137">-GalleryEndpoint</span></span>
<span data-ttu-id="be991-138">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="be991-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="be991-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="be991-139">-GraphAudience</span></span>
<span data-ttu-id="be991-140">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="be991-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="be991-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-141">-GraphEndpoint</span></span>
<span data-ttu-id="be991-142">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="be991-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="be991-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="be991-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="be991-144">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="be991-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="be991-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="be991-145">-Name</span></span>
<span data-ttu-id="be991-146">Anger namnet på den miljö som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="be991-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="be991-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="be991-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="be991-148">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="be991-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="be991-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="be991-150">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="be991-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="be991-151">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="be991-151">-Scope</span></span>
<span data-ttu-id="be991-152">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="be991-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="be991-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-153">-ServiceEndpoint</span></span>
<span data-ttu-id="be991-154">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="be991-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="be991-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="be991-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="be991-156">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="be991-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="be991-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="be991-157">-StorageEndpoint</span></span>
<span data-ttu-id="be991-158">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="be991-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="be991-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="be991-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="be991-160">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="be991-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="be991-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be991-161">-Confirm</span></span>
<span data-ttu-id="be991-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be991-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be991-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be991-163">-WhatIf</span></span>
<span data-ttu-id="be991-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be991-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be991-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="be991-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be991-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be991-166">CommonParameters</span></span>
<span data-ttu-id="be991-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be991-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be991-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be991-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be991-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be991-169">INPUTS</span></span>

## <span data-ttu-id="be991-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be991-170">OUTPUTS</span></span>

### <span data-ttu-id="be991-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="be991-171">PSAzureEnvironment</span></span>
<span data-ttu-id="be991-172">Denna cmdlet returnerar den uppsättning slut punkter och metadata som behövs för att kommunicera med en instans av Azure.</span><span class="sxs-lookup"><span data-stu-id="be991-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="be991-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be991-173">NOTES</span></span>

## <span data-ttu-id="be991-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be991-174">RELATED LINKS</span></span>

[<span data-ttu-id="be991-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="be991-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="be991-176">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="be991-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="be991-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="be991-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

