---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099140"
---
# <span data-ttu-id="e5fe1-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5fe1-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="e5fe1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fe1-103">Skapar en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="e5fe1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5fe1-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5fe1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5fe1-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fe1-106">Cmdleten **New-AzureNetworkSecurityGroup** skapar en Azure nätverks säkerhets grupp på en plats.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="e5fe1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-107">EXAMPLES</span></span>

## <span data-ttu-id="e5fe1-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5fe1-108">PARAMETERS</span></span>

### <span data-ttu-id="e5fe1-109">-Etikett</span><span class="sxs-lookup"><span data-stu-id="e5fe1-109">-Label</span></span>
<span data-ttu-id="e5fe1-110">Anger en beskrivning för den nya nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-110">Specifies a description for the new network security group.</span></span>

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

### <span data-ttu-id="e5fe1-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="e5fe1-111">-Location</span></span>
<span data-ttu-id="e5fe1-112">Anger den Azure-plats där denna cmdlet skapar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="e5fe1-113">Använd Get-AzureLocation cmdlet för att få giltiga platser.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="e5fe1-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5fe1-114">-Name</span></span>
<span data-ttu-id="e5fe1-115">Anger ett namn för den nya nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-115">Specifies a name for the new network security group.</span></span>

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

### <span data-ttu-id="e5fe1-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="e5fe1-116">-Profile</span></span>
<span data-ttu-id="e5fe1-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e5fe1-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5fe1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fe1-119">CommonParameters</span></span>
<span data-ttu-id="e5fe1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fe1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fe1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5fe1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fe1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5fe1-122">INPUTS</span></span>

## <span data-ttu-id="e5fe1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5fe1-123">OUTPUTS</span></span>

## <span data-ttu-id="e5fe1-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5fe1-124">NOTES</span></span>

## <span data-ttu-id="e5fe1-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5fe1-125">RELATED LINKS</span></span>

[<span data-ttu-id="e5fe1-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e5fe1-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


