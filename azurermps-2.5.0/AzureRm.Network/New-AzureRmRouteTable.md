---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930953"
---
# <span data-ttu-id="faa90-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="faa90-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="faa90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="faa90-102">SYNOPSIS</span></span>
<span data-ttu-id="faa90-103">Skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="faa90-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faa90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="faa90-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faa90-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="faa90-105">DESCRIPTION</span></span>
<span data-ttu-id="faa90-106">Cmdleten **New-AzureRmRouteTable** skapar en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="faa90-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="faa90-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="faa90-107">EXAMPLES</span></span>

### <span data-ttu-id="faa90-108">Exempel 1: skapa en routningstabell som innehåller ett flöde</span><span class="sxs-lookup"><span data-stu-id="faa90-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="faa90-109">Det första kommandot skapar en väg med namnet Route07 med hjälp av New-AzureRmRouteConfig cmdlet och lagrar den sedan i $Route-variabeln.</span><span class="sxs-lookup"><span data-stu-id="faa90-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="faa90-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="faa90-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="faa90-111">Det andra kommandot skapar en routningstabell med namnet RouteTable01 och lägger till vägen som lagras i $Route till den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="faa90-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="faa90-112">Kommandot anger den resurs grupp som tabellen tillhör och en plats för tabellen.</span><span class="sxs-lookup"><span data-stu-id="faa90-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="faa90-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="faa90-113">PARAMETERS</span></span>

### <span data-ttu-id="faa90-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faa90-114">-AsJob</span></span>
<span data-ttu-id="faa90-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="faa90-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="faa90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa90-116">-DefaultProfile</span></span>
<span data-ttu-id="faa90-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="faa90-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faa90-118">-Force</span><span class="sxs-lookup"><span data-stu-id="faa90-118">-Force</span></span>
<span data-ttu-id="faa90-119">Anger att den här cmdleten skapar en routningstabell även om det redan finns en vägkälla som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="faa90-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="faa90-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="faa90-120">-Location</span></span>
<span data-ttu-id="faa90-121">Anger i vilken Azure region den här cmdleten skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="faa90-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="faa90-122">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="faa90-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="faa90-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="faa90-123">-Name</span></span>
<span data-ttu-id="faa90-124">Anger ett namn för väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="faa90-124">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="faa90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa90-125">-ResourceGroupName</span></span>
<span data-ttu-id="faa90-126">Anger namnet på den resurs grupp som den här cmdleten skapar en routningstabell för.</span><span class="sxs-lookup"><span data-stu-id="faa90-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="faa90-127">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="faa90-127">-Route</span></span>
<span data-ttu-id="faa90-128">Anger en matris med **väg** objekt som ska kopplas till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="faa90-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="faa90-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="faa90-129">-Tag</span></span>
<span data-ttu-id="faa90-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="faa90-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="faa90-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="faa90-131">For example:</span></span>

<span data-ttu-id="faa90-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="faa90-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="faa90-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="faa90-133">-Confirm</span></span>
<span data-ttu-id="faa90-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="faa90-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa90-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa90-135">-WhatIf</span></span>
<span data-ttu-id="faa90-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="faa90-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa90-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="faa90-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa90-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa90-138">CommonParameters</span></span>
<span data-ttu-id="faa90-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa90-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa90-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa90-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa90-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="faa90-141">INPUTS</span></span>

## <span data-ttu-id="faa90-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="faa90-142">OUTPUTS</span></span>

### <span data-ttu-id="faa90-143">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="faa90-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="faa90-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="faa90-144">NOTES</span></span>

## <span data-ttu-id="faa90-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="faa90-145">RELATED LINKS</span></span>

[<span data-ttu-id="faa90-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="faa90-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="faa90-147">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="faa90-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="faa90-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="faa90-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="faa90-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="faa90-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
