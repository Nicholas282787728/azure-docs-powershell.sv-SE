---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: fe079282d85b5aea8ebedcf69504fbb0e3dab04b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924362"
---
# <span data-ttu-id="62003-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="62003-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="62003-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62003-102">SYNOPSIS</span></span>
<span data-ttu-id="62003-103">Tar bort en väg från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="62003-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="62003-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62003-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62003-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62003-105">DESCRIPTION</span></span>
<span data-ttu-id="62003-106">Cmdleten **Remove-AzRouteConfig** tar bort en väg från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="62003-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="62003-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62003-107">EXAMPLES</span></span>

### <span data-ttu-id="62003-108">Exempel 1: ta bort en väg</span><span class="sxs-lookup"><span data-stu-id="62003-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
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

<span data-ttu-id="62003-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="62003-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="62003-110">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="62003-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="62003-111">Den aktuella cmdleten tar bort vägen med namnet Route02 och skickar resultatet till cmdleten **set-AzRouteTable** , som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="62003-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="62003-112">Tabellen innehåller inte längre vägen med namnet Route02.</span><span class="sxs-lookup"><span data-stu-id="62003-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="62003-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62003-113">PARAMETERS</span></span>

### <span data-ttu-id="62003-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62003-114">-DefaultProfile</span></span>
<span data-ttu-id="62003-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62003-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62003-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="62003-116">-Name</span></span>
<span data-ttu-id="62003-117">Anger namnet på den väg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="62003-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62003-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="62003-118">-RouteTable</span></span>
<span data-ttu-id="62003-119">Anger den routningstabell som innehåller vägen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62003-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="62003-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62003-120">-Confirm</span></span>
<span data-ttu-id="62003-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62003-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62003-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62003-122">-WhatIf</span></span>
<span data-ttu-id="62003-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62003-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62003-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62003-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62003-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62003-125">CommonParameters</span></span>
<span data-ttu-id="62003-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62003-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62003-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62003-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62003-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62003-128">INPUTS</span></span>

### <span data-ttu-id="62003-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="62003-129">PSRouteTable</span></span>
<span data-ttu-id="62003-130">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="62003-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="62003-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62003-131">OUTPUTS</span></span>

### <span data-ttu-id="62003-132">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="62003-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="62003-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62003-133">NOTES</span></span>

## <span data-ttu-id="62003-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62003-134">RELATED LINKS</span></span>

[<span data-ttu-id="62003-135">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="62003-135">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="62003-136">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="62003-136">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="62003-137">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="62003-137">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="62003-138">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="62003-138">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


