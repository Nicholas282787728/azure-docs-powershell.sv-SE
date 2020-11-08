---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099563"
---
# <span data-ttu-id="ef106-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="ef106-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="ef106-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef106-102">SYNOPSIS</span></span>
<span data-ttu-id="ef106-103">Hämtar information om en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ef106-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="ef106-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef106-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef106-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef106-105">DESCRIPTION</span></span>
<span data-ttu-id="ef106-106">Cmdleten **Get-AzureNetworkSecurityGroupConfig** returnerar information om en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ef106-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="ef106-107">Ange en *detaljerad* parameter för att Visa nätverks säkerhets reglerna.</span><span class="sxs-lookup"><span data-stu-id="ef106-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="ef106-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef106-108">EXAMPLES</span></span>

## <span data-ttu-id="ef106-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef106-109">PARAMETERS</span></span>

### <span data-ttu-id="ef106-110">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="ef106-110">-Detailed</span></span>
<span data-ttu-id="ef106-111">Anger att nätverks säkerhets reglerna visas i den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef106-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="ef106-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="ef106-112">-Profile</span></span>
<span data-ttu-id="ef106-113">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ef106-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ef106-114">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ef106-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef106-115">-VM</span><span class="sxs-lookup"><span data-stu-id="ef106-115">-VM</span></span>
<span data-ttu-id="ef106-116">Anger den virtuella dator för vilken denna cmdlet får information om en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ef106-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef106-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef106-117">CommonParameters</span></span>
<span data-ttu-id="ef106-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef106-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef106-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef106-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef106-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef106-120">INPUTS</span></span>

## <span data-ttu-id="ef106-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef106-121">OUTPUTS</span></span>

## <span data-ttu-id="ef106-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef106-122">NOTES</span></span>

## <span data-ttu-id="ef106-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef106-123">RELATED LINKS</span></span>

[<span data-ttu-id="ef106-124">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ef106-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="ef106-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ef106-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


