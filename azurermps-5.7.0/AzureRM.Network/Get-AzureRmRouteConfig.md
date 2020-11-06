---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: f00a1d0c67d7bb395a328e01915f5bb0334d3d83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574916"
---
# <span data-ttu-id="e537c-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e537c-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="e537c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e537c-102">SYNOPSIS</span></span>
<span data-ttu-id="e537c-103">Hämtar vägar från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e537c-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e537c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e537c-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e537c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e537c-105">DESCRIPTION</span></span>
<span data-ttu-id="e537c-106">Cmdleten **Get-AzureRmRouteConfig** hämtar vägar från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e537c-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="e537c-107">Du kan ange en väg efter namn.</span><span class="sxs-lookup"><span data-stu-id="e537c-107">You can specify a route by name.</span></span>

## <span data-ttu-id="e537c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e537c-108">EXAMPLES</span></span>

### <span data-ttu-id="e537c-109">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="e537c-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="e537c-110">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="e537c-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="e537c-111">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e537c-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e537c-112">Den aktuella cmdleten får vägen med namnet Route07 i routningstabellen som heter RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="e537c-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="e537c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e537c-113">PARAMETERS</span></span>

### <span data-ttu-id="e537c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e537c-114">-DefaultProfile</span></span>
<span data-ttu-id="e537c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e537c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e537c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e537c-116">-Name</span></span>
<span data-ttu-id="e537c-117">Anger namnet på den väg som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e537c-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e537c-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e537c-118">-RouteTable</span></span>
<span data-ttu-id="e537c-119">Anger den routningstabell från vilken denna cmdlet tar vägen.</span><span class="sxs-lookup"><span data-stu-id="e537c-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="e537c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e537c-120">CommonParameters</span></span>
<span data-ttu-id="e537c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e537c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e537c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e537c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e537c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e537c-123">INPUTS</span></span>

### <span data-ttu-id="e537c-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e537c-124">PSRouteTable</span></span>
<span data-ttu-id="e537c-125">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e537c-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="e537c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e537c-126">OUTPUTS</span></span>

### <span data-ttu-id="e537c-127">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="e537c-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="e537c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e537c-128">NOTES</span></span>

## <span data-ttu-id="e537c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e537c-129">RELATED LINKS</span></span>

[<span data-ttu-id="e537c-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e537c-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="e537c-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e537c-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="e537c-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e537c-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="e537c-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e537c-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="e537c-134">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e537c-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


