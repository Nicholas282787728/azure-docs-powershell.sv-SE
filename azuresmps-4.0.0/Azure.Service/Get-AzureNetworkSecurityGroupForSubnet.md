---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093364"
---
# <span data-ttu-id="ab507-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="ab507-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="ab507-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab507-102">SYNOPSIS</span></span>
<span data-ttu-id="ab507-103">Hämtar nätverks säkerhets gruppen för ett undernät.</span><span class="sxs-lookup"><span data-stu-id="ab507-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="ab507-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab507-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ab507-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab507-105">DESCRIPTION</span></span>
<span data-ttu-id="ab507-106">Cmdleten **Get-AzureNetworkSecurityGroupForSubnet** hämtar nätverks säkerhets gruppen som är kopplad till ett undernät.</span><span class="sxs-lookup"><span data-stu-id="ab507-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="ab507-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab507-107">EXAMPLES</span></span>

## <span data-ttu-id="ab507-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab507-108">PARAMETERS</span></span>

### <span data-ttu-id="ab507-109">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="ab507-109">-Detailed</span></span>
<span data-ttu-id="ab507-110">Anger att nätverks säkerhets reglerna visas i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab507-110">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="ab507-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab507-111">-Profile</span></span>
<span data-ttu-id="ab507-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ab507-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ab507-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ab507-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab507-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ab507-114">-SubnetName</span></span>
<span data-ttu-id="ab507-115">Anger namnet på ett undernät som denna cmdlet ska ha en nätverks säkerhets grupp för.</span><span class="sxs-lookup"><span data-stu-id="ab507-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="ab507-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ab507-116">-VirtualNetworkName</span></span>
<span data-ttu-id="ab507-117">Anger namnet på ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ab507-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="ab507-118">Denna cmdlet får en nätverks säkerhets grupp för ett undernät i det virtuella nätverk som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ab507-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="ab507-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab507-119">CommonParameters</span></span>
<span data-ttu-id="ab507-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab507-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab507-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab507-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab507-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab507-122">INPUTS</span></span>

## <span data-ttu-id="ab507-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab507-123">OUTPUTS</span></span>

## <span data-ttu-id="ab507-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab507-124">NOTES</span></span>

## <span data-ttu-id="ab507-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab507-125">RELATED LINKS</span></span>

[<span data-ttu-id="ab507-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="ab507-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="ab507-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="ab507-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
