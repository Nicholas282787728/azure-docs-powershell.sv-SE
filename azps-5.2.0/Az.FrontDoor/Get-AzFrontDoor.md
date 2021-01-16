---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407368"
---
# <span data-ttu-id="fe938-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe938-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="fe938-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe938-102">SYNOPSIS</span></span>
<span data-ttu-id="fe938-103">Få belastnings utjämning på främre dörren</span><span class="sxs-lookup"><span data-stu-id="fe938-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="fe938-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe938-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe938-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe938-105">DESCRIPTION</span></span>
<span data-ttu-id="fe938-106">Med **Get-AzFrontDoor** cmdletGet får du alla befintliga front dörrar i det aktuella abonnemanget som innehåller information.</span><span class="sxs-lookup"><span data-stu-id="fe938-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="fe938-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe938-107">EXAMPLES</span></span>

### <span data-ttu-id="fe938-108">Exempel 1: Hämta alla FrontDoors i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe938-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
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

<span data-ttu-id="fe938-109">Skaffa alla FrontDoors i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe938-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="fe938-110">Exempel 2: Hämta alla FrontDoors i resurs gruppen "RG1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe938-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
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

<span data-ttu-id="fe938-111">Hämta alla FrontDoors i resurs gruppen "RG1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe938-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="fe938-112">Exempel 3: Hämta FrontDoors i resurs gruppen "RG1" med namnet "frontDoor1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe938-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
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

<span data-ttu-id="fe938-113">Hämta FrontDoors i resurs gruppen "RG1" med namnet "frontDoor1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fe938-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="fe938-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe938-114">PARAMETERS</span></span>

### <span data-ttu-id="fe938-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe938-115">-DefaultProfile</span></span>
<span data-ttu-id="fe938-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe938-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe938-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe938-117">-Name</span></span>
<span data-ttu-id="fe938-118">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="fe938-118">Front Door name.</span></span>

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

### <span data-ttu-id="fe938-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe938-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe938-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fe938-120">The resource group name.</span></span>

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

### <span data-ttu-id="fe938-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe938-121">CommonParameters</span></span>
<span data-ttu-id="fe938-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe938-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe938-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe938-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe938-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe938-124">INPUTS</span></span>

### <span data-ttu-id="fe938-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="fe938-125">None</span></span>

## <span data-ttu-id="fe938-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe938-126">OUTPUTS</span></span>

### <span data-ttu-id="fe938-127">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="fe938-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="fe938-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe938-128">NOTES</span></span>

## <span data-ttu-id="fe938-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe938-129">RELATED LINKS</span></span>

<span data-ttu-id="fe938-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="fe938-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
