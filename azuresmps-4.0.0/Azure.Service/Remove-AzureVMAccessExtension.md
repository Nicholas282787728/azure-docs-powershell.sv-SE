---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093236"
---
# <span data-ttu-id="3dfa5-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3dfa5-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="3dfa5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dfa5-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfa5-103">Tar bort tillägget VMAccess som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="3dfa5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dfa5-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3dfa5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dfa5-105">DESCRIPTION</span></span>
<span data-ttu-id="3dfa5-106">Cmdleten **Remove-AzureVMAccessExtension** tar bort tillägget VMAccess som används på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="3dfa5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dfa5-107">EXAMPLES</span></span>

### <span data-ttu-id="3dfa5-108">Exempel 1: ta bort ett VMAccess-tillägg från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="3dfa5-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="3dfa5-109">Det här kommandot tar bort ett VMAccess-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="3dfa5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dfa5-110">PARAMETERS</span></span>

### <span data-ttu-id="3dfa5-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3dfa5-111">-InformationAction</span></span>
<span data-ttu-id="3dfa5-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3dfa5-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3dfa5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3dfa5-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="3dfa5-114">Continue</span></span>
- <span data-ttu-id="3dfa5-115">Över</span><span class="sxs-lookup"><span data-stu-id="3dfa5-115">Ignore</span></span>
- <span data-ttu-id="3dfa5-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="3dfa5-116">Inquire</span></span>
- <span data-ttu-id="3dfa5-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3dfa5-117">SilentlyContinue</span></span>
- <span data-ttu-id="3dfa5-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="3dfa5-118">Stop</span></span>
- <span data-ttu-id="3dfa5-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3dfa5-119">Suspend</span></span>

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

### <span data-ttu-id="3dfa5-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3dfa5-120">-InformationVariable</span></span>
<span data-ttu-id="3dfa5-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3dfa5-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="3dfa5-122">-Profile</span></span>
<span data-ttu-id="3dfa5-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3dfa5-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3dfa5-125">-VM</span><span class="sxs-lookup"><span data-stu-id="3dfa5-125">-VM</span></span>
<span data-ttu-id="3dfa5-126">Anger det beständiga virtuella dator objekt som denna cmdlet tar bort VMAccess-tillägget från.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="3dfa5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfa5-127">CommonParameters</span></span>
<span data-ttu-id="3dfa5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfa5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfa5-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfa5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfa5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dfa5-130">INPUTS</span></span>

## <span data-ttu-id="3dfa5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dfa5-131">OUTPUTS</span></span>

## <span data-ttu-id="3dfa5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dfa5-132">NOTES</span></span>

## <span data-ttu-id="3dfa5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dfa5-133">RELATED LINKS</span></span>

[<span data-ttu-id="3dfa5-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3dfa5-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="3dfa5-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3dfa5-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


