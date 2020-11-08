---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099042"
---
# <span data-ttu-id="a8c2c-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8c2c-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="a8c2c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a8c2c-103">Kopplar en routningstabell till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="a8c2c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8c2c-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8c2c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="a8c2c-106">Cmdleten **set-AzureSubnetRouteTable** associerar en routningstabell till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="a8c2c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8c2c-107">EXAMPLES</span></span>

### <span data-ttu-id="a8c2c-108">Exempel 1: koppla en routningstabell till ett undernät</span><span class="sxs-lookup"><span data-stu-id="a8c2c-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="a8c2c-109">Det här kommandot associerar routningstabellen med namnet PublicRouteTable till under nätet med namnet ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="a8c2c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8c2c-110">PARAMETERS</span></span>

### <span data-ttu-id="a8c2c-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8c2c-111">-PassThru</span></span>
<span data-ttu-id="a8c2c-112">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8c2c-113">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8c2c-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8c2c-114">-Profile</span></span>
<span data-ttu-id="a8c2c-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8c2c-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8c2c-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="a8c2c-117">-RouteTableName</span></span>
<span data-ttu-id="a8c2c-118">Anger namnet på den routningstabell som denna cmdlet associerar med ett undernät.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="a8c2c-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a8c2c-119">-SubnetName</span></span>
<span data-ttu-id="a8c2c-120">Anger det undernät som denna cmdlet associerar till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="a8c2c-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a8c2c-121">-VirtualNetworkName</span></span>
<span data-ttu-id="a8c2c-122">Anger namnet på ett virtuellt nätverk som innehåller det undernät som denna cmdlet kopplar till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="a8c2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8c2c-123">CommonParameters</span></span>
<span data-ttu-id="a8c2c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8c2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8c2c-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8c2c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8c2c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8c2c-126">INPUTS</span></span>

## <span data-ttu-id="a8c2c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8c2c-127">OUTPUTS</span></span>

## <span data-ttu-id="a8c2c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8c2c-128">NOTES</span></span>

## <span data-ttu-id="a8c2c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8c2c-129">RELATED LINKS</span></span>

[<span data-ttu-id="a8c2c-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8c2c-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="a8c2c-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a8c2c-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
