---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: d27a05e652cbcd11d35536ebff97f04b3c60f520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758032"
---
# <span data-ttu-id="c3608-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3608-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="c3608-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3608-102">SYNOPSIS</span></span>
<span data-ttu-id="c3608-103">Tar bort slut punkter och metadata för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="c3608-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3608-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3608-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3608-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3608-105">DESCRIPTION</span></span>
<span data-ttu-id="c3608-106">Remove-AzureRmEnvironment cmdlet tar bort slut punkter och metadatainformation för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="c3608-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="c3608-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3608-107">EXAMPLES</span></span>

### <span data-ttu-id="c3608-108">Exempel 1: skapa och ta bort en test miljö</span><span class="sxs-lookup"><span data-stu-id="c3608-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="c3608-109">Det här exemplet visar hur du skapar en miljö med Add-AzureRmEnvironment och hur du tar bort miljön med Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="c3608-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="c3608-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3608-110">PARAMETERS</span></span>

### <span data-ttu-id="c3608-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3608-111">-DefaultProfile</span></span>
<span data-ttu-id="c3608-112">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3608-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3608-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3608-113">-Name</span></span>
<span data-ttu-id="c3608-114">Anger namnet på den miljö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c3608-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="c3608-115">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c3608-115">-Scope</span></span>
<span data-ttu-id="c3608-116">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="c3608-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c3608-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3608-117">-Confirm</span></span>
<span data-ttu-id="c3608-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3608-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3608-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3608-119">-WhatIf</span></span>
<span data-ttu-id="c3608-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3608-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3608-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3608-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3608-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3608-122">CommonParameters</span></span>
<span data-ttu-id="c3608-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3608-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3608-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3608-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3608-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3608-125">INPUTS</span></span>

## <span data-ttu-id="c3608-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3608-126">OUTPUTS</span></span>

### <span data-ttu-id="c3608-127">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3608-127">PSAzureEnvironment</span></span>

## <span data-ttu-id="c3608-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3608-128">NOTES</span></span>

## <span data-ttu-id="c3608-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3608-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3608-130">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3608-130">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="c3608-131">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3608-131">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="c3608-132">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3608-132">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

