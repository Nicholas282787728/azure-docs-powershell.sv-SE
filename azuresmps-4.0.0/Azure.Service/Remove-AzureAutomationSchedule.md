---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099400"
---
# <span data-ttu-id="d8827-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d8827-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="d8827-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8827-102">SYNOPSIS</span></span>

<span data-ttu-id="d8827-103">Tar bort ett Azure Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="d8827-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="d8827-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8827-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8827-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8827-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d8827-106">Cmdleten **Remove-AzureAutomationSchedule** tar bort ett schema från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d8827-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d8827-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8827-107">EXAMPLES</span></span>

### <span data-ttu-id="d8827-108">Exempel 1: ta bort ett schema</span><span class="sxs-lookup"><span data-stu-id="d8827-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="d8827-109">Det här kommandot tar bort schemat som heter mina schema.</span><span class="sxs-lookup"><span data-stu-id="d8827-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="d8827-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8827-110">PARAMETERS</span></span>

### <span data-ttu-id="d8827-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8827-111">-AutomationAccountName</span></span>
<span data-ttu-id="d8827-112">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="d8827-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="d8827-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d8827-113">-Force</span></span>
<span data-ttu-id="d8827-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d8827-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8827-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8827-115">-Name</span></span>
<span data-ttu-id="d8827-116">Anger namnet på schemat som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d8827-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="d8827-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8827-117">-Profile</span></span>
<span data-ttu-id="d8827-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d8827-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8827-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d8827-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8827-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8827-120">-Confirm</span></span>
<span data-ttu-id="d8827-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8827-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8827-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8827-122">-WhatIf</span></span>
<span data-ttu-id="d8827-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8827-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8827-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8827-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8827-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8827-125">CommonParameters</span></span>
<span data-ttu-id="d8827-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8827-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8827-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8827-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8827-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8827-128">INPUTS</span></span>

## <span data-ttu-id="d8827-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8827-129">OUTPUTS</span></span>

## <span data-ttu-id="d8827-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8827-130">NOTES</span></span>

## <span data-ttu-id="d8827-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8827-131">RELATED LINKS</span></span>

[<span data-ttu-id="d8827-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d8827-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="d8827-133">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d8827-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="d8827-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d8827-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


