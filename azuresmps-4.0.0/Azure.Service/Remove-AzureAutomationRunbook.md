---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099401"
---
# <span data-ttu-id="169a2-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="169a2-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="169a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="169a2-102">SYNOPSIS</span></span>

<span data-ttu-id="169a2-103">Tar bort en Runbook.</span><span class="sxs-lookup"><span data-stu-id="169a2-103">Removes a runbook.</span></span>

## <span data-ttu-id="169a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="169a2-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="169a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="169a2-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="169a2-106">Cmdleten **Remove-AzureAutomationRunbook** tar bort en Runbook från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="169a2-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="169a2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="169a2-107">EXAMPLES</span></span>

### <span data-ttu-id="169a2-108">Exempel 1: ta bort en Runbook</span><span class="sxs-lookup"><span data-stu-id="169a2-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="169a2-109">Det här kommandot tar bort Runbook-flödet som heter MyRunbook i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="169a2-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="169a2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="169a2-110">PARAMETERS</span></span>

### <span data-ttu-id="169a2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="169a2-111">-AutomationAccountName</span></span>
<span data-ttu-id="169a2-112">Anger namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="169a2-112">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169a2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="169a2-113">-Force</span></span>
<span data-ttu-id="169a2-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="169a2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169a2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="169a2-115">-Name</span></span>
<span data-ttu-id="169a2-116">Anger namnet på den Runbook som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="169a2-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169a2-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="169a2-117">-Profile</span></span>
<span data-ttu-id="169a2-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="169a2-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="169a2-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="169a2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="169a2-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="169a2-120">-Confirm</span></span>
<span data-ttu-id="169a2-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="169a2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="169a2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="169a2-122">-WhatIf</span></span>
<span data-ttu-id="169a2-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="169a2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="169a2-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="169a2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="169a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169a2-125">CommonParameters</span></span>
<span data-ttu-id="169a2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169a2-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169a2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169a2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="169a2-128">INPUTS</span></span>

## <span data-ttu-id="169a2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="169a2-129">OUTPUTS</span></span>

## <span data-ttu-id="169a2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="169a2-130">NOTES</span></span>

## <span data-ttu-id="169a2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="169a2-131">RELATED LINKS</span></span>

[<span data-ttu-id="169a2-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="169a2-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="169a2-133">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="169a2-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="169a2-134">Publicera – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="169a2-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="169a2-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="169a2-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="169a2-136">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="169a2-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


