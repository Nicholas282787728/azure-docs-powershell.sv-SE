---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099398"
---
# <span data-ttu-id="ce607-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce607-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="ce607-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce607-102">SYNOPSIS</span></span>
<span data-ttu-id="ce607-103">Tar bort en tillgänglighets uppsättning från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ce607-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="ce607-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce607-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ce607-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce607-105">DESCRIPTION</span></span>
<span data-ttu-id="ce607-106">Cmdleten **Remove-AzureAvailabilitySet** tar bort en tillgänglighets uppsättning från en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ce607-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="ce607-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce607-107">EXAMPLES</span></span>

### <span data-ttu-id="ce607-108">9.1</span><span class="sxs-lookup"><span data-stu-id="ce607-108">1:</span></span>
```

```

## <span data-ttu-id="ce607-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce607-109">PARAMETERS</span></span>

### <span data-ttu-id="ce607-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ce607-110">-InformationAction</span></span>
<span data-ttu-id="ce607-111">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ce607-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ce607-112">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ce607-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce607-113">Vidare</span><span class="sxs-lookup"><span data-stu-id="ce607-113">Continue</span></span>
- <span data-ttu-id="ce607-114">Över</span><span class="sxs-lookup"><span data-stu-id="ce607-114">Ignore</span></span>
- <span data-ttu-id="ce607-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="ce607-115">Inquire</span></span>
- <span data-ttu-id="ce607-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ce607-116">SilentlyContinue</span></span>
- <span data-ttu-id="ce607-117">Stanna</span><span class="sxs-lookup"><span data-stu-id="ce607-117">Stop</span></span>
- <span data-ttu-id="ce607-118">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ce607-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce607-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ce607-119">-InformationVariable</span></span>
<span data-ttu-id="ce607-120">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ce607-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce607-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="ce607-121">-Profile</span></span>
<span data-ttu-id="ce607-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ce607-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce607-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ce607-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce607-124">-VM</span><span class="sxs-lookup"><span data-stu-id="ce607-124">-VM</span></span>
<span data-ttu-id="ce607-125">Anger den virtuella dator som den här cmdleten tar bort en tillgänglighets uppsättning från.</span><span class="sxs-lookup"><span data-stu-id="ce607-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

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

### <span data-ttu-id="ce607-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce607-126">CommonParameters</span></span>
<span data-ttu-id="ce607-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce607-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce607-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce607-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce607-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce607-129">INPUTS</span></span>

## <span data-ttu-id="ce607-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce607-130">OUTPUTS</span></span>

## <span data-ttu-id="ce607-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce607-131">NOTES</span></span>

## <span data-ttu-id="ce607-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce607-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce607-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce607-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


