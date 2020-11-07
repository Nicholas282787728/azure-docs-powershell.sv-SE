---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931269"
---
# <span data-ttu-id="c8155-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8155-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="c8155-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8155-102">SYNOPSIS</span></span>
<span data-ttu-id="c8155-103">Hämtar vägar från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="c8155-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8155-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8155-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8155-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8155-105">DESCRIPTION</span></span>
<span data-ttu-id="c8155-106">Cmdleten **Get-AzureRmRouteConfig** hämtar vägar från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="c8155-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="c8155-107">Du kan ange en väg efter namn.</span><span class="sxs-lookup"><span data-stu-id="c8155-107">You can specify a route by name.</span></span>

## <span data-ttu-id="c8155-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8155-108">EXAMPLES</span></span>

### <span data-ttu-id="c8155-109">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="c8155-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="c8155-110">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="c8155-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="c8155-111">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c8155-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c8155-112">Den aktuella cmdleten får vägen med namnet Route07 i routningstabellen som heter RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="c8155-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="c8155-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8155-113">PARAMETERS</span></span>

### <span data-ttu-id="c8155-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8155-114">-DefaultProfile</span></span>
<span data-ttu-id="c8155-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8155-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8155-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8155-116">-Name</span></span>
<span data-ttu-id="c8155-117">Anger namnet på den väg som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="c8155-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8155-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c8155-118">-RouteTable</span></span>
<span data-ttu-id="c8155-119">Anger den routningstabell från vilken denna cmdlet tar vägen.</span><span class="sxs-lookup"><span data-stu-id="c8155-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="c8155-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8155-120">CommonParameters</span></span>
<span data-ttu-id="c8155-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8155-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8155-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8155-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8155-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8155-123">INPUTS</span></span>

### <span data-ttu-id="c8155-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8155-124">PSRouteTable</span></span>
<span data-ttu-id="c8155-125">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c8155-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="c8155-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8155-126">OUTPUTS</span></span>

### <span data-ttu-id="c8155-127">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="c8155-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="c8155-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8155-128">NOTES</span></span>

## <span data-ttu-id="c8155-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8155-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8155-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8155-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="c8155-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c8155-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="c8155-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8155-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="c8155-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8155-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="c8155-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c8155-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


