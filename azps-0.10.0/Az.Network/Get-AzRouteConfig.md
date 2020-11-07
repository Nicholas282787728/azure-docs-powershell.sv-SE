---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922225"
---
# <span data-ttu-id="e0521-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0521-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="e0521-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0521-102">SYNOPSIS</span></span>
<span data-ttu-id="e0521-103">Hämtar vägar från en route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e0521-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="e0521-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0521-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0521-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0521-105">DESCRIPTION</span></span>
<span data-ttu-id="e0521-106">Cmdleten **Get-AzRouteConfig** hämtar vägar från en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e0521-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="e0521-107">Du kan ange en väg efter namn.</span><span class="sxs-lookup"><span data-stu-id="e0521-107">You can specify a route by name.</span></span>

## <span data-ttu-id="e0521-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0521-108">EXAMPLES</span></span>

### <span data-ttu-id="e0521-109">Exempel 1: Hämta en routningstabell</span><span class="sxs-lookup"><span data-stu-id="e0521-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="e0521-110">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av cmdleten **Get-AzRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="e0521-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="e0521-111">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e0521-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e0521-112">Den aktuella cmdleten får vägen med namnet Route07 i routningstabellen som heter RouteTable01.</span><span class="sxs-lookup"><span data-stu-id="e0521-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="e0521-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0521-113">PARAMETERS</span></span>

### <span data-ttu-id="e0521-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0521-114">-DefaultProfile</span></span>
<span data-ttu-id="e0521-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0521-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0521-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0521-116">-Name</span></span>
<span data-ttu-id="e0521-117">Anger namnet på den väg som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e0521-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e0521-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e0521-118">-RouteTable</span></span>
<span data-ttu-id="e0521-119">Anger den routningstabell från vilken denna cmdlet tar vägen.</span><span class="sxs-lookup"><span data-stu-id="e0521-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="e0521-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0521-120">CommonParameters</span></span>
<span data-ttu-id="e0521-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0521-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0521-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0521-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0521-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0521-123">INPUTS</span></span>

### <span data-ttu-id="e0521-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0521-124">PSRouteTable</span></span>
<span data-ttu-id="e0521-125">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e0521-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="e0521-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0521-126">OUTPUTS</span></span>

### <span data-ttu-id="e0521-127">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="e0521-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="e0521-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0521-128">NOTES</span></span>

## <span data-ttu-id="e0521-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0521-129">RELATED LINKS</span></span>

[<span data-ttu-id="e0521-130">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0521-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="e0521-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e0521-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e0521-132">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0521-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e0521-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0521-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="e0521-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e0521-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


