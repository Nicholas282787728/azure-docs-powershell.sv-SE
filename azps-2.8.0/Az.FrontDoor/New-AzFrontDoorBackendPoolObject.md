---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 32af04aec91302304be3ed11c17d81d2e71cc772
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744151"
---
# <span data-ttu-id="98d09-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="98d09-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="98d09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98d09-102">SYNOPSIS</span></span>
<span data-ttu-id="98d09-103">Skapa ett PSBackendPool-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="98d09-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="98d09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98d09-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d09-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98d09-105">DESCRIPTION</span></span>
<span data-ttu-id="98d09-106">Skapa ett PSBackendPool-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="98d09-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="98d09-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98d09-107">EXAMPLES</span></span>

### <span data-ttu-id="98d09-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98d09-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="98d09-109">Skapa ett PSBackendPool-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="98d09-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="98d09-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98d09-110">PARAMETERS</span></span>

### <span data-ttu-id="98d09-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="98d09-111">-Backend</span></span>
<span data-ttu-id="98d09-112">Uppsättningen av bakände för denna pool.</span><span class="sxs-lookup"><span data-stu-id="98d09-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d09-113">-DefaultProfile</span></span>
<span data-ttu-id="98d09-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98d09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98d09-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="98d09-115">-FrontDoorName</span></span>
<span data-ttu-id="98d09-116">Namnet på den främre dörren som den här regeln tillhör.</span><span class="sxs-lookup"><span data-stu-id="98d09-116">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d09-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="98d09-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="98d09-118">Namn på Inställningar för hälso avsökning för den här backend-poolen</span><span class="sxs-lookup"><span data-stu-id="98d09-118">The name of the health probe settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d09-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="98d09-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="98d09-120">Namn på Inställningar för belastnings utjämning för den här backend-poolen</span><span class="sxs-lookup"><span data-stu-id="98d09-120">The name of the load balancing settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d09-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="98d09-121">-Name</span></span>
<span data-ttu-id="98d09-122">BackendPool namn.</span><span class="sxs-lookup"><span data-stu-id="98d09-122">BackendPool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d09-123">-ResourceGroupName</span></span>
<span data-ttu-id="98d09-124">Namnet på resurs gruppen som RoutingRule skapas i.</span><span class="sxs-lookup"><span data-stu-id="98d09-124">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d09-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d09-125">CommonParameters</span></span>
<span data-ttu-id="98d09-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d09-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d09-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98d09-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d09-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98d09-128">INPUTS</span></span>

### <span data-ttu-id="98d09-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="98d09-129">None</span></span>

## <span data-ttu-id="98d09-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98d09-130">OUTPUTS</span></span>

### <span data-ttu-id="98d09-131">Microsoft. Azure. commands. FrontDoor. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="98d09-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="98d09-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98d09-132">NOTES</span></span>

## <span data-ttu-id="98d09-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98d09-133">RELATED LINKS</span></span>

<span data-ttu-id="98d09-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="98d09-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
