---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756162"
---
# <span data-ttu-id="bb698-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="bb698-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="bb698-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb698-102">SYNOPSIS</span></span>
<span data-ttu-id="bb698-103">Skapa ett PSBackendPool-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="bb698-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb698-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb698-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb698-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb698-105">DESCRIPTION</span></span>
<span data-ttu-id="bb698-106">Skapa ett PSBackendPool-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="bb698-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="bb698-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb698-107">EXAMPLES</span></span>

### <span data-ttu-id="bb698-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bb698-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="bb698-109">Skapa ett PSBackendPool-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="bb698-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="bb698-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb698-110">PARAMETERS</span></span>

### <span data-ttu-id="bb698-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="bb698-111">-Backend</span></span>
<span data-ttu-id="bb698-112">Uppsättningen av bakände för denna pool.</span><span class="sxs-lookup"><span data-stu-id="bb698-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="bb698-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb698-113">-DefaultProfile</span></span>
<span data-ttu-id="bb698-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb698-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb698-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="bb698-115">-FrontDoorName</span></span>
<span data-ttu-id="bb698-116">Namnet på den främre dörren som den här regeln tillhör.</span><span class="sxs-lookup"><span data-stu-id="bb698-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="bb698-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="bb698-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="bb698-118">Namn på Inställningar för hälso avsökning för den här backend-poolen</span><span class="sxs-lookup"><span data-stu-id="bb698-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="bb698-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="bb698-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="bb698-120">Namn på Inställningar för belastnings utjämning för den här backend-poolen</span><span class="sxs-lookup"><span data-stu-id="bb698-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="bb698-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb698-121">-Name</span></span>
<span data-ttu-id="bb698-122">BackendPool namn.</span><span class="sxs-lookup"><span data-stu-id="bb698-122">BackendPool name.</span></span>

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

### <span data-ttu-id="bb698-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb698-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb698-124">Namnet på resurs gruppen som RoutingRule skapas i.</span><span class="sxs-lookup"><span data-stu-id="bb698-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="bb698-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb698-125">CommonParameters</span></span>
<span data-ttu-id="bb698-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb698-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb698-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb698-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb698-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb698-128">INPUTS</span></span>

### <span data-ttu-id="bb698-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="bb698-129">None</span></span>

## <span data-ttu-id="bb698-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb698-130">OUTPUTS</span></span>

### <span data-ttu-id="bb698-131">Microsoft. Azure. commands. FrontDoor. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="bb698-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="bb698-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb698-132">NOTES</span></span>

## <span data-ttu-id="bb698-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb698-133">RELATED LINKS</span></span>

<span data-ttu-id="bb698-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="bb698-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
