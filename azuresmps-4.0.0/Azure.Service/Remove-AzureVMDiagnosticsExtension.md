---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093230"
---
# <span data-ttu-id="8785e-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8785e-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="8785e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8785e-102">SYNOPSIS</span></span>
<span data-ttu-id="8785e-103">Tar bort Azure Diagnostics-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8785e-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="8785e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8785e-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8785e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8785e-105">DESCRIPTION</span></span>
<span data-ttu-id="8785e-106">Cmdleten **Remove-AzureVMDiagnosticsExtension** tar bort ett Microsoft Azure Diagnostics-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8785e-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="8785e-107">Du måste skicka utdata från denna cmdlet till cmdleten **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8785e-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="8785e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8785e-108">EXAMPLES</span></span>

### <span data-ttu-id="8785e-109">Exempel 1: ta bort Azure Diagnostics-tillägget från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="8785e-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="8785e-110">Det här kommandot tar bort Azure Diagnostics-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8785e-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="8785e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8785e-111">PARAMETERS</span></span>

### <span data-ttu-id="8785e-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8785e-112">-InformationAction</span></span>
<span data-ttu-id="8785e-113">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="8785e-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8785e-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8785e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8785e-115">Vidare</span><span class="sxs-lookup"><span data-stu-id="8785e-115">Continue</span></span>
- <span data-ttu-id="8785e-116">Över</span><span class="sxs-lookup"><span data-stu-id="8785e-116">Ignore</span></span>
- <span data-ttu-id="8785e-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="8785e-117">Inquire</span></span>
- <span data-ttu-id="8785e-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8785e-118">SilentlyContinue</span></span>
- <span data-ttu-id="8785e-119">Stanna</span><span class="sxs-lookup"><span data-stu-id="8785e-119">Stop</span></span>
- <span data-ttu-id="8785e-120">Avbryt</span><span class="sxs-lookup"><span data-stu-id="8785e-120">Suspend</span></span>

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

### <span data-ttu-id="8785e-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8785e-121">-InformationVariable</span></span>
<span data-ttu-id="8785e-122">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="8785e-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8785e-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="8785e-123">-Profile</span></span>
<span data-ttu-id="8785e-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="8785e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8785e-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="8785e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8785e-126">-VM</span><span class="sxs-lookup"><span data-stu-id="8785e-126">-VM</span></span>
<span data-ttu-id="8785e-127">Anger permanent virtuell dator-objekt.</span><span class="sxs-lookup"><span data-stu-id="8785e-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8785e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8785e-128">CommonParameters</span></span>
<span data-ttu-id="8785e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8785e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8785e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8785e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8785e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8785e-131">INPUTS</span></span>

## <span data-ttu-id="8785e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8785e-132">OUTPUTS</span></span>

## <span data-ttu-id="8785e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8785e-133">NOTES</span></span>

## <span data-ttu-id="8785e-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8785e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8785e-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8785e-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="8785e-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="8785e-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="8785e-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8785e-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


