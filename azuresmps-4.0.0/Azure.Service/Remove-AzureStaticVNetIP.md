---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099334"
---
# <span data-ttu-id="afece-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="afece-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="afece-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afece-102">SYNOPSIS</span></span>
<span data-ttu-id="afece-103">Tar bort den statiska IP-postinformationen från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="afece-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="afece-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afece-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="afece-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afece-105">DESCRIPTION</span></span>
<span data-ttu-id="afece-106">Cmdleten **Remove-AzureStaticVNetIP** tar bort det statiska virtuella nätverkets IP-adress från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="afece-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="afece-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afece-107">EXAMPLES</span></span>

### <span data-ttu-id="afece-108">9.1</span><span class="sxs-lookup"><span data-stu-id="afece-108">1:</span></span>
```

```

## <span data-ttu-id="afece-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afece-109">PARAMETERS</span></span>

### <span data-ttu-id="afece-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="afece-110">-InformationAction</span></span>
<span data-ttu-id="afece-111">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="afece-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="afece-112">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="afece-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afece-113">Vidare</span><span class="sxs-lookup"><span data-stu-id="afece-113">Continue</span></span>
- <span data-ttu-id="afece-114">Över</span><span class="sxs-lookup"><span data-stu-id="afece-114">Ignore</span></span>
- <span data-ttu-id="afece-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="afece-115">Inquire</span></span>
- <span data-ttu-id="afece-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="afece-116">SilentlyContinue</span></span>
- <span data-ttu-id="afece-117">Stanna</span><span class="sxs-lookup"><span data-stu-id="afece-117">Stop</span></span>
- <span data-ttu-id="afece-118">Avbryt</span><span class="sxs-lookup"><span data-stu-id="afece-118">Suspend</span></span>

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

### <span data-ttu-id="afece-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="afece-119">-InformationVariable</span></span>
<span data-ttu-id="afece-120">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="afece-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="afece-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="afece-121">-Profile</span></span>
<span data-ttu-id="afece-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="afece-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="afece-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="afece-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="afece-124">-VM</span><span class="sxs-lookup"><span data-stu-id="afece-124">-VM</span></span>
<span data-ttu-id="afece-125">Anger ett permanent virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="afece-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="afece-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afece-126">CommonParameters</span></span>
<span data-ttu-id="afece-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afece-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afece-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afece-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afece-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afece-129">INPUTS</span></span>

## <span data-ttu-id="afece-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afece-130">OUTPUTS</span></span>

## <span data-ttu-id="afece-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afece-131">NOTES</span></span>

## <span data-ttu-id="afece-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afece-132">RELATED LINKS</span></span>

[<span data-ttu-id="afece-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="afece-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="afece-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="afece-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


