---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258268"
---
# <span data-ttu-id="e9b04-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9b04-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="e9b04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9b04-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b04-103">Hämtar vägar från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e9b04-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="e9b04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9b04-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b04-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9b04-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b04-106">Cmdleten **Get-AzRouteConfig** hämtar vägar från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e9b04-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="e9b04-107">Du kan ange en väg efter namn.</span><span class="sxs-lookup"><span data-stu-id="e9b04-107">You can specify a route by name.</span></span>

## <span data-ttu-id="e9b04-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9b04-108">EXAMPLES</span></span>

### <span data-ttu-id="e9b04-109">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="e9b04-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="e9b04-110">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="e9b04-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="e9b04-111">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e9b04-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e9b04-112">Den aktuella cmdleten får vägen med namnet Route07 i routningstabellen som heter RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="e9b04-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="e9b04-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9b04-113">PARAMETERS</span></span>

### <span data-ttu-id="e9b04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b04-114">-DefaultProfile</span></span>
<span data-ttu-id="e9b04-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b04-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b04-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9b04-116">-Name</span></span>
<span data-ttu-id="e9b04-117">Anger namnet på den väg som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e9b04-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b04-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e9b04-118">-RouteTable</span></span>
<span data-ttu-id="e9b04-119">Anger den routningstabell från vilken denna cmdlet tar vägen.</span><span class="sxs-lookup"><span data-stu-id="e9b04-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b04-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b04-120">CommonParameters</span></span>
<span data-ttu-id="e9b04-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b04-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b04-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9b04-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b04-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9b04-123">INPUTS</span></span>

### <span data-ttu-id="e9b04-124">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9b04-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e9b04-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9b04-125">OUTPUTS</span></span>

### <span data-ttu-id="e9b04-126">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="e9b04-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="e9b04-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9b04-127">NOTES</span></span>

## <span data-ttu-id="e9b04-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9b04-128">RELATED LINKS</span></span>

[<span data-ttu-id="e9b04-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9b04-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="e9b04-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e9b04-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e9b04-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9b04-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e9b04-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9b04-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="e9b04-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e9b04-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

