---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: 459c217904ba44662d18c81c4c493a3b7f2033e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577263"
---
# <span data-ttu-id="24901-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="24901-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="24901-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24901-102">SYNOPSIS</span></span>
<span data-ttu-id="24901-103">Hämtar automatiserade Runbooks och associerade scheman.</span><span class="sxs-lookup"><span data-stu-id="24901-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24901-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24901-104">SYNTAX</span></span>

### <span data-ttu-id="24901-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="24901-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24901-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="24901-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24901-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="24901-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24901-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="24901-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24901-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="24901-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24901-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24901-110">DESCRIPTION</span></span>
<span data-ttu-id="24901-111">Cmdleten **Get-AzureRmAutomationScheduledRunbook** hämtar en eller flera Azure Automation-runbooks och tillhör ande scheman.</span><span class="sxs-lookup"><span data-stu-id="24901-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="24901-112">Denna cmdlet hämtar som standard alla schemalagda Runbooks.</span><span class="sxs-lookup"><span data-stu-id="24901-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="24901-113">Ange namnet på en Runbook eller ett schema eller båda för att visa specifika Runbook-scheman.</span><span class="sxs-lookup"><span data-stu-id="24901-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="24901-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24901-114">EXAMPLES</span></span>

### <span data-ttu-id="24901-115">Exempel 1: få alla schemalagda Runbooks</span><span class="sxs-lookup"><span data-stu-id="24901-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="24901-116">Det här kommandot får alla schemalagda Runbooks i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="24901-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="24901-117">Exempel 2: Hämta alla scheman som är kopplade till en Runbook</span><span class="sxs-lookup"><span data-stu-id="24901-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="24901-118">Med det här kommandot hämtas alla schemalagda Runbooks för Runbook-Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="24901-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="24901-119">Exempel 3: Hämta alla Runbooks som är kopplade till ett schema</span><span class="sxs-lookup"><span data-stu-id="24901-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="24901-120">Med det här kommandot hämtas alla schemalagda Runbooks för schemaläggning Schedule01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="24901-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="24901-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24901-121">PARAMETERS</span></span>

### <span data-ttu-id="24901-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24901-122">-AutomationAccountName</span></span>
<span data-ttu-id="24901-123">Anger ett Automation-konto för den Runbook som denna cmdlet körs på.</span><span class="sxs-lookup"><span data-stu-id="24901-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24901-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24901-124">-DefaultProfile</span></span>
<span data-ttu-id="24901-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="24901-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24901-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="24901-126">-JobScheduleId</span></span>
<span data-ttu-id="24901-127">Anger ID för ett schemalagt jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="24901-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24901-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24901-128">-ResourceGroupName</span></span>
<span data-ttu-id="24901-129">Anger namnet på en resurs grupp för schemalagda Runbooks som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="24901-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24901-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="24901-130">-RunbookName</span></span>
<span data-ttu-id="24901-131">Anger namnet på en Runbook som denna cmdlet får schemalagda Runbooks för.</span><span class="sxs-lookup"><span data-stu-id="24901-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24901-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="24901-132">-ScheduleName</span></span>
<span data-ttu-id="24901-133">Anger namnet på ett schema som denna cmdlet ska schemalägga Runbooks för.</span><span class="sxs-lookup"><span data-stu-id="24901-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24901-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24901-134">CommonParameters</span></span>
<span data-ttu-id="24901-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24901-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24901-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24901-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24901-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24901-137">INPUTS</span></span>

### <span data-ttu-id="24901-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="24901-138">None</span></span>
<span data-ttu-id="24901-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="24901-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24901-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24901-140">OUTPUTS</span></span>

### <span data-ttu-id="24901-141">Microsoft. Azure. commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="24901-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="24901-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24901-142">NOTES</span></span>

## <span data-ttu-id="24901-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24901-143">RELATED LINKS</span></span>

[<span data-ttu-id="24901-144">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="24901-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="24901-145">Avregistrera-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="24901-145">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


