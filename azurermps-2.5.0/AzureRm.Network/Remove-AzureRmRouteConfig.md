---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: c5117fc961a93395991055eff2d404b5b8c6c051
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931201"
---
# <span data-ttu-id="12324-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="12324-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="12324-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12324-102">SYNOPSIS</span></span>
<span data-ttu-id="12324-103">Tar bort en väg från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="12324-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12324-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12324-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12324-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12324-105">DESCRIPTION</span></span>
<span data-ttu-id="12324-106">Cmdleten **Remove-AzureRmRouteConfig** tar bort en väg från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="12324-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="12324-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12324-107">EXAMPLES</span></span>

### <span data-ttu-id="12324-108">Exempel 1: ta bort en väg</span><span class="sxs-lookup"><span data-stu-id="12324-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="12324-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="12324-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="12324-110">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="12324-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="12324-111">Den aktuella cmdleten tar bort vägen med namnet Route02 och skickar resultatet till cmdleten **set-AzureRmRouteTable** , som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="12324-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="12324-112">Tabellen innehåller inte längre vägen med namnet Route02.</span><span class="sxs-lookup"><span data-stu-id="12324-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="12324-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12324-113">PARAMETERS</span></span>

### <span data-ttu-id="12324-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12324-114">-DefaultProfile</span></span>
<span data-ttu-id="12324-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12324-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12324-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="12324-116">-Name</span></span>
<span data-ttu-id="12324-117">Anger namnet på den väg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="12324-117">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12324-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="12324-118">-RouteTable</span></span>
<span data-ttu-id="12324-119">Anger den routningstabell som innehåller vägen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12324-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12324-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12324-120">-Confirm</span></span>
<span data-ttu-id="12324-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12324-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12324-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12324-122">-WhatIf</span></span>
<span data-ttu-id="12324-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12324-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12324-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12324-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12324-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12324-125">CommonParameters</span></span>
<span data-ttu-id="12324-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12324-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12324-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12324-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12324-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12324-128">INPUTS</span></span>

### <span data-ttu-id="12324-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="12324-129">PSRouteTable</span></span>
<span data-ttu-id="12324-130">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="12324-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="12324-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12324-131">OUTPUTS</span></span>

### <span data-ttu-id="12324-132">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="12324-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="12324-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12324-133">NOTES</span></span>

## <span data-ttu-id="12324-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12324-134">RELATED LINKS</span></span>

[<span data-ttu-id="12324-135">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="12324-135">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="12324-136">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="12324-136">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="12324-137">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="12324-137">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="12324-138">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="12324-138">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


