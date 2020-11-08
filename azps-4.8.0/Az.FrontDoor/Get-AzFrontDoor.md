---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101505"
---
# <span data-ttu-id="af4c2-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="af4c2-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="af4c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="af4c2-103">Få belastnings utjämning på främre dörren</span><span class="sxs-lookup"><span data-stu-id="af4c2-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="af4c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af4c2-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af4c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af4c2-105">DESCRIPTION</span></span>
<span data-ttu-id="af4c2-106">Med **Get-AzFrontDoor** cmdletGet får du alla befintliga front dörrar i det aktuella abonnemanget som innehåller information.</span><span class="sxs-lookup"><span data-stu-id="af4c2-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="af4c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af4c2-107">EXAMPLES</span></span>

### <span data-ttu-id="af4c2-108">Exempel 1: Hämta alla FrontDoors i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af4c2-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="af4c2-109">Skaffa alla FrontDoors i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af4c2-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="af4c2-110">Exempel 2: Hämta alla FrontDoors i resurs gruppen "RG1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af4c2-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="af4c2-111">Hämta alla FrontDoors i resurs gruppen "RG1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af4c2-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="af4c2-112">Exempel 3: Hämta FrontDoors i resurs gruppen "RG1" med namnet "frontDoor1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af4c2-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="af4c2-113">Hämta FrontDoors i resurs gruppen "RG1" med namnet "frontDoor1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="af4c2-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="af4c2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af4c2-114">PARAMETERS</span></span>

### <span data-ttu-id="af4c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4c2-115">-DefaultProfile</span></span>
<span data-ttu-id="af4c2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af4c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af4c2-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="af4c2-117">-Name</span></span>
<span data-ttu-id="af4c2-118">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="af4c2-118">Front Door name.</span></span>

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

### <span data-ttu-id="af4c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="af4c2-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="af4c2-120">The resource group name.</span></span>

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

### <span data-ttu-id="af4c2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4c2-121">CommonParameters</span></span>
<span data-ttu-id="af4c2-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af4c2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4c2-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af4c2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4c2-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af4c2-124">INPUTS</span></span>

### <span data-ttu-id="af4c2-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="af4c2-125">None</span></span>

## <span data-ttu-id="af4c2-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af4c2-126">OUTPUTS</span></span>

### <span data-ttu-id="af4c2-127">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="af4c2-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="af4c2-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af4c2-128">NOTES</span></span>

## <span data-ttu-id="af4c2-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af4c2-129">RELATED LINKS</span></span>

<span data-ttu-id="af4c2-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="af4c2-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
