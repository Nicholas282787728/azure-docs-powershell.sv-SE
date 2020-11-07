---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756164"
---
# <span data-ttu-id="4a00d-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="4a00d-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="4a00d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a00d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a00d-103">Få belastnings utjämning på främre dörren</span><span class="sxs-lookup"><span data-stu-id="4a00d-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a00d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a00d-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a00d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a00d-105">DESCRIPTION</span></span>
<span data-ttu-id="4a00d-106">Med **Get-AzureRmFrontDoor** cmdletGet får du alla befintliga front dörrar i det aktuella abonnemanget som innehåller information.</span><span class="sxs-lookup"><span data-stu-id="4a00d-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="4a00d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a00d-107">EXAMPLES</span></span>

### <span data-ttu-id="4a00d-108">Exempel 1: Hämta alla FrontDoors i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a00d-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="4a00d-109">Skaffa alla FrontDoors i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a00d-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="4a00d-110">Exempel 2: Hämta alla FrontDoors i resurs gruppen "RG1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a00d-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="4a00d-111">Hämta alla FrontDoors i resurs gruppen "RG1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a00d-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="4a00d-112">Exempel 3: Hämta FrontDoors i resurs gruppen "RG1" med namnet "frontDoor1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a00d-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="4a00d-113">Hämta FrontDoors i resurs gruppen "RG1" med namnet "frontDoor1" i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a00d-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="4a00d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a00d-114">PARAMETERS</span></span>

### <span data-ttu-id="4a00d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a00d-115">-DefaultProfile</span></span>
<span data-ttu-id="4a00d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a00d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a00d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a00d-117">-Name</span></span>
<span data-ttu-id="4a00d-118">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="4a00d-118">Front Door name.</span></span>

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

### <span data-ttu-id="4a00d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a00d-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a00d-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4a00d-120">The resource group name.</span></span>

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

### <span data-ttu-id="4a00d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a00d-121">CommonParameters</span></span>
<span data-ttu-id="4a00d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a00d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a00d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a00d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a00d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a00d-124">INPUTS</span></span>

### <span data-ttu-id="4a00d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4a00d-125">System.String</span></span>

## <span data-ttu-id="4a00d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a00d-126">OUTPUTS</span></span>

### <span data-ttu-id="4a00d-127">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="4a00d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="4a00d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a00d-128">NOTES</span></span>

## <span data-ttu-id="4a00d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a00d-129">RELATED LINKS</span></span>

<span data-ttu-id="4a00d-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="4a00d-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
