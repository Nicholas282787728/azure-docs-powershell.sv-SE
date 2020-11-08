---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927930"
---
# <span data-ttu-id="90119-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="90119-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="90119-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90119-102">SYNOPSIS</span></span>
<span data-ttu-id="90119-103">Ändrar ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="90119-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="90119-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90119-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90119-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90119-105">DESCRIPTION</span></span>
<span data-ttu-id="90119-106">Cmdleten **set-AzAutomationSchedule** ändrar ett schema i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="90119-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="90119-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90119-107">EXAMPLES</span></span>

### <span data-ttu-id="90119-108">Exempel 1: ändra ett schema</span><span class="sxs-lookup"><span data-stu-id="90119-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="90119-109">Det här kommandot ändrar beskrivningen av schemat som heter Schedule01.</span><span class="sxs-lookup"><span data-stu-id="90119-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="90119-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90119-110">PARAMETERS</span></span>

### <span data-ttu-id="90119-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90119-111">-AutomationAccountName</span></span>
<span data-ttu-id="90119-112">Anger namnet på ett Automation-konto som denna cmdlet ändrar ett schema för.</span><span class="sxs-lookup"><span data-stu-id="90119-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="90119-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90119-113">-DefaultProfile</span></span>
<span data-ttu-id="90119-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="90119-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90119-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="90119-115">-Description</span></span>
<span data-ttu-id="90119-116">Anger en beskrivning av schemat.</span><span class="sxs-lookup"><span data-stu-id="90119-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90119-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="90119-117">-IsEnabled</span></span>
<span data-ttu-id="90119-118">Anger om denna cmdlet aktiverar schemat.</span><span class="sxs-lookup"><span data-stu-id="90119-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90119-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="90119-119">-Name</span></span>
<span data-ttu-id="90119-120">Anger namnet på det schema som den här cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="90119-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90119-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90119-121">-ResourceGroupName</span></span>
<span data-ttu-id="90119-122">Anger namnet på en resurs grupp för vilken denna cmdlet ändrar ett schema.</span><span class="sxs-lookup"><span data-stu-id="90119-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="90119-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90119-123">CommonParameters</span></span>
<span data-ttu-id="90119-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90119-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90119-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90119-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90119-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90119-126">INPUTS</span></span>

### <span data-ttu-id="90119-127">System. String</span><span class="sxs-lookup"><span data-stu-id="90119-127">System.String</span></span>

### <span data-ttu-id="90119-128">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90119-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="90119-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90119-129">OUTPUTS</span></span>

### <span data-ttu-id="90119-130">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="90119-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="90119-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90119-131">NOTES</span></span>

## <span data-ttu-id="90119-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90119-132">RELATED LINKS</span></span>

[<span data-ttu-id="90119-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="90119-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="90119-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="90119-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="90119-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="90119-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

