---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422171"
---
# <span data-ttu-id="25a9f-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="25a9f-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="25a9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="25a9f-103">Hämta eller Visa en lista över virtuella nätverk enheter.</span><span class="sxs-lookup"><span data-stu-id="25a9f-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="25a9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25a9f-104">SYNTAX</span></span>

### <span data-ttu-id="25a9f-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="25a9f-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25a9f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25a9f-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25a9f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25a9f-107">DESCRIPTION</span></span>
<span data-ttu-id="25a9f-108">Get-AzNetworkVirtualAppliance kommandon hämtar eller visar resurser för virtuella nätverk enheter.</span><span class="sxs-lookup"><span data-stu-id="25a9f-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="25a9f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25a9f-109">EXAMPLES</span></span>

### <span data-ttu-id="25a9f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25a9f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="25a9f-111">Skaffa en resurs för virtuella nätverk enheter.</span><span class="sxs-lookup"><span data-stu-id="25a9f-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="25a9f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25a9f-112">PARAMETERS</span></span>

### <span data-ttu-id="25a9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a9f-113">-DefaultProfile</span></span>
<span data-ttu-id="25a9f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25a9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a9f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="25a9f-115">-Name</span></span>
<span data-ttu-id="25a9f-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="25a9f-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="25a9f-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="25a9f-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a9f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25a9f-119">-ResourceId</span></span>
<span data-ttu-id="25a9f-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="25a9f-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25a9f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a9f-121">CommonParameters</span></span>
<span data-ttu-id="25a9f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a9f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a9f-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25a9f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a9f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25a9f-124">INPUTS</span></span>

### <span data-ttu-id="25a9f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="25a9f-125">System.String</span></span>

## <span data-ttu-id="25a9f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25a9f-126">OUTPUTS</span></span>

### <span data-ttu-id="25a9f-127">Microsoft. Azure. commands. Networks. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="25a9f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="25a9f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25a9f-128">NOTES</span></span>

## <span data-ttu-id="25a9f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25a9f-129">RELATED LINKS</span></span>
