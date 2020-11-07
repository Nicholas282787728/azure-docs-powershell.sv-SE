---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 8742b9967720948118f132de23fd07dbfdcb5f0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754861"
---
# <span data-ttu-id="13129-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="13129-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="13129-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13129-102">SYNOPSIS</span></span>
<span data-ttu-id="13129-103">Hämtar DSC-kompilator jobb i Automation.</span><span class="sxs-lookup"><span data-stu-id="13129-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="13129-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13129-104">SYNTAX</span></span>

### <span data-ttu-id="13129-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="13129-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13129-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="13129-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13129-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="13129-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13129-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13129-108">DESCRIPTION</span></span>
<span data-ttu-id="13129-109">Cmdleten **Get-AzAutomationDscCompilationJob** får AP-kompilatorn (Desired State Configuration) i APS för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="13129-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="13129-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13129-110">EXAMPLES</span></span>

### <span data-ttu-id="13129-111">Exempel 1: Hämta alla DSC Compilation-jobb</span><span class="sxs-lookup"><span data-stu-id="13129-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="13129-112">Det här kommandot får alla kompilator jobb i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="13129-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="13129-113">Exempel 2: Hämta DSC-kompilator jobb för en konfiguration</span><span class="sxs-lookup"><span data-stu-id="13129-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="13129-114">Det här kommandot får alla kompilator jobb för DSC-konfigurationen som heter ContosoConfiguration i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="13129-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="13129-115">Exempel 3: Hämta ett specifikt DSC-kompilator jobb</span><span class="sxs-lookup"><span data-stu-id="13129-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="13129-116">Det här kommandot får Compilation Job med angivet ID i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="13129-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="13129-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13129-117">PARAMETERS</span></span>

### <span data-ttu-id="13129-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13129-118">-AutomationAccountName</span></span>
<span data-ttu-id="13129-119">Anger namnet på det Automation-konto som innehåller de DSC Compilation-jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="13129-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="13129-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="13129-120">-ConfigurationName</span></span>
<span data-ttu-id="13129-121">Anger namnet på den DSC-konfiguration för vilken denna cmdlet ska kompilera jobb.</span><span class="sxs-lookup"><span data-stu-id="13129-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13129-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13129-122">-DefaultProfile</span></span>
<span data-ttu-id="13129-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="13129-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13129-124">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="13129-124">-EndTime</span></span>
<span data-ttu-id="13129-125">Anger en slut tid.</span><span class="sxs-lookup"><span data-stu-id="13129-125">Specifies an end time.</span></span>
<span data-ttu-id="13129-126">Denna cmdlet används för att kompilera jobb som startats till den tidpunkt då den här parametern anges.</span><span class="sxs-lookup"><span data-stu-id="13129-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13129-127">-ID</span><span class="sxs-lookup"><span data-stu-id="13129-127">-Id</span></span>
<span data-ttu-id="13129-128">Anger det unika ID: t för det DSC Compilation-jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="13129-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13129-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13129-129">-ResourceGroupName</span></span>
<span data-ttu-id="13129-130">Anger namnet på en resurs grupp där denna cmdlet får DSC Compilation-jobb.</span><span class="sxs-lookup"><span data-stu-id="13129-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="13129-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="13129-131">-StartTime</span></span>
<span data-ttu-id="13129-132">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="13129-132">Specifies a start time.</span></span>
<span data-ttu-id="13129-133">Denna cmdlet hämtar jobb som startar vid eller efter den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="13129-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13129-134">-Status</span><span class="sxs-lookup"><span data-stu-id="13129-134">-Status</span></span>
<span data-ttu-id="13129-135">Anger statusen för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="13129-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="13129-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="13129-136">Valid values are:</span></span> 
- <span data-ttu-id="13129-137">Rätta</span><span class="sxs-lookup"><span data-stu-id="13129-137">Completed</span></span> 
- <span data-ttu-id="13129-138">Startade</span><span class="sxs-lookup"><span data-stu-id="13129-138">Failed</span></span> 
- <span data-ttu-id="13129-139">I kö</span><span class="sxs-lookup"><span data-stu-id="13129-139">Queued</span></span> 
- <span data-ttu-id="13129-140">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="13129-140">Starting</span></span> 
- <span data-ttu-id="13129-141">Återupptas</span><span class="sxs-lookup"><span data-stu-id="13129-141">Resuming</span></span> 
- <span data-ttu-id="13129-142">Aktiv</span><span class="sxs-lookup"><span data-stu-id="13129-142">Running</span></span> 
- <span data-ttu-id="13129-143">Igång</span><span class="sxs-lookup"><span data-stu-id="13129-143">Stopped</span></span> 
- <span data-ttu-id="13129-144">Stänger</span><span class="sxs-lookup"><span data-stu-id="13129-144">Stopping</span></span> 
- <span data-ttu-id="13129-145">Hängande</span><span class="sxs-lookup"><span data-stu-id="13129-145">Suspended</span></span> 
- <span data-ttu-id="13129-146">Pausa</span><span class="sxs-lookup"><span data-stu-id="13129-146">Suspending</span></span> 
- <span data-ttu-id="13129-147">Aktivera</span><span class="sxs-lookup"><span data-stu-id="13129-147">Activating</span></span>
- <span data-ttu-id="13129-148">Nya</span><span class="sxs-lookup"><span data-stu-id="13129-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13129-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13129-149">CommonParameters</span></span>
<span data-ttu-id="13129-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13129-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13129-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13129-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13129-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13129-152">INPUTS</span></span>

### <span data-ttu-id="13129-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="13129-153">System.Guid</span></span>

### <span data-ttu-id="13129-154">System. String</span><span class="sxs-lookup"><span data-stu-id="13129-154">System.String</span></span>

## <span data-ttu-id="13129-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13129-155">OUTPUTS</span></span>

### <span data-ttu-id="13129-156">Microsoft. Azure. commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="13129-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="13129-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13129-157">NOTES</span></span>

## <span data-ttu-id="13129-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13129-158">RELATED LINKS</span></span>

[<span data-ttu-id="13129-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="13129-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="13129-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="13129-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

