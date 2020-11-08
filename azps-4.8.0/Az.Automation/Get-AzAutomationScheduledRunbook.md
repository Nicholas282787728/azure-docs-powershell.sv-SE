---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260377"
---
# <span data-ttu-id="fd916-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="fd916-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="fd916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd916-102">SYNOPSIS</span></span>
<span data-ttu-id="fd916-103">Hämtar automatiserade Runbooks och associerade scheman.</span><span class="sxs-lookup"><span data-stu-id="fd916-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="fd916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd916-104">SYNTAX</span></span>

### <span data-ttu-id="fd916-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="fd916-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd916-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="fd916-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd916-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="fd916-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd916-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="fd916-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd916-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="fd916-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd916-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd916-110">DESCRIPTION</span></span>
<span data-ttu-id="fd916-111">Cmdleten **Get-AzAutomationScheduledRunbook** hämtar en eller flera Azure Automation-runbooks och tillhör ande scheman.</span><span class="sxs-lookup"><span data-stu-id="fd916-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="fd916-112">Denna cmdlet hämtar som standard alla schemalagda Runbooks.</span><span class="sxs-lookup"><span data-stu-id="fd916-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="fd916-113">Ange namnet på en Runbook eller ett schema eller båda för att visa specifika Runbook-scheman.</span><span class="sxs-lookup"><span data-stu-id="fd916-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="fd916-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd916-114">EXAMPLES</span></span>

### <span data-ttu-id="fd916-115">Exempel 1: få alla schemalagda Runbooks</span><span class="sxs-lookup"><span data-stu-id="fd916-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fd916-116">Det här kommandot får alla schemalagda Runbooks i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fd916-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="fd916-117">Exempel 2: Hämta alla scheman som är kopplade till en Runbook</span><span class="sxs-lookup"><span data-stu-id="fd916-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="fd916-118">Med det här kommandot hämtas alla schemalagda Runbooks för Runbook-Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fd916-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="fd916-119">Exempel 3: Hämta alla Runbooks som är kopplade till ett schema</span><span class="sxs-lookup"><span data-stu-id="fd916-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="fd916-120">Med det här kommandot hämtas alla schemalagda Runbooks för schemaläggning Schedule01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fd916-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fd916-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd916-121">PARAMETERS</span></span>

### <span data-ttu-id="fd916-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd916-122">-AutomationAccountName</span></span>
<span data-ttu-id="fd916-123">Anger ett Automation-konto för den Runbook som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="fd916-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fd916-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd916-124">-DefaultProfile</span></span>
<span data-ttu-id="fd916-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fd916-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd916-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="fd916-126">-JobScheduleId</span></span>
<span data-ttu-id="fd916-127">Anger ID för ett schemalagt jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="fd916-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd916-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd916-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd916-129">Anger namnet på en resurs grupp för schemalagda Runbooks som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="fd916-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fd916-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="fd916-130">-RunbookName</span></span>
<span data-ttu-id="fd916-131">Anger namnet på en Runbook som denna cmdlet får schemalagda Runbooks för.</span><span class="sxs-lookup"><span data-stu-id="fd916-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd916-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="fd916-132">-ScheduleName</span></span>
<span data-ttu-id="fd916-133">Anger namnet på ett schema som denna cmdlet ska schemalägga Runbooks för.</span><span class="sxs-lookup"><span data-stu-id="fd916-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd916-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd916-134">CommonParameters</span></span>
<span data-ttu-id="fd916-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd916-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd916-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd916-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd916-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd916-137">INPUTS</span></span>

### <span data-ttu-id="fd916-138">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd916-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd916-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fd916-139">System.String</span></span>

## <span data-ttu-id="fd916-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd916-140">OUTPUTS</span></span>

### <span data-ttu-id="fd916-141">Microsoft. Azure. commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="fd916-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="fd916-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd916-142">NOTES</span></span>

## <span data-ttu-id="fd916-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd916-143">RELATED LINKS</span></span>

[<span data-ttu-id="fd916-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="fd916-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="fd916-145">Avregistrera-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="fd916-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


