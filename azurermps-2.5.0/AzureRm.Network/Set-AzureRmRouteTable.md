---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 198b14e4aab131b3d6044c793c5f3a4ea030b322
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930873"
---
# <span data-ttu-id="76a92-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="76a92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76a92-102">SYNOPSIS</span></span>
<span data-ttu-id="76a92-103">Anger mål tillstånd för en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="76a92-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76a92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76a92-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a92-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76a92-105">DESCRIPTION</span></span>
<span data-ttu-id="76a92-106">Cmdleten **set-AzureRmRouteTable** anger mål tillståndet för en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="76a92-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="76a92-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76a92-107">EXAMPLES</span></span>

### <span data-ttu-id="76a92-108">Exempel 1: lägga till en väg och ange mål tillstånd för routningstabellen</span><span class="sxs-lookup"><span data-stu-id="76a92-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="76a92-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av Get-AzureRmRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a92-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="76a92-110">Kommandot skickar den tabellen till Add-AzureRmRouteConfig cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="76a92-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76a92-111">**Add-AzureRmRouteConfig** lägger till vägen med namnet Route07 och skickar sedan resultatet till den aktuella cmdleten, vilket uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="76a92-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="76a92-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76a92-112">PARAMETERS</span></span>

### <span data-ttu-id="76a92-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76a92-113">-AsJob</span></span>
<span data-ttu-id="76a92-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="76a92-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a92-115">-DefaultProfile</span></span>
<span data-ttu-id="76a92-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76a92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-117">-RouteTable</span></span>
<span data-ttu-id="76a92-118">Anger ett väg tabell objekt som representerar det mål tillstånd där denna cmdlet ställer in väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="76a92-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76a92-119">-Confirm</span></span>
<span data-ttu-id="76a92-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76a92-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a92-121">-WhatIf</span></span>
<span data-ttu-id="76a92-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76a92-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76a92-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76a92-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a92-124">CommonParameters</span></span>
<span data-ttu-id="76a92-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a92-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a92-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a92-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76a92-127">INPUTS</span></span>

### <span data-ttu-id="76a92-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-128">PSRouteTable</span></span>
<span data-ttu-id="76a92-129">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="76a92-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="76a92-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76a92-130">OUTPUTS</span></span>

### <span data-ttu-id="76a92-131">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="76a92-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76a92-132">NOTES</span></span>

## <span data-ttu-id="76a92-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76a92-133">RELATED LINKS</span></span>

[<span data-ttu-id="76a92-134">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76a92-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="76a92-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="76a92-136">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="76a92-137">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="76a92-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

