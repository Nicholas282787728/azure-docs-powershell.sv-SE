---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093258"
---
# <span data-ttu-id="338aa-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="338aa-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="338aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="338aa-102">SYNOPSIS</span></span>
<span data-ttu-id="338aa-103">Hämtar BGInfo-tillägget som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="338aa-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="338aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="338aa-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="338aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="338aa-105">DESCRIPTION</span></span>
<span data-ttu-id="338aa-106">Cmdleten **Get-AzureVMBGInfoExtension** hämtar fil namns tillägget BgInfo på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="338aa-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="338aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="338aa-107">EXAMPLES</span></span>

### <span data-ttu-id="338aa-108">Exempel 1: få tillägget BGInfo installerat på en angiven virtuell dator</span><span class="sxs-lookup"><span data-stu-id="338aa-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="338aa-109">Det här kommandot får tillägget BGInfo som används på en angiven virtuell dator</span><span class="sxs-lookup"><span data-stu-id="338aa-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="338aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="338aa-110">PARAMETERS</span></span>

### <span data-ttu-id="338aa-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="338aa-111">-InformationAction</span></span>
<span data-ttu-id="338aa-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="338aa-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="338aa-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="338aa-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="338aa-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="338aa-114">Continue</span></span>
- <span data-ttu-id="338aa-115">Över</span><span class="sxs-lookup"><span data-stu-id="338aa-115">Ignore</span></span>
- <span data-ttu-id="338aa-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="338aa-116">Inquire</span></span>
- <span data-ttu-id="338aa-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="338aa-117">SilentlyContinue</span></span>
- <span data-ttu-id="338aa-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="338aa-118">Stop</span></span>
- <span data-ttu-id="338aa-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="338aa-119">Suspend</span></span>

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

### <span data-ttu-id="338aa-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="338aa-120">-InformationVariable</span></span>
<span data-ttu-id="338aa-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="338aa-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="338aa-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="338aa-122">-Profile</span></span>
<span data-ttu-id="338aa-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="338aa-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="338aa-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="338aa-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="338aa-125">-VM</span><span class="sxs-lookup"><span data-stu-id="338aa-125">-VM</span></span>
<span data-ttu-id="338aa-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="338aa-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="338aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338aa-127">CommonParameters</span></span>
<span data-ttu-id="338aa-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338aa-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="338aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338aa-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="338aa-130">INPUTS</span></span>

## <span data-ttu-id="338aa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="338aa-131">OUTPUTS</span></span>

## <span data-ttu-id="338aa-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="338aa-132">NOTES</span></span>

## <span data-ttu-id="338aa-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="338aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="338aa-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="338aa-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="338aa-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="338aa-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


