---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: f00840afac4a4d1f0d92316bc859e0a66e7806ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922094"
---
# <span data-ttu-id="c8dbf-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8dbf-101">New-AzRouteTable</span></span>

## <span data-ttu-id="c8dbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c8dbf-103">Skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-103">Creates a route table.</span></span>

## <span data-ttu-id="c8dbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8dbf-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8dbf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="c8dbf-106">Cmdleten **New-AzRouteTable** skapar en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="c8dbf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8dbf-107">EXAMPLES</span></span>

### <span data-ttu-id="c8dbf-108">Exempel 1: skapa en routningstabell som innehåller ett flöde</span><span class="sxs-lookup"><span data-stu-id="c8dbf-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="c8dbf-109">Det första kommandot skapar en väg med namnet Route07 med hjälp av New-AzRouteConfig cmdlet och lagrar den sedan i $Route-variabeln.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="c8dbf-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="c8dbf-111">Det andra kommandot skapar en routningstabell med namnet RouteTable01 och lägger till vägen som lagras i $Route till den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="c8dbf-112">Kommandot anger den resurs grupp som tabellen tillhör och en plats för tabellen.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="c8dbf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8dbf-113">PARAMETERS</span></span>

### <span data-ttu-id="c8dbf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8dbf-114">-AsJob</span></span>
<span data-ttu-id="c8dbf-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c8dbf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8dbf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8dbf-116">-DefaultProfile</span></span>
<span data-ttu-id="c8dbf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8dbf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c8dbf-118">-Force</span></span>
<span data-ttu-id="c8dbf-119">Anger att den här cmdleten skapar en routningstabell även om det redan finns en vägkälla som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="c8dbf-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="c8dbf-120">-Location</span></span>
<span data-ttu-id="c8dbf-121">Anger i vilken Azure region den här cmdleten skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="c8dbf-122">Mer information finns i [Azure-regioner](http://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="c8dbf-122">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8dbf-123">-Name</span></span>
<span data-ttu-id="c8dbf-124">Anger ett namn för väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-124">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8dbf-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8dbf-126">Anger namnet på den resurs grupp som den här cmdleten skapar en routningstabell för.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-127">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="c8dbf-127">-Route</span></span>
<span data-ttu-id="c8dbf-128">Anger en matris med **väg** objekt som ska kopplas till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c8dbf-129">-Tag</span></span>
<span data-ttu-id="c8dbf-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8dbf-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="c8dbf-131">For example:</span></span>

<span data-ttu-id="c8dbf-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="c8dbf-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8dbf-133">-Confirm</span></span>
<span data-ttu-id="c8dbf-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8dbf-135">-WhatIf</span></span>
<span data-ttu-id="c8dbf-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8dbf-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8dbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8dbf-138">CommonParameters</span></span>
<span data-ttu-id="c8dbf-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8dbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8dbf-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8dbf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8dbf-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8dbf-141">INPUTS</span></span>

## <span data-ttu-id="c8dbf-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8dbf-142">OUTPUTS</span></span>

### <span data-ttu-id="c8dbf-143">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8dbf-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c8dbf-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8dbf-144">NOTES</span></span>

## <span data-ttu-id="c8dbf-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8dbf-145">RELATED LINKS</span></span>

[<span data-ttu-id="c8dbf-146">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8dbf-146">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c8dbf-147">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8dbf-147">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="c8dbf-148">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8dbf-148">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="c8dbf-149">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8dbf-149">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
