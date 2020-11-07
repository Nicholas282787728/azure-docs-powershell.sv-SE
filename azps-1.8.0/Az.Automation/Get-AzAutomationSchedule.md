---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: 237cd5dfa3ae64273361bb2f79f301ffa93dd29c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754833"
---
# <span data-ttu-id="dcfab-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcfab-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="dcfab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcfab-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfab-103">Får ett Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="dcfab-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="dcfab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcfab-104">SYNTAX</span></span>

### <span data-ttu-id="dcfab-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="dcfab-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcfab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dcfab-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcfab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcfab-107">DESCRIPTION</span></span>
<span data-ttu-id="dcfab-108">Cmdleten **Get-AzAutomationSchedule** får ett Azure Automation-schema.</span><span class="sxs-lookup"><span data-stu-id="dcfab-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="dcfab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcfab-109">EXAMPLES</span></span>

### <span data-ttu-id="dcfab-110">Exempel 1: få ett schema</span><span class="sxs-lookup"><span data-stu-id="dcfab-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dcfab-111">Det här kommandot får schemat med namnet DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="dcfab-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="dcfab-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcfab-112">PARAMETERS</span></span>

### <span data-ttu-id="dcfab-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dcfab-113">-AutomationAccountName</span></span>
<span data-ttu-id="dcfab-114">Anger namnet på ett Automation-konto som denna cmdlet får ett schema för.</span><span class="sxs-lookup"><span data-stu-id="dcfab-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="dcfab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfab-115">-DefaultProfile</span></span>
<span data-ttu-id="dcfab-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dcfab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcfab-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcfab-117">-Name</span></span>
<span data-ttu-id="dcfab-118">Anger namnet på ett schema som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="dcfab-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcfab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcfab-119">-ResourceGroupName</span></span>
<span data-ttu-id="dcfab-120">Anger namnet på en resurs grupp för vilken denna cmdlet får ett schema.</span><span class="sxs-lookup"><span data-stu-id="dcfab-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="dcfab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfab-121">CommonParameters</span></span>
<span data-ttu-id="dcfab-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcfab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfab-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcfab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfab-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcfab-124">INPUTS</span></span>

### <span data-ttu-id="dcfab-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dcfab-125">System.String</span></span>

## <span data-ttu-id="dcfab-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcfab-126">OUTPUTS</span></span>

### <span data-ttu-id="dcfab-127">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="dcfab-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="dcfab-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcfab-128">NOTES</span></span>

## <span data-ttu-id="dcfab-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcfab-129">RELATED LINKS</span></span>

[<span data-ttu-id="dcfab-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcfab-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="dcfab-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcfab-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="dcfab-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dcfab-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


