---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099099"
---
# <span data-ttu-id="7e9da-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7e9da-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="7e9da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e9da-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9da-103">Tar bort en nätverks säkerhets regel från en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="7e9da-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="7e9da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e9da-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e9da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e9da-105">DESCRIPTION</span></span>
<span data-ttu-id="7e9da-106">Cmdleten **Remove-AzureNetworkSecurityRule** tar bort en Azure Network Security-regel från en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="7e9da-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="7e9da-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e9da-107">EXAMPLES</span></span>

## <span data-ttu-id="7e9da-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e9da-108">PARAMETERS</span></span>

### <span data-ttu-id="7e9da-109">-Force</span><span class="sxs-lookup"><span data-stu-id="7e9da-109">-Force</span></span>
<span data-ttu-id="7e9da-110">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7e9da-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e9da-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e9da-111">-Name</span></span>
<span data-ttu-id="7e9da-112">Anger namnet på nätverks säkerhets regeln som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="7e9da-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e9da-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7e9da-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7e9da-114">Anger den nätverks säkerhets grupp som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="7e9da-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="7e9da-115">Använd Get-AzureNetworkSecurityGroup cmdlet för att få ett **INetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7e9da-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e9da-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e9da-116">-Profile</span></span>
<span data-ttu-id="7e9da-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7e9da-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7e9da-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7e9da-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e9da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9da-119">CommonParameters</span></span>
<span data-ttu-id="7e9da-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e9da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9da-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9da-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9da-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e9da-122">INPUTS</span></span>

## <span data-ttu-id="7e9da-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e9da-123">OUTPUTS</span></span>

## <span data-ttu-id="7e9da-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e9da-124">NOTES</span></span>

## <span data-ttu-id="7e9da-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e9da-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e9da-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7e9da-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


