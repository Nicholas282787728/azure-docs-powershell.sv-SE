---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099787"
---
# <span data-ttu-id="3b89f-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="3b89f-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="3b89f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b89f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b89f-103">Hämtar information om statisk IP-adress från ett virtuellt dator objekt, om det finns något.</span><span class="sxs-lookup"><span data-stu-id="3b89f-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="3b89f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b89f-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3b89f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b89f-105">DESCRIPTION</span></span>
<span data-ttu-id="3b89f-106">Cmdleten **Get-AzureStaticVNetIP** hämtar den statiska virtuell nätverks informationen (VNet) från ett virtuellt dator objekt, om det finns något.</span><span class="sxs-lookup"><span data-stu-id="3b89f-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="3b89f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b89f-107">EXAMPLES</span></span>

### <span data-ttu-id="3b89f-108">9.1</span><span class="sxs-lookup"><span data-stu-id="3b89f-108">1:</span></span>
```

```

## <span data-ttu-id="3b89f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b89f-109">PARAMETERS</span></span>

### <span data-ttu-id="3b89f-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3b89f-110">-InformationAction</span></span>
<span data-ttu-id="3b89f-111">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3b89f-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b89f-112">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3b89f-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b89f-113">Vidare</span><span class="sxs-lookup"><span data-stu-id="3b89f-113">Continue</span></span>
- <span data-ttu-id="3b89f-114">Över</span><span class="sxs-lookup"><span data-stu-id="3b89f-114">Ignore</span></span>
- <span data-ttu-id="3b89f-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="3b89f-115">Inquire</span></span>
- <span data-ttu-id="3b89f-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b89f-116">SilentlyContinue</span></span>
- <span data-ttu-id="3b89f-117">Stanna</span><span class="sxs-lookup"><span data-stu-id="3b89f-117">Stop</span></span>
- <span data-ttu-id="3b89f-118">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3b89f-118">Suspend</span></span>

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

### <span data-ttu-id="3b89f-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b89f-119">-InformationVariable</span></span>
<span data-ttu-id="3b89f-120">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3b89f-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3b89f-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="3b89f-121">-Profile</span></span>
<span data-ttu-id="3b89f-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3b89f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b89f-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3b89f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b89f-124">-VM</span><span class="sxs-lookup"><span data-stu-id="3b89f-124">-VM</span></span>
<span data-ttu-id="3b89f-125">Anger ett permanent virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="3b89f-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="3b89f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b89f-126">CommonParameters</span></span>
<span data-ttu-id="3b89f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b89f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b89f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b89f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b89f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b89f-129">INPUTS</span></span>

## <span data-ttu-id="3b89f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b89f-130">OUTPUTS</span></span>

## <span data-ttu-id="3b89f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b89f-131">NOTES</span></span>

## <span data-ttu-id="3b89f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b89f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b89f-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="3b89f-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


