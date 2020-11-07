---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: ba8fc7809bc9cea8ea34dbc4d15816134e8d7e13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747694"
---
# <span data-ttu-id="76c1d-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="76c1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="76c1d-103">Uppdaterar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="76c1d-103">Updates a route table.</span></span>

## <span data-ttu-id="76c1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76c1d-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="76c1d-106">Cmdleten **set-AzRouteTable** uppdaterar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="76c1d-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="76c1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76c1d-107">EXAMPLES</span></span>

### <span data-ttu-id="76c1d-108">Exempel 1: uppdatera en routningstabell genom att lägga till väg konfiguration i den</span><span class="sxs-lookup"><span data-stu-id="76c1d-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
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

<span data-ttu-id="76c1d-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76c1d-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="76c1d-110">Kommandot skickar den tabellen till Add-AzRouteConfig cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="76c1d-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76c1d-111">**Add-AzRouteConfig** lägger till vägen med namnet Route07 och skickar sedan resultatet till den aktuella cmdleten, vilket uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="76c1d-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="76c1d-112">Exempel 2: ändra routningstabellen</span><span class="sxs-lookup"><span data-stu-id="76c1d-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="76c1d-113">Med det första kommandot hämtas routningstabellen med namnet rtName och lagras i variabeln $rt.</span><span class="sxs-lookup"><span data-stu-id="76c1d-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="76c1d-114">Det andra kommandot visar värdet för DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="76c1d-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="76c1d-115">Det tredje kommandot uppdaterar värdet för DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="76c1d-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="76c1d-116">Det fjärde kommandot uppdaterar routningstabellen på servern.</span><span class="sxs-lookup"><span data-stu-id="76c1d-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="76c1d-117">Det femte kommandot uppdaterar väg tabellen och lagrar den i $rt variabeln.</span><span class="sxs-lookup"><span data-stu-id="76c1d-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="76c1d-118">Det sjätte kommandot visar värdet för DisableBgpRoutePropagation.</span><span class="sxs-lookup"><span data-stu-id="76c1d-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="76c1d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76c1d-119">PARAMETERS</span></span>

### <span data-ttu-id="76c1d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76c1d-120">-AsJob</span></span>
<span data-ttu-id="76c1d-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="76c1d-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c1d-122">-DefaultProfile</span></span>
<span data-ttu-id="76c1d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76c1d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c1d-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-124">-RouteTable</span></span>
<span data-ttu-id="76c1d-125">Anger ett väg tabell objekt som representerar tillståndet som väg tabellen ska anges i.</span><span class="sxs-lookup"><span data-stu-id="76c1d-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76c1d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76c1d-126">-Confirm</span></span>
<span data-ttu-id="76c1d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76c1d-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c1d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c1d-128">-WhatIf</span></span>
<span data-ttu-id="76c1d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76c1d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76c1d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76c1d-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c1d-131">CommonParameters</span></span>
<span data-ttu-id="76c1d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c1d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c1d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c1d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76c1d-134">INPUTS</span></span>

### <span data-ttu-id="76c1d-135">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="76c1d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76c1d-136">OUTPUTS</span></span>

### <span data-ttu-id="76c1d-137">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="76c1d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76c1d-138">NOTES</span></span>

## <span data-ttu-id="76c1d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76c1d-139">RELATED LINKS</span></span>

[<span data-ttu-id="76c1d-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76c1d-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="76c1d-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="76c1d-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="76c1d-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="76c1d-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

