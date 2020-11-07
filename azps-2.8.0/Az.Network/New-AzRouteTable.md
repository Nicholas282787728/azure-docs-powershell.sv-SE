---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919080"
---
# <span data-ttu-id="ff335-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff335-101">New-AzRouteTable</span></span>

## <span data-ttu-id="ff335-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff335-102">SYNOPSIS</span></span>
<span data-ttu-id="ff335-103">Skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="ff335-103">Creates a route table.</span></span>

## <span data-ttu-id="ff335-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff335-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff335-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff335-105">DESCRIPTION</span></span>
<span data-ttu-id="ff335-106">Cmdleten **New-AzRouteTable** skapar en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="ff335-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="ff335-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff335-107">EXAMPLES</span></span>

### <span data-ttu-id="ff335-108">Exempel 1: skapa en routningstabell som innehåller ett flöde</span><span class="sxs-lookup"><span data-stu-id="ff335-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="ff335-109">Det första kommandot skapar en väg med namnet Route07 med hjälp av New-AzRouteConfig cmdlet och lagrar den sedan i $Route-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ff335-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="ff335-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="ff335-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="ff335-111">Det andra kommandot skapar en routningstabell med namnet RouteTable01 och lägger till vägen som lagras i $Route till den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="ff335-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="ff335-112">Kommandot anger den resurs grupp som tabellen tillhör och en plats för tabellen.</span><span class="sxs-lookup"><span data-stu-id="ff335-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="ff335-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff335-113">PARAMETERS</span></span>

### <span data-ttu-id="ff335-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff335-114">-AsJob</span></span>
<span data-ttu-id="ff335-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ff335-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff335-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff335-116">-DefaultProfile</span></span>
<span data-ttu-id="ff335-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff335-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff335-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="ff335-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="ff335-119">Inaktivera automatisk spridning av BGP-vägar.</span><span class="sxs-lookup"><span data-stu-id="ff335-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="ff335-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ff335-120">-Force</span></span>
<span data-ttu-id="ff335-121">Anger att den här cmdleten skapar en routningstabell även om det redan finns en vägkälla som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="ff335-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="ff335-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="ff335-122">-Location</span></span>
<span data-ttu-id="ff335-123">Anger i vilken Azure region den här cmdleten skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="ff335-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="ff335-124">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="ff335-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff335-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff335-125">-Name</span></span>
<span data-ttu-id="ff335-126">Anger ett namn för väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="ff335-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff335-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff335-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff335-128">Anger namnet på den resurs grupp som den här cmdleten skapar en routningstabell för.</span><span class="sxs-lookup"><span data-stu-id="ff335-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff335-129">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="ff335-129">-Route</span></span>
<span data-ttu-id="ff335-130">Anger en matris med **väg** objekt som ska kopplas till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="ff335-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff335-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ff335-131">-Tag</span></span>
<span data-ttu-id="ff335-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ff335-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ff335-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ff335-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff335-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff335-134">-Confirm</span></span>
<span data-ttu-id="ff335-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff335-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff335-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff335-136">-WhatIf</span></span>
<span data-ttu-id="ff335-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff335-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff335-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff335-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff335-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff335-139">CommonParameters</span></span>
<span data-ttu-id="ff335-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff335-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff335-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff335-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff335-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff335-142">INPUTS</span></span>

### <span data-ttu-id="ff335-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ff335-143">System.String</span></span>

### <span data-ttu-id="ff335-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ff335-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff335-145">Microsoft. Azure. commands. Network. Models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="ff335-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="ff335-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff335-146">OUTPUTS</span></span>

### <span data-ttu-id="ff335-147">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff335-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ff335-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff335-148">NOTES</span></span>

## <span data-ttu-id="ff335-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff335-149">RELATED LINKS</span></span>

[<span data-ttu-id="ff335-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff335-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="ff335-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ff335-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="ff335-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff335-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="ff335-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff335-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
