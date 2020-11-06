---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581536"
---
# <span data-ttu-id="9ed32-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9ed32-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="9ed32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ed32-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed32-103">Hämtar DSC-kompilator jobb i Automation.</span><span class="sxs-lookup"><span data-stu-id="9ed32-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ed32-104">SYNTAX</span></span>

### <span data-ttu-id="9ed32-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="9ed32-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed32-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="9ed32-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed32-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9ed32-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed32-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ed32-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed32-109">Cmdleten **Get-AzureRmAutomationDscCompilationJob** får AP-kompilatorn (Desired State Configuration) i APS för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9ed32-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="9ed32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ed32-110">EXAMPLES</span></span>

### <span data-ttu-id="9ed32-111">Exempel 1: Hämta alla DSC Compilation-jobb</span><span class="sxs-lookup"><span data-stu-id="9ed32-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9ed32-112">Det här kommandot får alla kompilator jobb i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ed32-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9ed32-113">Exempel 2: Hämta DSC-kompilator jobb för en konfiguration</span><span class="sxs-lookup"><span data-stu-id="9ed32-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="9ed32-114">Det här kommandot får alla kompilator jobb för DSC-konfigurationen som heter ContosoConfiguration i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ed32-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9ed32-115">Exempel 3: Hämta ett specifikt DSC-kompilator jobb</span><span class="sxs-lookup"><span data-stu-id="9ed32-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="9ed32-116">Det här kommandot får Compilation Job med angivet ID i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ed32-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9ed32-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ed32-117">PARAMETERS</span></span>

### <span data-ttu-id="9ed32-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ed32-118">-AutomationAccountName</span></span>
<span data-ttu-id="9ed32-119">Anger namnet på det Automation-konto som innehåller de DSC Compilation-jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="9ed32-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ed32-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9ed32-120">-ConfigurationName</span></span>
<span data-ttu-id="9ed32-121">Anger namnet på den DSC-konfiguration för vilken denna cmdlet ska kompilera jobb.</span><span class="sxs-lookup"><span data-stu-id="9ed32-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="9ed32-122">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="9ed32-122">-EndTime</span></span>
<span data-ttu-id="9ed32-123">Anger en slut tid.</span><span class="sxs-lookup"><span data-stu-id="9ed32-123">Specifies an end time.</span></span>
<span data-ttu-id="9ed32-124">Denna cmdlet används för att kompilera jobb som startats till den tidpunkt då den här parametern anges.</span><span class="sxs-lookup"><span data-stu-id="9ed32-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ed32-125">-ID</span><span class="sxs-lookup"><span data-stu-id="9ed32-125">-Id</span></span>
<span data-ttu-id="9ed32-126">Anger det unika ID: t för det DSC Compilation-jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="9ed32-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ed32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed32-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ed32-128">Anger namnet på en resurs grupp där denna cmdlet får DSC Compilation-jobb.</span><span class="sxs-lookup"><span data-stu-id="9ed32-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="9ed32-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9ed32-129">-StartTime</span></span>
<span data-ttu-id="9ed32-130">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="9ed32-130">Specifies a start time.</span></span>
<span data-ttu-id="9ed32-131">Denna cmdlet hämtar jobb som startar vid eller efter den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9ed32-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="9ed32-132">-Status</span><span class="sxs-lookup"><span data-stu-id="9ed32-132">-Status</span></span>
<span data-ttu-id="9ed32-133">Anger statusen för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="9ed32-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9ed32-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="9ed32-134">Valid values are:</span></span> 

- <span data-ttu-id="9ed32-135">Rätta</span><span class="sxs-lookup"><span data-stu-id="9ed32-135">Completed</span></span> 
- <span data-ttu-id="9ed32-136">Startade</span><span class="sxs-lookup"><span data-stu-id="9ed32-136">Failed</span></span> 
- <span data-ttu-id="9ed32-137">I kö</span><span class="sxs-lookup"><span data-stu-id="9ed32-137">Queued</span></span> 
- <span data-ttu-id="9ed32-138">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="9ed32-138">Starting</span></span> 
- <span data-ttu-id="9ed32-139">Återupptas</span><span class="sxs-lookup"><span data-stu-id="9ed32-139">Resuming</span></span> 
- <span data-ttu-id="9ed32-140">Aktiv</span><span class="sxs-lookup"><span data-stu-id="9ed32-140">Running</span></span> 
- <span data-ttu-id="9ed32-141">Igång</span><span class="sxs-lookup"><span data-stu-id="9ed32-141">Stopped</span></span> 
- <span data-ttu-id="9ed32-142">Stänger</span><span class="sxs-lookup"><span data-stu-id="9ed32-142">Stopping</span></span> 
- <span data-ttu-id="9ed32-143">Hängande</span><span class="sxs-lookup"><span data-stu-id="9ed32-143">Suspended</span></span> 
- <span data-ttu-id="9ed32-144">Pausa</span><span class="sxs-lookup"><span data-stu-id="9ed32-144">Suspending</span></span> 
- <span data-ttu-id="9ed32-145">Aktivera</span><span class="sxs-lookup"><span data-stu-id="9ed32-145">Activating</span></span>
- <span data-ttu-id="9ed32-146">Nya</span><span class="sxs-lookup"><span data-stu-id="9ed32-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed32-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed32-147">-DefaultProfile</span></span>
<span data-ttu-id="9ed32-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed32-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed32-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed32-149">CommonParameters</span></span>
<span data-ttu-id="9ed32-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed32-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed32-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed32-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed32-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ed32-152">INPUTS</span></span>

## <span data-ttu-id="9ed32-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ed32-153">OUTPUTS</span></span>

### <span data-ttu-id="9ed32-154">Microsoft. Azure. commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="9ed32-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="9ed32-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ed32-155">NOTES</span></span>

## <span data-ttu-id="9ed32-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ed32-156">RELATED LINKS</span></span>

[<span data-ttu-id="9ed32-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="9ed32-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="9ed32-158">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9ed32-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


