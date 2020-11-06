---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579812"
---
# <span data-ttu-id="3aa66-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3aa66-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="3aa66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3aa66-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa66-103">Tar bort ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="3aa66-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aa66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3aa66-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3aa66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3aa66-105">DESCRIPTION</span></span>
<span data-ttu-id="3aa66-106">Cmdleten **Remove-AzureRmAutomationSchedule** tar bort ett schema från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3aa66-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="3aa66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3aa66-107">EXAMPLES</span></span>

### <span data-ttu-id="3aa66-108">Exempel 1: ta bort ett schema</span><span class="sxs-lookup"><span data-stu-id="3aa66-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3aa66-109">Det här kommandot ändrar beskrivningen av schemat som heter Schedule01.</span><span class="sxs-lookup"><span data-stu-id="3aa66-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="3aa66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3aa66-110">PARAMETERS</span></span>

### <span data-ttu-id="3aa66-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3aa66-111">-AutomationAccountName</span></span>
<span data-ttu-id="3aa66-112">Anger namnet på ett Automation-konto som denna cmdlet ändrar ett schema för.</span><span class="sxs-lookup"><span data-stu-id="3aa66-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="3aa66-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3aa66-113">-Force</span></span>
<span data-ttu-id="3aa66-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="3aa66-114">ps_force</span></span>

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

### <span data-ttu-id="3aa66-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3aa66-115">-Name</span></span>
<span data-ttu-id="3aa66-116">Anger namnet på det schema som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="3aa66-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3aa66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa66-117">-ResourceGroupName</span></span>
<span data-ttu-id="3aa66-118">Anger namnet på en resurs grupp för vilken denna cmdlet tar bort ett schema.</span><span class="sxs-lookup"><span data-stu-id="3aa66-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="3aa66-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3aa66-119">-Confirm</span></span>
<span data-ttu-id="3aa66-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3aa66-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa66-121">-WhatIf</span></span>
<span data-ttu-id="3aa66-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3aa66-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aa66-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3aa66-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa66-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa66-124">-DefaultProfile</span></span>
<span data-ttu-id="3aa66-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa66-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aa66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa66-126">CommonParameters</span></span>
<span data-ttu-id="3aa66-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa66-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa66-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa66-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3aa66-129">INPUTS</span></span>

## <span data-ttu-id="3aa66-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3aa66-130">OUTPUTS</span></span>

## <span data-ttu-id="3aa66-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3aa66-131">NOTES</span></span>

## <span data-ttu-id="3aa66-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3aa66-132">RELATED LINKS</span></span>

[<span data-ttu-id="3aa66-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3aa66-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3aa66-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3aa66-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3aa66-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3aa66-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


