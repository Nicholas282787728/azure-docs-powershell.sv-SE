---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: d56b631f106ef4984a81a8911af26288f720cac7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754754"
---
# <span data-ttu-id="7ab50-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ab50-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="7ab50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ab50-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab50-103">Tar bort ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="7ab50-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="7ab50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ab50-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab50-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ab50-105">DESCRIPTION</span></span>
<span data-ttu-id="7ab50-106">Cmdleten **Remove-AzAutomationSchedule** tar bort ett schema från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7ab50-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="7ab50-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ab50-107">EXAMPLES</span></span>

### <span data-ttu-id="7ab50-108">Exempel 1: ta bort ett schema</span><span class="sxs-lookup"><span data-stu-id="7ab50-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7ab50-109">Det här kommandot tar bort schemat med namnet Schedule01 i Automation-konto Contoso17 i resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7ab50-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7ab50-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ab50-110">PARAMETERS</span></span>

### <span data-ttu-id="7ab50-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ab50-111">-AutomationAccountName</span></span>
<span data-ttu-id="7ab50-112">Anger namnet på ett Automation-konto som denna cmdlet tar bort ett schema för.</span><span class="sxs-lookup"><span data-stu-id="7ab50-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab50-113">-DefaultProfile</span></span>
<span data-ttu-id="7ab50-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7ab50-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7ab50-115">-Force</span></span>
<span data-ttu-id="7ab50-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7ab50-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ab50-117">-Name</span></span>
<span data-ttu-id="7ab50-118">Anger namnet på det schema som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="7ab50-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab50-119">-ResourceGroupName</span></span>
<span data-ttu-id="7ab50-120">Anger namnet på en resurs grupp för vilken denna cmdlet tar bort ett schema.</span><span class="sxs-lookup"><span data-stu-id="7ab50-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ab50-121">-Confirm</span></span>
<span data-ttu-id="7ab50-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ab50-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab50-123">-WhatIf</span></span>
<span data-ttu-id="7ab50-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ab50-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab50-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ab50-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab50-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab50-126">CommonParameters</span></span>
<span data-ttu-id="7ab50-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab50-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab50-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab50-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab50-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ab50-129">INPUTS</span></span>

### <span data-ttu-id="7ab50-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ab50-130">System.String</span></span>

## <span data-ttu-id="7ab50-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ab50-131">OUTPUTS</span></span>

### <span data-ttu-id="7ab50-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="7ab50-132">System.Void</span></span>

## <span data-ttu-id="7ab50-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ab50-133">NOTES</span></span>

## <span data-ttu-id="7ab50-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ab50-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ab50-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ab50-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="7ab50-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ab50-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="7ab50-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7ab50-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


