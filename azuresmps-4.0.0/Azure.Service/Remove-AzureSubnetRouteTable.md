---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099686"
---
# <span data-ttu-id="71c44-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c44-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="71c44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71c44-102">SYNOPSIS</span></span>
<span data-ttu-id="71c44-103">Tar bort en kopplings tabell från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="71c44-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="71c44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71c44-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="71c44-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71c44-105">DESCRIPTION</span></span>
<span data-ttu-id="71c44-106">Cmdleten **Remove-AzureSubnetRouteTable** tar bort en koppling för routningstabellen från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="71c44-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="71c44-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71c44-107">EXAMPLES</span></span>

### <span data-ttu-id="71c44-108">Exempel 1: ta bort en associering mellan en routningstabell och ett undernät</span><span class="sxs-lookup"><span data-stu-id="71c44-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="71c44-109">Det här kommandot tar bort kopplingen för väg tabellen som heter PublicRouteTable till under nätet med namnet ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="71c44-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="71c44-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71c44-110">PARAMETERS</span></span>

### <span data-ttu-id="71c44-111">-Force</span><span class="sxs-lookup"><span data-stu-id="71c44-111">-Force</span></span>
<span data-ttu-id="71c44-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="71c44-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71c44-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71c44-113">-PassThru</span></span>
<span data-ttu-id="71c44-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="71c44-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="71c44-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="71c44-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71c44-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="71c44-116">-Profile</span></span>
<span data-ttu-id="71c44-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="71c44-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="71c44-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="71c44-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71c44-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="71c44-119">-SubnetName</span></span>
<span data-ttu-id="71c44-120">Anger det undernät som denna cmdlet tar bort routningstabellen för.</span><span class="sxs-lookup"><span data-stu-id="71c44-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="71c44-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="71c44-121">-VirtualNetworkName</span></span>
<span data-ttu-id="71c44-122">Anger namnet på ett virtuellt nätverk som innehåller det undernät som den här cmdleten tar bort routningstabellen för.</span><span class="sxs-lookup"><span data-stu-id="71c44-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="71c44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c44-123">CommonParameters</span></span>
<span data-ttu-id="71c44-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c44-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c44-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c44-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71c44-126">INPUTS</span></span>

## <span data-ttu-id="71c44-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71c44-127">OUTPUTS</span></span>

## <span data-ttu-id="71c44-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71c44-128">NOTES</span></span>

## <span data-ttu-id="71c44-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71c44-129">RELATED LINKS</span></span>

[<span data-ttu-id="71c44-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c44-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="71c44-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c44-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


