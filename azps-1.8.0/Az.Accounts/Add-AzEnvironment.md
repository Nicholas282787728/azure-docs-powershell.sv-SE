---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 47f57068af722bd9f34826176d2a31cdfd9843a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743549"
---
# <span data-ttu-id="7cd87-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7cd87-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="7cd87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cd87-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd87-103">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7cd87-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="7cd87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cd87-104">SYNTAX</span></span>

### <span data-ttu-id="7cd87-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="7cd87-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd87-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cd87-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cd87-107">DESCRIPTION</span></span>
<span data-ttu-id="7cd87-108">Add-AzEnvironment cmdlet lägger till slut punkter och metadata för att aktivera Azure Resource Manager-cmdlets för att ansluta till en ny instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7cd87-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="7cd87-109">De inbyggda miljöerna AzureCloud och AzureChinaCloud är befintliga offentliga instanser av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7cd87-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="7cd87-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cd87-110">EXAMPLES</span></span>

### <span data-ttu-id="7cd87-111">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="7cd87-111">Example 1: Creating and modifying a new environment</span></span>
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="7cd87-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cd87-112">PARAMETERS</span></span>

### <span data-ttu-id="7cd87-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="7cd87-114">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="7cd87-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="7cd87-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd87-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="7cd87-116">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="7cd87-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="7cd87-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="7cd87-117">-AdTenant</span></span>
<span data-ttu-id="7cd87-118">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7cd87-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="7cd87-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-119">-ARMEndpoint</span></span>
<span data-ttu-id="7cd87-120">Azure Resource Manager slut punkt</span><span class="sxs-lookup"><span data-stu-id="7cd87-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="7cd87-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd87-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="7cd87-122">Resurs-ID för Azure Analysis Services-resursen.</span><span class="sxs-lookup"><span data-stu-id="7cd87-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd87-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7cd87-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="7cd87-124">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="7cd87-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd87-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7cd87-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="7cd87-126">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="7cd87-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="7cd87-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7cd87-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="7cd87-128">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="7cd87-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="7cd87-129">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="7cd87-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="7cd87-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7cd87-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="7cd87-131">DNS-suffix för Azure Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7cd87-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="7cd87-132">Exempel är vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="7cd87-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="7cd87-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd87-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="7cd87-134">Resurs-ID för Azure Key Vault data-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="7cd87-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="7cd87-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="7cd87-136">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="7cd87-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="7cd87-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd87-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="7cd87-138">Mål gruppen för tokens som autentiserar med Azure logganalys-API: t.</span><span class="sxs-lookup"><span data-stu-id="7cd87-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="7cd87-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd87-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="7cd87-140">Resurs-ID för Azure Batch-tjänsten som är mottagaren av den begärda token</span><span class="sxs-lookup"><span data-stu-id="7cd87-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="7cd87-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="7cd87-141">-DataLakeAudience</span></span>
<span data-ttu-id="7cd87-142">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="7cd87-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="7cd87-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd87-143">-DefaultProfile</span></span>
<span data-ttu-id="7cd87-144">Credeetnails, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7cd87-144">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cd87-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="7cd87-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="7cd87-146">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="7cd87-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="7cd87-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-147">-GalleryEndpoint</span></span>
<span data-ttu-id="7cd87-148">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="7cd87-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="7cd87-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="7cd87-149">-GraphAudience</span></span>
<span data-ttu-id="7cd87-150">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="7cd87-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="7cd87-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-151">-GraphEndpoint</span></span>
<span data-ttu-id="7cd87-152">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="7cd87-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="7cd87-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="7cd87-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="7cd87-154">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="7cd87-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="7cd87-155">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cd87-155">-Name</span></span>
<span data-ttu-id="7cd87-156">Anger namnet på den miljö som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="7cd87-156">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="7cd87-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="7cd87-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="7cd87-158">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="7cd87-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="7cd87-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="7cd87-160">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="7cd87-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="7cd87-161">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="7cd87-161">-Scope</span></span>
<span data-ttu-id="7cd87-162">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="7cd87-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="7cd87-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-163">-ServiceEndpoint</span></span>
<span data-ttu-id="7cd87-164">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="7cd87-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="7cd87-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7cd87-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="7cd87-166">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="7cd87-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="7cd87-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cd87-167">-StorageEndpoint</span></span>
<span data-ttu-id="7cd87-168">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="7cd87-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="7cd87-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7cd87-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="7cd87-170">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="7cd87-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="7cd87-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cd87-171">-Confirm</span></span>
<span data-ttu-id="7cd87-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cd87-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd87-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd87-173">-WhatIf</span></span>
<span data-ttu-id="7cd87-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cd87-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cd87-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cd87-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd87-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd87-176">CommonParameters</span></span>
<span data-ttu-id="7cd87-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd87-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd87-178">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd87-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd87-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cd87-179">INPUTS</span></span>

### <span data-ttu-id="7cd87-180">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd87-180">System.String</span></span>

### <span data-ttu-id="7cd87-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cd87-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7cd87-182">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cd87-182">OUTPUTS</span></span>

### <span data-ttu-id="7cd87-183">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7cd87-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="7cd87-184">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cd87-184">NOTES</span></span>

## <span data-ttu-id="7cd87-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cd87-185">RELATED LINKS</span></span>

[<span data-ttu-id="7cd87-186">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7cd87-186">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="7cd87-187">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7cd87-187">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="7cd87-188">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7cd87-188">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

