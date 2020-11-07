---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575735"
---
# <span data-ttu-id="46359-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="46359-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46359-102">SYNOPSIS</span></span>
<span data-ttu-id="46359-103">Startar ett Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="46359-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46359-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46359-104">SYNTAX</span></span>

### <span data-ttu-id="46359-105">ByAsynchronousReturnJob (standard)</span><span class="sxs-lookup"><span data-stu-id="46359-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46359-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="46359-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46359-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46359-107">DESCRIPTION</span></span>
<span data-ttu-id="46359-108">**Start-AzureRmAutomationRunbook** cmdlet startar ett Azure Automation Runbook-jobb.</span><span class="sxs-lookup"><span data-stu-id="46359-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="46359-109">Ange ID eller namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="46359-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="46359-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46359-110">EXAMPLES</span></span>

### <span data-ttu-id="46359-111">Exempel 1: starta ett Runbook-jobb</span><span class="sxs-lookup"><span data-stu-id="46359-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="46359-112">Det här kommandot startar ett Runbook-jobb för Runbook med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="46359-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="46359-113">Exempel 2: starta ett Runbook-jobb och vänta med resultat</span><span class="sxs-lookup"><span data-stu-id="46359-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="46359-114">Det här kommandot startar ett Runbook-jobb för Runbook med namnet Runbk01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="46359-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="46359-115">Det här kommandot anger parametern _wait_ .</span><span class="sxs-lookup"><span data-stu-id="46359-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="46359-116">Därför returneras resultatet när jobbet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="46359-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="46359-117">Cmdleten väntar upp till 1000 sekunder för resultaten.</span><span class="sxs-lookup"><span data-stu-id="46359-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="46359-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46359-118">PARAMETERS</span></span>

### <span data-ttu-id="46359-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="46359-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="46359-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46359-120">-DefaultProfile</span></span>
<span data-ttu-id="46359-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="46359-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46359-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="46359-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="46359-123">Anger antalet sekunder som denna cmdlet väntar innan jobbet avbryts.</span><span class="sxs-lookup"><span data-stu-id="46359-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="46359-124">Standardvärdet är 10800 eller tre timmar.</span><span class="sxs-lookup"><span data-stu-id="46359-124">The default value is 10800, or three hours.</span></span>

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46359-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="46359-125">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46359-126">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="46359-126">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46359-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46359-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="46359-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="46359-128">-RunOn</span></span>
<span data-ttu-id="46359-129">Anger vilken hybrid Worker-grupp som Runbook ska köras på.</span><span class="sxs-lookup"><span data-stu-id="46359-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46359-130">-Vänta</span><span class="sxs-lookup"><span data-stu-id="46359-130">-Wait</span></span>
<span data-ttu-id="46359-131">Anger att denna cmdlet väntar på att jobbet ska slutföras, inaktive ras eller Miss lyckas och sedan återgår till Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46359-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46359-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46359-132">CommonParameters</span></span>
<span data-ttu-id="46359-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46359-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46359-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46359-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46359-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46359-135">INPUTS</span></span>

### <span data-ttu-id="46359-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="46359-136">None</span></span>
<span data-ttu-id="46359-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="46359-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46359-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46359-138">OUTPUTS</span></span>

### <span data-ttu-id="46359-139">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="46359-139">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="46359-140">Denna cmdlet returnerar ett **Job** -objekt om du inte anger parametern _wait_ .</span><span class="sxs-lookup"><span data-stu-id="46359-140">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="46359-141">Om du inte anger _vänta_ returneras ett **jobb** objekt omedelbart av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46359-141">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="46359-142">Om du anger _vänta_ slutförs jobbet och resultatet returneras.</span><span class="sxs-lookup"><span data-stu-id="46359-142">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="46359-143">Resultatet är inte ett **Job** -objekt.</span><span class="sxs-lookup"><span data-stu-id="46359-143">The result is not a **Job** object.</span></span>

## <span data-ttu-id="46359-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46359-144">NOTES</span></span>

## <span data-ttu-id="46359-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46359-145">RELATED LINKS</span></span>

[<span data-ttu-id="46359-146">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-148">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-149">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-150">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-151">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="46359-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="46359-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)