---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099678"
---
# <span data-ttu-id="5924e-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5924e-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="5924e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5924e-102">SYNOPSIS</span></span>
<span data-ttu-id="5924e-103">Tar bort tillägget för anpassat skript från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5924e-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="5924e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5924e-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5924e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5924e-105">DESCRIPTION</span></span>
<span data-ttu-id="5924e-106">Cmdleten **Remove-AzureVMCustomScriptExtension** tar bort det anpassade skript tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5924e-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="5924e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5924e-107">EXAMPLES</span></span>

### <span data-ttu-id="5924e-108">Exempel 1: ta bort ett anpassat skript tillägg för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5924e-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="5924e-109">Det här kommandot tar bort det anpassade skript tillägget för Azure Virtual Machine från den angivna virtuella datorn enligt variabeln $VM.</span><span class="sxs-lookup"><span data-stu-id="5924e-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="5924e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5924e-110">PARAMETERS</span></span>

### <span data-ttu-id="5924e-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5924e-111">-InformationAction</span></span>
<span data-ttu-id="5924e-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="5924e-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5924e-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5924e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5924e-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="5924e-114">Continue</span></span>
- <span data-ttu-id="5924e-115">Över</span><span class="sxs-lookup"><span data-stu-id="5924e-115">Ignore</span></span>
- <span data-ttu-id="5924e-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="5924e-116">Inquire</span></span>
- <span data-ttu-id="5924e-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5924e-117">SilentlyContinue</span></span>
- <span data-ttu-id="5924e-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="5924e-118">Stop</span></span>
- <span data-ttu-id="5924e-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="5924e-119">Suspend</span></span>

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

### <span data-ttu-id="5924e-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5924e-120">-InformationVariable</span></span>
<span data-ttu-id="5924e-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="5924e-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5924e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5924e-122">-Profile</span></span>
<span data-ttu-id="5924e-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5924e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5924e-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5924e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5924e-125">-VM</span><span class="sxs-lookup"><span data-stu-id="5924e-125">-VM</span></span>
<span data-ttu-id="5924e-126">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="5924e-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5924e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5924e-127">CommonParameters</span></span>
<span data-ttu-id="5924e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5924e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5924e-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5924e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5924e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5924e-130">INPUTS</span></span>

## <span data-ttu-id="5924e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5924e-131">OUTPUTS</span></span>

## <span data-ttu-id="5924e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5924e-132">NOTES</span></span>

## <span data-ttu-id="5924e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5924e-133">RELATED LINKS</span></span>

[<span data-ttu-id="5924e-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5924e-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="5924e-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5924e-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


