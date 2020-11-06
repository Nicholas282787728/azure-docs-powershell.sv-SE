---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: cce9b4eff96be34521af58ec85f7abb93d39b3cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580876"
---
# <span data-ttu-id="67724-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="67724-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="67724-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67724-102">SYNOPSIS</span></span>
<span data-ttu-id="67724-103">Tar bort ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="67724-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67724-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67724-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67724-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67724-105">DESCRIPTION</span></span>
<span data-ttu-id="67724-106">Cmdleten **Remove-AzureRmAutomationSchedule** tar bort ett schema från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="67724-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="67724-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67724-107">EXAMPLES</span></span>

### <span data-ttu-id="67724-108">Exempel 1: ta bort ett schema</span><span class="sxs-lookup"><span data-stu-id="67724-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="67724-109">Det här kommandot tar bort schemat med namnet Schedule01 i Automation-konto Contoso17 i resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="67724-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="67724-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67724-110">PARAMETERS</span></span>

### <span data-ttu-id="67724-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67724-111">-AutomationAccountName</span></span>
<span data-ttu-id="67724-112">Anger namnet på ett Automation-konto som denna cmdlet tar bort ett schema för.</span><span class="sxs-lookup"><span data-stu-id="67724-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="67724-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67724-113">-DefaultProfile</span></span>
<span data-ttu-id="67724-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="67724-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67724-115">-Force</span><span class="sxs-lookup"><span data-stu-id="67724-115">-Force</span></span>
<span data-ttu-id="67724-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="67724-116">ps_force</span></span>

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

### <span data-ttu-id="67724-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="67724-117">-Name</span></span>
<span data-ttu-id="67724-118">Anger namnet på det schema som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="67724-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="67724-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67724-119">-ResourceGroupName</span></span>
<span data-ttu-id="67724-120">Anger namnet på en resurs grupp för vilken denna cmdlet tar bort ett schema.</span><span class="sxs-lookup"><span data-stu-id="67724-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="67724-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67724-121">-Confirm</span></span>
<span data-ttu-id="67724-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67724-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67724-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67724-123">-WhatIf</span></span>
<span data-ttu-id="67724-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67724-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67724-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67724-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67724-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67724-126">CommonParameters</span></span>
<span data-ttu-id="67724-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67724-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67724-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67724-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67724-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67724-129">INPUTS</span></span>

### <span data-ttu-id="67724-130">System. String</span><span class="sxs-lookup"><span data-stu-id="67724-130">System.String</span></span>

## <span data-ttu-id="67724-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67724-131">OUTPUTS</span></span>

### <span data-ttu-id="67724-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="67724-132">System.Void</span></span>

## <span data-ttu-id="67724-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67724-133">NOTES</span></span>

## <span data-ttu-id="67724-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67724-134">RELATED LINKS</span></span>

[<span data-ttu-id="67724-135">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="67724-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="67724-136">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="67724-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="67724-137">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="67724-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


