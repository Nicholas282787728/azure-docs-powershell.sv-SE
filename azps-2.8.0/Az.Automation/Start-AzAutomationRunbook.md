---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 2f9b5354731a64a5cb614e173aa45be5349197d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745446"
---
# <span data-ttu-id="43993-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="43993-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43993-102">SYNOPSIS</span></span>
<span data-ttu-id="43993-103">Startar ett Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="43993-103">Starts a runbook job.</span></span>

## <span data-ttu-id="43993-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43993-104">SYNTAX</span></span>

### <span data-ttu-id="43993-105">ByAsynchronousReturnJob (standard)</span><span class="sxs-lookup"><span data-stu-id="43993-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43993-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="43993-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43993-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43993-107">DESCRIPTION</span></span>
<span data-ttu-id="43993-108">**Start-AzAutomationRunbook** cmdlet startar ett Azure Automation Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="43993-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="43993-109">Ange ID eller namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="43993-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="43993-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43993-110">EXAMPLES</span></span>

### <span data-ttu-id="43993-111">Exempel 1: starta ett Runbook-jobb</span><span class="sxs-lookup"><span data-stu-id="43993-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43993-112">Det här kommandot startar ett Runbook-jobb för Runbook med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43993-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="43993-113">Exempel 2: starta ett Finplanerat 2-Runbook-jobb med parametrar</span><span class="sxs-lookup"><span data-stu-id="43993-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="43993-114">Det här kommandot startar ett Runbook-jobb för den "python 2" Runbook med namnet RunbkPy01 i Azure Automation-kontot med namnet Contoso17 med "ValueForPosition1" som den första positions parametern och "ValueForPosition2" för den andra.</span><span class="sxs-lookup"><span data-stu-id="43993-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="43993-115">Exempel 3: starta ett Runbook-jobb och vänta med resultat</span><span class="sxs-lookup"><span data-stu-id="43993-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="43993-116">Det här kommandot startar ett Runbook-jobb för Runbook med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43993-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="43993-117">Det här kommandot anger parametern _wait_ .</span><span class="sxs-lookup"><span data-stu-id="43993-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="43993-118">Därför returneras resultatet när jobbet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="43993-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="43993-119">Cmdleten väntar upp till 1000 sekunder för resultaten.</span><span class="sxs-lookup"><span data-stu-id="43993-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="43993-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43993-120">PARAMETERS</span></span>

### <span data-ttu-id="43993-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43993-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="43993-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43993-122">-DefaultProfile</span></span>
<span data-ttu-id="43993-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="43993-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43993-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="43993-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="43993-125">Anger antalet sekunder som denna cmdlet väntar innan jobbet avbryts.</span><span class="sxs-lookup"><span data-stu-id="43993-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="43993-126">Standardvärdet är 10800 eller tre timmar.</span><span class="sxs-lookup"><span data-stu-id="43993-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43993-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="43993-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43993-128">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="43993-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43993-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43993-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="43993-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="43993-130">-RunOn</span></span>
<span data-ttu-id="43993-131">Anger vilken hybrid Worker-grupp som Runbook ska köras på.</span><span class="sxs-lookup"><span data-stu-id="43993-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43993-132">-Vänta</span><span class="sxs-lookup"><span data-stu-id="43993-132">-Wait</span></span>
<span data-ttu-id="43993-133">Anger att denna cmdlet väntar på att jobbet ska slutföras, inaktive ras eller Miss lyckas och sedan återgår till Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43993-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43993-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43993-134">CommonParameters</span></span>
<span data-ttu-id="43993-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43993-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43993-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43993-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43993-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43993-137">INPUTS</span></span>

### <span data-ttu-id="43993-138">System. String</span><span class="sxs-lookup"><span data-stu-id="43993-138">System.String</span></span>

## <span data-ttu-id="43993-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43993-139">OUTPUTS</span></span>

### <span data-ttu-id="43993-140">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="43993-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="43993-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="43993-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="43993-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43993-142">NOTES</span></span>

## <span data-ttu-id="43993-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43993-143">RELATED LINKS</span></span>

[<span data-ttu-id="43993-144">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="43993-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="43993-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="43993-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="43993-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="43993-149">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="43993-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="43993-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="43993-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
