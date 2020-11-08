---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093234"
---
# <span data-ttu-id="1e7f4-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="1e7f4-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="1e7f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="1e7f4-103">Tar bort tillägget BGInfo som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1e7f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e7f4-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e7f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e7f4-105">DESCRIPTION</span></span>
<span data-ttu-id="1e7f4-106">Cmdleten **Remove-AzureVMBGInfoExtension** tar bort tillägget BgInfo som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1e7f4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e7f4-107">EXAMPLES</span></span>

### <span data-ttu-id="1e7f4-108">Exempel 1: ta bort BGInfo-tillägget på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="1e7f4-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="1e7f4-109">Det här kommandot tar bort tillägget BGInfo som tillämpas på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1e7f4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e7f4-110">PARAMETERS</span></span>

### <span data-ttu-id="1e7f4-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e7f4-111">-InformationAction</span></span>
<span data-ttu-id="1e7f4-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e7f4-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1e7f4-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e7f4-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="1e7f4-114">Continue</span></span>
- <span data-ttu-id="1e7f4-115">Över</span><span class="sxs-lookup"><span data-stu-id="1e7f4-115">Ignore</span></span>
- <span data-ttu-id="1e7f4-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="1e7f4-116">Inquire</span></span>
- <span data-ttu-id="1e7f4-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e7f4-117">SilentlyContinue</span></span>
- <span data-ttu-id="1e7f4-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="1e7f4-118">Stop</span></span>
- <span data-ttu-id="1e7f4-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="1e7f4-119">Suspend</span></span>

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

### <span data-ttu-id="1e7f4-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e7f4-120">-InformationVariable</span></span>
<span data-ttu-id="1e7f4-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e7f4-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e7f4-122">-Profile</span></span>
<span data-ttu-id="1e7f4-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e7f4-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e7f4-125">-VM</span><span class="sxs-lookup"><span data-stu-id="1e7f4-125">-VM</span></span>
<span data-ttu-id="1e7f4-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="1e7f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e7f4-127">CommonParameters</span></span>
<span data-ttu-id="1e7f4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e7f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e7f4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e7f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e7f4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e7f4-130">INPUTS</span></span>

## <span data-ttu-id="1e7f4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e7f4-131">OUTPUTS</span></span>

## <span data-ttu-id="1e7f4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e7f4-132">NOTES</span></span>

## <span data-ttu-id="1e7f4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e7f4-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e7f4-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="1e7f4-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="1e7f4-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="1e7f4-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


