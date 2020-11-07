---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 253a17f16033836622ceb83bdac8532aa808a20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756724"
---
# <span data-ttu-id="6525e-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6525e-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="6525e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6525e-102">SYNOPSIS</span></span>
<span data-ttu-id="6525e-103">Hämtar DSC-kompilator jobb i Automation.</span><span class="sxs-lookup"><span data-stu-id="6525e-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6525e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6525e-104">SYNTAX</span></span>

### <span data-ttu-id="6525e-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="6525e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6525e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="6525e-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6525e-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6525e-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6525e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6525e-108">DESCRIPTION</span></span>
<span data-ttu-id="6525e-109">Cmdleten **Get-AzureRmAutomationDscCompilationJob** får AP-kompilatorn (Desired State Configuration) i APS för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6525e-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="6525e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6525e-110">EXAMPLES</span></span>

### <span data-ttu-id="6525e-111">Exempel 1: Hämta alla DSC Compilation-jobb</span><span class="sxs-lookup"><span data-stu-id="6525e-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6525e-112">Det här kommandot får alla kompilator jobb i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6525e-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6525e-113">Exempel 2: Hämta DSC-kompilator jobb för en konfiguration</span><span class="sxs-lookup"><span data-stu-id="6525e-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="6525e-114">Det här kommandot får alla kompilator jobb för DSC-konfigurationen som heter ContosoConfiguration i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6525e-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6525e-115">Exempel 3: Hämta ett specifikt DSC-kompilator jobb</span><span class="sxs-lookup"><span data-stu-id="6525e-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="6525e-116">Det här kommandot får Compilation Job med angivet ID i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6525e-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6525e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6525e-117">PARAMETERS</span></span>

### <span data-ttu-id="6525e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6525e-118">-AutomationAccountName</span></span>
<span data-ttu-id="6525e-119">Anger namnet på det Automation-konto som innehåller de DSC Compilation-jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6525e-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6525e-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6525e-120">-ConfigurationName</span></span>
<span data-ttu-id="6525e-121">Anger namnet på den DSC-konfiguration för vilken denna cmdlet ska kompilera jobb.</span><span class="sxs-lookup"><span data-stu-id="6525e-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="6525e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6525e-122">-DefaultProfile</span></span>
<span data-ttu-id="6525e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6525e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6525e-124">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="6525e-124">-EndTime</span></span>
<span data-ttu-id="6525e-125">Anger en slut tid.</span><span class="sxs-lookup"><span data-stu-id="6525e-125">Specifies an end time.</span></span>
<span data-ttu-id="6525e-126">Denna cmdlet används för att kompilera jobb som startats till den tidpunkt då den här parametern anges.</span><span class="sxs-lookup"><span data-stu-id="6525e-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="6525e-127">-ID</span><span class="sxs-lookup"><span data-stu-id="6525e-127">-Id</span></span>
<span data-ttu-id="6525e-128">Anger det unika ID: t för det DSC Compilation-jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6525e-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6525e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6525e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6525e-130">Anger namnet på en resurs grupp där denna cmdlet får DSC Compilation-jobb.</span><span class="sxs-lookup"><span data-stu-id="6525e-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="6525e-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6525e-131">-StartTime</span></span>
<span data-ttu-id="6525e-132">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="6525e-132">Specifies a start time.</span></span>
<span data-ttu-id="6525e-133">Denna cmdlet hämtar jobb som startar vid eller efter den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6525e-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="6525e-134">-Status</span><span class="sxs-lookup"><span data-stu-id="6525e-134">-Status</span></span>
<span data-ttu-id="6525e-135">Anger statusen för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6525e-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6525e-136">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="6525e-136">Valid values are:</span></span> 
- <span data-ttu-id="6525e-137">Rätta</span><span class="sxs-lookup"><span data-stu-id="6525e-137">Completed</span></span> 
- <span data-ttu-id="6525e-138">Startade</span><span class="sxs-lookup"><span data-stu-id="6525e-138">Failed</span></span> 
- <span data-ttu-id="6525e-139">I kö</span><span class="sxs-lookup"><span data-stu-id="6525e-139">Queued</span></span> 
- <span data-ttu-id="6525e-140">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="6525e-140">Starting</span></span> 
- <span data-ttu-id="6525e-141">Återupptas</span><span class="sxs-lookup"><span data-stu-id="6525e-141">Resuming</span></span> 
- <span data-ttu-id="6525e-142">Aktiv</span><span class="sxs-lookup"><span data-stu-id="6525e-142">Running</span></span> 
- <span data-ttu-id="6525e-143">Igång</span><span class="sxs-lookup"><span data-stu-id="6525e-143">Stopped</span></span> 
- <span data-ttu-id="6525e-144">Stänger</span><span class="sxs-lookup"><span data-stu-id="6525e-144">Stopping</span></span> 
- <span data-ttu-id="6525e-145">Hängande</span><span class="sxs-lookup"><span data-stu-id="6525e-145">Suspended</span></span> 
- <span data-ttu-id="6525e-146">Pausa</span><span class="sxs-lookup"><span data-stu-id="6525e-146">Suspending</span></span> 
- <span data-ttu-id="6525e-147">Aktivera</span><span class="sxs-lookup"><span data-stu-id="6525e-147">Activating</span></span>
- <span data-ttu-id="6525e-148">Nya</span><span class="sxs-lookup"><span data-stu-id="6525e-148">New</span></span>

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

### <span data-ttu-id="6525e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6525e-149">CommonParameters</span></span>
<span data-ttu-id="6525e-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6525e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6525e-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6525e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6525e-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6525e-152">INPUTS</span></span>

### <span data-ttu-id="6525e-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6525e-153">System.Guid</span></span>

### <span data-ttu-id="6525e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="6525e-154">System.String</span></span>

## <span data-ttu-id="6525e-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6525e-155">OUTPUTS</span></span>

### <span data-ttu-id="6525e-156">Microsoft. Azure. commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="6525e-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="6525e-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6525e-157">NOTES</span></span>

## <span data-ttu-id="6525e-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6525e-158">RELATED LINKS</span></span>

[<span data-ttu-id="6525e-159">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="6525e-159">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="6525e-160">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6525e-160">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


