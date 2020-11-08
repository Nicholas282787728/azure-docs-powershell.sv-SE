---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099059"
---
# <span data-ttu-id="eb3ce-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="eb3ce-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="eb3ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3ce-103">Associerar en nätverks säkerhets grupp till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="eb3ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb3ce-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb3ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb3ce-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3ce-106">Cmdleten **set-AzureNetworkSecurityGroupToSubnet** associerar en Azure Network Security-grupp till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="eb3ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb3ce-107">EXAMPLES</span></span>

## <span data-ttu-id="eb3ce-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb3ce-108">PARAMETERS</span></span>

### <span data-ttu-id="eb3ce-109">-Force</span><span class="sxs-lookup"><span data-stu-id="eb3ce-109">-Force</span></span>
<span data-ttu-id="eb3ce-110">Anger att denna cmdlet inte ber dig bekräfta borttagningen av en tidigare nätverks säkerhets grupp från under nätet.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="eb3ce-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb3ce-111">-Name</span></span>
<span data-ttu-id="eb3ce-112">Anger namnet på den nätverks säkerhets grupp som denna cmdlet associeras till under nätet.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

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

### <span data-ttu-id="eb3ce-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb3ce-113">-PassThru</span></span>
<span data-ttu-id="eb3ce-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="eb3ce-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb3ce-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="eb3ce-116">-Profile</span></span>
<span data-ttu-id="eb3ce-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="eb3ce-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb3ce-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="eb3ce-119">-SubnetName</span></span>
<span data-ttu-id="eb3ce-120">Anger namnet på ett undernät som denna cmdlet associerar en nätverks säkerhets grupp med.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="eb3ce-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="eb3ce-121">-VirtualNetworkName</span></span>
<span data-ttu-id="eb3ce-122">Anger namnet på ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="eb3ce-123">Denna cmdlet associerar en nätverks säkerhets grupp till ett undernät i det virtuella nätverk som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb3ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3ce-124">CommonParameters</span></span>
<span data-ttu-id="eb3ce-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb3ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3ce-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb3ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3ce-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb3ce-127">INPUTS</span></span>

## <span data-ttu-id="eb3ce-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb3ce-128">OUTPUTS</span></span>

## <span data-ttu-id="eb3ce-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb3ce-129">NOTES</span></span>

## <span data-ttu-id="eb3ce-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb3ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb3ce-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="eb3ce-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="eb3ce-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="eb3ce-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


