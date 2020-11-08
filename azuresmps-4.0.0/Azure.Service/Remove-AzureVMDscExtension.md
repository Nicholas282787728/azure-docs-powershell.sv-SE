---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099677"
---
# <span data-ttu-id="94fda-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="94fda-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="94fda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94fda-102">SYNOPSIS</span></span>
<span data-ttu-id="94fda-103">Tar bort ett Azure DSC-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="94fda-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="94fda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94fda-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94fda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94fda-105">DESCRIPTION</span></span>
<span data-ttu-id="94fda-106">Cmdleten **Remove-AzureVMDscExtension** tar bort ett Azure DSC-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="94fda-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="94fda-107">Utdata från denna cmdlet måste vara piped till cmdleten **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="94fda-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="94fda-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94fda-108">EXAMPLES</span></span>

### <span data-ttu-id="94fda-109">Exempel 1: ta bort ett DSC-tillägg från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="94fda-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="94fda-110">Det här kommandot tar bort ett Azure DSC-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="94fda-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="94fda-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94fda-111">PARAMETERS</span></span>

### <span data-ttu-id="94fda-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="94fda-112">-InformationAction</span></span>
<span data-ttu-id="94fda-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="94fda-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="94fda-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="94fda-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94fda-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="94fda-115">Continue</span></span>
- <span data-ttu-id="94fda-116">Över</span><span class="sxs-lookup"><span data-stu-id="94fda-116">Ignore</span></span>
- <span data-ttu-id="94fda-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="94fda-117">Inquire</span></span>
- <span data-ttu-id="94fda-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="94fda-118">SilentlyContinue</span></span>
- <span data-ttu-id="94fda-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="94fda-119">Stop</span></span>
- <span data-ttu-id="94fda-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="94fda-120">Suspend</span></span>

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

### <span data-ttu-id="94fda-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="94fda-121">-InformationVariable</span></span>
<span data-ttu-id="94fda-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="94fda-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="94fda-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="94fda-123">-Profile</span></span>
<span data-ttu-id="94fda-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="94fda-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="94fda-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="94fda-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="94fda-126">-VM</span><span class="sxs-lookup"><span data-stu-id="94fda-126">-VM</span></span>
<span data-ttu-id="94fda-127">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="94fda-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="94fda-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94fda-128">-Confirm</span></span>
<span data-ttu-id="94fda-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94fda-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94fda-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94fda-130">-WhatIf</span></span>
<span data-ttu-id="94fda-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94fda-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94fda-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94fda-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94fda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fda-133">CommonParameters</span></span>
<span data-ttu-id="94fda-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94fda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fda-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94fda-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fda-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94fda-136">INPUTS</span></span>

## <span data-ttu-id="94fda-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94fda-137">OUTPUTS</span></span>

## <span data-ttu-id="94fda-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94fda-138">NOTES</span></span>

## <span data-ttu-id="94fda-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94fda-139">RELATED LINKS</span></span>

[<span data-ttu-id="94fda-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="94fda-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="94fda-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="94fda-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="94fda-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="94fda-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


