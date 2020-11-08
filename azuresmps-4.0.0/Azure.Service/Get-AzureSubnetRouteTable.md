---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093268"
---
# <span data-ttu-id="f07fb-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f07fb-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="f07fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f07fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f07fb-103">Hämtar en väg tabell för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="f07fb-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="f07fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f07fb-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f07fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f07fb-105">DESCRIPTION</span></span>
<span data-ttu-id="f07fb-106">Cmdleten **Get-AzureSubnetRouteTable** hämtar väg tabellen som är kopplad till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="f07fb-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="f07fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f07fb-107">EXAMPLES</span></span>

### <span data-ttu-id="f07fb-108">Exempel 1: Visa vägar för ett undernät</span><span class="sxs-lookup"><span data-stu-id="f07fb-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="f07fb-109">Det här kommandot visar vägarna i väg tabell namnet som är kopplat till under nätet med namnet ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="f07fb-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="f07fb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f07fb-110">PARAMETERS</span></span>

### <span data-ttu-id="f07fb-111">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="f07fb-111">-Detailed</span></span>
<span data-ttu-id="f07fb-112">Anger att den här cmdleten visar vägarna i väg tabellen som är associerad med under nätet.</span><span class="sxs-lookup"><span data-stu-id="f07fb-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="f07fb-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="f07fb-113">-Profile</span></span>
<span data-ttu-id="f07fb-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f07fb-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f07fb-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f07fb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07fb-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f07fb-116">-SubnetName</span></span>
<span data-ttu-id="f07fb-117">Anger det undernät som denna cmdlet hämtar väg tabellen för.</span><span class="sxs-lookup"><span data-stu-id="f07fb-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07fb-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f07fb-118">-VirtualNetworkName</span></span>
<span data-ttu-id="f07fb-119">Anger namnet på ett virtuellt nätverk som innehåller det undernät som den här cmdleten får väg tabellen för.</span><span class="sxs-lookup"><span data-stu-id="f07fb-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07fb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07fb-120">CommonParameters</span></span>
<span data-ttu-id="f07fb-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07fb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07fb-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07fb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07fb-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f07fb-123">INPUTS</span></span>

## <span data-ttu-id="f07fb-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f07fb-124">OUTPUTS</span></span>

## <span data-ttu-id="f07fb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f07fb-125">NOTES</span></span>

## <span data-ttu-id="f07fb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f07fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="f07fb-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f07fb-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="f07fb-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="f07fb-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


