---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099380"
---
# <span data-ttu-id="37702-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="37702-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="37702-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37702-102">SYNOPSIS</span></span>
<span data-ttu-id="37702-103">Avkopplar en nätverks säkerhets grupp från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="37702-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="37702-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37702-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37702-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37702-105">DESCRIPTION</span></span>
<span data-ttu-id="37702-106">Cmdleten **Remove-AzureNetworkSecurityGroupFromSubnet** kopplas bort en Azure nätverks säkerhets grupp från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="37702-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="37702-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37702-107">EXAMPLES</span></span>

## <span data-ttu-id="37702-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37702-108">PARAMETERS</span></span>

### <span data-ttu-id="37702-109">-Force</span><span class="sxs-lookup"><span data-stu-id="37702-109">-Force</span></span>
<span data-ttu-id="37702-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="37702-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37702-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="37702-111">-Name</span></span>
<span data-ttu-id="37702-112">Anger namnet på nätverks säkerhets gruppen som denna cmdlet kopplas från ett undernät.</span><span class="sxs-lookup"><span data-stu-id="37702-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="37702-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37702-113">-PassThru</span></span>
<span data-ttu-id="37702-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="37702-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="37702-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="37702-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="37702-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="37702-116">-Profile</span></span>
<span data-ttu-id="37702-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="37702-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="37702-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="37702-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37702-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="37702-119">-SubnetName</span></span>
<span data-ttu-id="37702-120">Anger namnet på ett undernät som denna cmdlet avkopplar en nätverks säkerhets grupp från.</span><span class="sxs-lookup"><span data-stu-id="37702-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="37702-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="37702-121">-VirtualNetworkName</span></span>
<span data-ttu-id="37702-122">Anger namnet på ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="37702-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="37702-123">Denna cmdlet avassocierar en nätverks säkerhets grupp från ett undernät i det virtuella nätverk som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="37702-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="37702-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37702-124">CommonParameters</span></span>
<span data-ttu-id="37702-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37702-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37702-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37702-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37702-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37702-127">INPUTS</span></span>

## <span data-ttu-id="37702-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37702-128">OUTPUTS</span></span>

## <span data-ttu-id="37702-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37702-129">NOTES</span></span>

## <span data-ttu-id="37702-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37702-130">RELATED LINKS</span></span>

[<span data-ttu-id="37702-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="37702-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="37702-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="37702-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


