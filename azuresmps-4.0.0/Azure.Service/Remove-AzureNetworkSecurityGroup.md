---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099384"
---
# <span data-ttu-id="9bba1-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bba1-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="9bba1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bba1-102">SYNOPSIS</span></span>
<span data-ttu-id="9bba1-103">Tar bort en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="9bba1-103">Deletes a network security group.</span></span>

## <span data-ttu-id="9bba1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bba1-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bba1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bba1-105">DESCRIPTION</span></span>
<span data-ttu-id="9bba1-106">Cmdleten **Remove-AzureNetworkSecurityGroup** tar bort en Azure Network Security-grupp från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9bba1-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="9bba1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bba1-107">EXAMPLES</span></span>

## <span data-ttu-id="9bba1-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bba1-108">PARAMETERS</span></span>

### <span data-ttu-id="9bba1-109">-Force</span><span class="sxs-lookup"><span data-stu-id="9bba1-109">-Force</span></span>
<span data-ttu-id="9bba1-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9bba1-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bba1-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bba1-111">-Name</span></span>
<span data-ttu-id="9bba1-112">Anger namnet på den nätverks säkerhets grupp som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9bba1-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9bba1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bba1-113">-PassThru</span></span>
<span data-ttu-id="9bba1-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9bba1-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="9bba1-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9bba1-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9bba1-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="9bba1-116">-Profile</span></span>
<span data-ttu-id="9bba1-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9bba1-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9bba1-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9bba1-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9bba1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bba1-119">CommonParameters</span></span>
<span data-ttu-id="9bba1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bba1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bba1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bba1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bba1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bba1-122">INPUTS</span></span>

## <span data-ttu-id="9bba1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bba1-123">OUTPUTS</span></span>

## <span data-ttu-id="9bba1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bba1-124">NOTES</span></span>

## <span data-ttu-id="9bba1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bba1-125">RELATED LINKS</span></span>

[<span data-ttu-id="9bba1-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bba1-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="9bba1-127">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9bba1-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


