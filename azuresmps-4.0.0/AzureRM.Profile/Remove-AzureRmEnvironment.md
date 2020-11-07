---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754980"
---
# <span data-ttu-id="bb5f5-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb5f5-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="bb5f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5f5-103">Tar bort slut punkter och metadata för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="bb5f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb5f5-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb5f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb5f5-105">DESCRIPTION</span></span>
<span data-ttu-id="bb5f5-106">Remove-AzureRmEnvironment cmdlet tar bort slut punkter och metadatainformation för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="bb5f5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb5f5-107">EXAMPLES</span></span>

### <span data-ttu-id="bb5f5-108">Exempel 1: skapa och ta bort en test miljö</span><span class="sxs-lookup"><span data-stu-id="bb5f5-108">Example 1: Creating and removing a test environment</span></span>
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

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

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
```

<span data-ttu-id="bb5f5-109">Det här exemplet visar hur du skapar en miljö med Add-AzureRmEnvironment och hur du tar bort miljön med Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="bb5f5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb5f5-110">PARAMETERS</span></span>

### <span data-ttu-id="bb5f5-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb5f5-111">-Name</span></span>
<span data-ttu-id="bb5f5-112">Anger namnet på den miljö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-112">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="bb5f5-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb5f5-113">-Confirm</span></span>
<span data-ttu-id="bb5f5-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb5f5-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb5f5-115">-WhatIf</span></span>
<span data-ttu-id="bb5f5-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb5f5-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb5f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5f5-118">CommonParameters</span></span>
<span data-ttu-id="bb5f5-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb5f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5f5-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5f5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5f5-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb5f5-121">INPUTS</span></span>

## <span data-ttu-id="bb5f5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb5f5-122">OUTPUTS</span></span>

### <span data-ttu-id="bb5f5-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb5f5-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="bb5f5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb5f5-124">NOTES</span></span>

## <span data-ttu-id="bb5f5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb5f5-125">RELATED LINKS</span></span>

[<span data-ttu-id="bb5f5-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb5f5-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="bb5f5-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb5f5-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="bb5f5-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb5f5-128">Set-AzureRMEnvironment</span></span>]()

