---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: a311d64fbdb086ca1d52ab5a1db725e278c6cc16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582080"
---
# <span data-ttu-id="d4be8-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4be8-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="d4be8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4be8-102">SYNOPSIS</span></span>
<span data-ttu-id="d4be8-103">Skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="d4be8-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4be8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4be8-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-DisableBgpRoutePropagation] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4be8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4be8-105">DESCRIPTION</span></span>
<span data-ttu-id="d4be8-106">Cmdleten **New-AzureRmRouteTable** skapar en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="d4be8-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="d4be8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4be8-107">EXAMPLES</span></span>

### <span data-ttu-id="d4be8-108">Exempel 1: skapa en routningstabell som innehåller ett flöde</span><span class="sxs-lookup"><span data-stu-id="d4be8-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="d4be8-109">Det första kommandot skapar en väg med namnet Route07 med hjälp av New-AzureRmRouteConfig cmdlet och lagrar den sedan i $Route-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d4be8-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="d4be8-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="d4be8-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="d4be8-111">Det andra kommandot skapar en routningstabell med namnet RouteTable01 och lägger till vägen som lagras i $Route till den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="d4be8-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="d4be8-112">Kommandot anger den resurs grupp som tabellen tillhör och en plats för tabellen.</span><span class="sxs-lookup"><span data-stu-id="d4be8-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="d4be8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4be8-113">PARAMETERS</span></span>

### <span data-ttu-id="d4be8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4be8-114">-AsJob</span></span>
<span data-ttu-id="d4be8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d4be8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4be8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4be8-116">-DefaultProfile</span></span>
<span data-ttu-id="d4be8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4be8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4be8-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="d4be8-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="d4be8-119">Inaktivera automatisk spridning av BGP-vägar.</span><span class="sxs-lookup"><span data-stu-id="d4be8-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="d4be8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d4be8-120">-Force</span></span>
<span data-ttu-id="d4be8-121">Anger att den här cmdleten skapar en routningstabell även om det redan finns en vägkälla som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="d4be8-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="d4be8-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="d4be8-122">-Location</span></span>
<span data-ttu-id="d4be8-123">Anger i vilken Azure region den här cmdleten skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="d4be8-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="d4be8-124">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="d4be8-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="d4be8-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4be8-125">-Name</span></span>
<span data-ttu-id="d4be8-126">Anger ett namn för väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="d4be8-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="d4be8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4be8-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4be8-128">Anger namnet på den resurs grupp som den här cmdleten skapar en routningstabell för.</span><span class="sxs-lookup"><span data-stu-id="d4be8-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="d4be8-129">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="d4be8-129">-Route</span></span>
<span data-ttu-id="d4be8-130">Anger en matris med **väg** objekt som ska kopplas till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="d4be8-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="d4be8-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d4be8-131">-Tag</span></span>
<span data-ttu-id="d4be8-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d4be8-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d4be8-133">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d4be8-133">For example:</span></span>

<span data-ttu-id="d4be8-134">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d4be8-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d4be8-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4be8-135">-Confirm</span></span>
<span data-ttu-id="d4be8-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4be8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4be8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4be8-137">-WhatIf</span></span>
<span data-ttu-id="d4be8-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4be8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4be8-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4be8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4be8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4be8-140">CommonParameters</span></span>
<span data-ttu-id="d4be8-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4be8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4be8-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4be8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4be8-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4be8-143">INPUTS</span></span>

### <span data-ttu-id="d4be8-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="d4be8-144">None</span></span>
<span data-ttu-id="d4be8-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d4be8-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4be8-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4be8-146">OUTPUTS</span></span>

### <span data-ttu-id="d4be8-147">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4be8-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d4be8-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4be8-148">NOTES</span></span>

## <span data-ttu-id="d4be8-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4be8-149">RELATED LINKS</span></span>

[<span data-ttu-id="d4be8-150">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4be8-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="d4be8-151">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d4be8-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="d4be8-152">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4be8-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="d4be8-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4be8-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
