---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 5ede64a5efaa5e44b5de5551bde4d17730b910b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089712"
---
# <span data-ttu-id="1d81a-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d81a-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="1d81a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d81a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d81a-103">Anger egenskaper för en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="1d81a-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="1d81a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d81a-104">SYNTAX</span></span>

### <span data-ttu-id="1d81a-105">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="1d81a-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d81a-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d81a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d81a-107">DESCRIPTION</span></span>
<span data-ttu-id="1d81a-108">Med Set-AzEnvironment cmdlet anges slut punkter och metadata för anslutning till en instans av Azure.</span><span class="sxs-lookup"><span data-stu-id="1d81a-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="1d81a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d81a-109">EXAMPLES</span></span>

### <span data-ttu-id="1d81a-110">Exempel 1: skapa och ändra en ny miljö</span><span class="sxs-lookup"><span data-stu-id="1d81a-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

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
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
```

<span data-ttu-id="1d81a-111">I det här exemplet skapar vi en ny Azure-miljö med exempel slut punkter med Add-AzEnvironment och sedan ändrar vi värdet för attributen ActiveDirectoryEndpoint och GraphEndpoint för den skapade miljön med cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="1d81a-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="1d81a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d81a-112">PARAMETERS</span></span>

### <span data-ttu-id="1d81a-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="1d81a-114">Anger bas auktoritet för Azure Active Directory-verifikation.</span><span class="sxs-lookup"><span data-stu-id="1d81a-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="1d81a-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1d81a-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="1d81a-116">Anger mål gruppen för tokens som autentiserar förfrågningar till slut punkter för Azure Resource Manager eller tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="1d81a-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="1d81a-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="1d81a-117">-AdTenant</span></span>
<span data-ttu-id="1d81a-118">Anger standard klient organisation för Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1d81a-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="1d81a-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-119">-ARMEndpoint</span></span>
<span data-ttu-id="1d81a-120">Slut punkten för Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1d81a-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="1d81a-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1d81a-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="1d81a-122">Resurs-ID för Azure Analysis Services-resursen.</span><span class="sxs-lookup"><span data-stu-id="1d81a-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="1d81a-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="1d81a-124">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="1d81a-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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
### <span data-ttu-id="1d81a-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1d81a-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="1d81a-126">Resurs-ID för Azure attestering-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="1d81a-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="1d81a-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="1d81a-128">DNS-suffix för Azure attestering-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1d81a-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="1d81a-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="1d81a-130">DNS-suffix för Azure Data Lake Analytics-jobb och katalog tjänster</span><span class="sxs-lookup"><span data-stu-id="1d81a-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="1d81a-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="1d81a-132">DNS-suffix för Azure Data Lake Store-filsystem.</span><span class="sxs-lookup"><span data-stu-id="1d81a-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="1d81a-133">Exempel: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="1d81a-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="1d81a-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="1d81a-135">DNS-suffix för Azure Key valv-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1d81a-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="1d81a-136">Exempel är vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="1d81a-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="1d81a-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1d81a-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="1d81a-138">Resurs-ID för Azure Key Vault data-tjänsten som är mottagaren av den begärda token.</span><span class="sxs-lookup"><span data-stu-id="1d81a-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="1d81a-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="1d81a-140">Slut punkten som används vid kommunikation med Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="1d81a-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="1d81a-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1d81a-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="1d81a-142">Mål gruppen för tokens som autentiserar med Azure logganalys-API: t.</span><span class="sxs-lookup"><span data-stu-id="1d81a-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="1d81a-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1d81a-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="1d81a-144">Resurs-ID för Azure Batch-tjänsten som är mottagaren av den begärda token</span><span class="sxs-lookup"><span data-stu-id="1d81a-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="1d81a-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="1d81a-145">-DataLakeAudience</span></span>
<span data-ttu-id="1d81a-146">Mål gruppen för tokens som autentiserar med slut punkten för AD Lake-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="1d81a-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="1d81a-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d81a-147">-DefaultProfile</span></span>
<span data-ttu-id="1d81a-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d81a-148">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d81a-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="1d81a-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="1d81a-150">Anger att Active Directory Federation Services (AD FS) on-plats tillåts.</span><span class="sxs-lookup"><span data-stu-id="1d81a-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="1d81a-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-151">-GalleryEndpoint</span></span>
<span data-ttu-id="1d81a-152">Anger slut punkten för Azure Resource Manager-galleriet med mallar för distribuering.</span><span class="sxs-lookup"><span data-stu-id="1d81a-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="1d81a-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="1d81a-153">-GraphAudience</span></span>
<span data-ttu-id="1d81a-154">Mål gruppen för tokens som autentiseras med slut punkten för annons diagrammet.</span><span class="sxs-lookup"><span data-stu-id="1d81a-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="1d81a-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-155">-GraphEndpoint</span></span>
<span data-ttu-id="1d81a-156">Anger URL-adressen för diagrammet (Active Directory-metadata).</span><span class="sxs-lookup"><span data-stu-id="1d81a-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="1d81a-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="1d81a-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="1d81a-158">Anger URL-adressen för hanterings portalen.</span><span class="sxs-lookup"><span data-stu-id="1d81a-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="1d81a-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d81a-159">-Name</span></span>
<span data-ttu-id="1d81a-160">Anger namnet på den miljö som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="1d81a-160">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="1d81a-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="1d81a-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="1d81a-162">Anger URL-adressen dit. publishsettings-filer kan hämtas.</span><span class="sxs-lookup"><span data-stu-id="1d81a-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="1d81a-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="1d81a-164">Anger URL-adressen för Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="1d81a-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="1d81a-165">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="1d81a-165">-Scope</span></span>
<span data-ttu-id="1d81a-166">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="1d81a-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="1d81a-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-167">-ServiceEndpoint</span></span>
<span data-ttu-id="1d81a-168">Anger sändnings begär Anden för tjänste hantering (RDFE).</span><span class="sxs-lookup"><span data-stu-id="1d81a-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="1d81a-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="1d81a-170">Anger domänsuffix för domän namn för Azure SQL Database-servrar.</span><span class="sxs-lookup"><span data-stu-id="1d81a-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="1d81a-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d81a-171">-StorageEndpoint</span></span>
<span data-ttu-id="1d81a-172">Anger slut punkt för lagring (BLOB, tabell, kö och fil).</span><span class="sxs-lookup"><span data-stu-id="1d81a-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="1d81a-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1d81a-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="1d81a-174">Anger domänsuffix för Azure Traffic Manager-tjänster.</span><span class="sxs-lookup"><span data-stu-id="1d81a-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="1d81a-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d81a-175">-Confirm</span></span>
<span data-ttu-id="1d81a-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d81a-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d81a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d81a-177">-WhatIf</span></span>
<span data-ttu-id="1d81a-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d81a-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d81a-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d81a-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d81a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d81a-180">CommonParameters</span></span>
<span data-ttu-id="1d81a-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d81a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d81a-182">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d81a-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d81a-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d81a-183">INPUTS</span></span>

### <span data-ttu-id="1d81a-184">System. String</span><span class="sxs-lookup"><span data-stu-id="1d81a-184">System.String</span></span>

### <span data-ttu-id="1d81a-185">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d81a-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d81a-186">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d81a-186">OUTPUTS</span></span>

### <span data-ttu-id="1d81a-187">Microsoft. Azure. commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d81a-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="1d81a-188">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d81a-188">NOTES</span></span>

## <span data-ttu-id="1d81a-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d81a-189">RELATED LINKS</span></span>

[<span data-ttu-id="1d81a-190">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d81a-190">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="1d81a-191">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d81a-191">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="1d81a-192">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d81a-192">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

