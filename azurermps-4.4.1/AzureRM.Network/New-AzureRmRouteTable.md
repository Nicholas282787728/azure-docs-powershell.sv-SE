---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575985"
---
# <span data-ttu-id="9978d-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9978d-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="9978d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9978d-102">SYNOPSIS</span></span>
<span data-ttu-id="9978d-103">Skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="9978d-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9978d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9978d-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9978d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9978d-105">DESCRIPTION</span></span>
<span data-ttu-id="9978d-106">Cmdleten **New-AzureRmRouteTable** skapar en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="9978d-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="9978d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9978d-107">EXAMPLES</span></span>

### <span data-ttu-id="9978d-108">Exempel 1: skapa en routningstabell som innehåller ett flöde</span><span class="sxs-lookup"><span data-stu-id="9978d-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="9978d-109">Det första kommandot skapar en väg med namnet Route07 med hjälp av New-AzureRmRouteConfig cmdlet och lagrar den sedan i $Route-variabeln.</span><span class="sxs-lookup"><span data-stu-id="9978d-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="9978d-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="9978d-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="9978d-111">Det andra kommandot skapar en routningstabell med namnet RouteTable01 och lägger till vägen som lagras i $Route till den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="9978d-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="9978d-112">Kommandot anger den resurs grupp som tabellen tillhör och en plats för tabellen.</span><span class="sxs-lookup"><span data-stu-id="9978d-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="9978d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9978d-113">PARAMETERS</span></span>

### <span data-ttu-id="9978d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9978d-114">-Force</span></span>
<span data-ttu-id="9978d-115">Anger att den här cmdleten skapar en routningstabell även om det redan finns en vägkälla som har samma namn.</span><span class="sxs-lookup"><span data-stu-id="9978d-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="9978d-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="9978d-116">-Location</span></span>
<span data-ttu-id="9978d-117">Anger i vilken Azure region den här cmdleten skapar en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="9978d-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="9978d-118">Mer information finns i [Azure-regioner](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="9978d-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="9978d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9978d-119">-Name</span></span>
<span data-ttu-id="9978d-120">Anger ett namn för väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="9978d-120">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="9978d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9978d-121">-ResourceGroupName</span></span>
<span data-ttu-id="9978d-122">Anger namnet på den resurs grupp som den här cmdleten skapar en routningstabell för.</span><span class="sxs-lookup"><span data-stu-id="9978d-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="9978d-123">-Cirkulera</span><span class="sxs-lookup"><span data-stu-id="9978d-123">-Route</span></span>
<span data-ttu-id="9978d-124">Anger en matris med **väg** objekt som ska kopplas till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="9978d-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="9978d-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9978d-125">-Tag</span></span>
<span data-ttu-id="9978d-126">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9978d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9978d-127">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="9978d-127">For example:</span></span>

<span data-ttu-id="9978d-128">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="9978d-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9978d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9978d-129">-Confirm</span></span>
<span data-ttu-id="9978d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9978d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9978d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9978d-131">-WhatIf</span></span>
<span data-ttu-id="9978d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9978d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9978d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9978d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9978d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9978d-134">-DefaultProfile</span></span>
<span data-ttu-id="9978d-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9978d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9978d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9978d-136">CommonParameters</span></span>
<span data-ttu-id="9978d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9978d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9978d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9978d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9978d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9978d-139">INPUTS</span></span>

## <span data-ttu-id="9978d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9978d-140">OUTPUTS</span></span>

### <span data-ttu-id="9978d-141">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9978d-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9978d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9978d-142">NOTES</span></span>

## <span data-ttu-id="9978d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9978d-143">RELATED LINKS</span></span>

[<span data-ttu-id="9978d-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9978d-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="9978d-145">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9978d-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="9978d-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9978d-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="9978d-147">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9978d-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
