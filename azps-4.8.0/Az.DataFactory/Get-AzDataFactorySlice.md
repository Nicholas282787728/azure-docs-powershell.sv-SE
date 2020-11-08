---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260060"
---
# <span data-ttu-id="67f73-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="67f73-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="67f73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67f73-102">SYNOPSIS</span></span>
<span data-ttu-id="67f73-103">Hämtar data sektorer för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67f73-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="67f73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67f73-104">SYNTAX</span></span>

### <span data-ttu-id="67f73-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="67f73-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67f73-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="67f73-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67f73-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67f73-107">DESCRIPTION</span></span>
<span data-ttu-id="67f73-108">Cmdleten **Get-AzDataFactorySlice** hämtar data segment för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67f73-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="67f73-109">Ange en start tid och en slut tid för att definiera ett data område som ska visas.</span><span class="sxs-lookup"><span data-stu-id="67f73-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="67f73-110">Statusen för en data sektor är något av följande värden:</span><span class="sxs-lookup"><span data-stu-id="67f73-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="67f73-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="67f73-111">PendingExecution.</span></span>
<span data-ttu-id="67f73-112">Data behandling har inte påbörjats.</span><span class="sxs-lookup"><span data-stu-id="67f73-112">Data processing has not started.</span></span> 
- <span data-ttu-id="67f73-113">Inaktive.</span><span class="sxs-lookup"><span data-stu-id="67f73-113">InProgress.</span></span>
<span data-ttu-id="67f73-114">Data bearbetning pågår.</span><span class="sxs-lookup"><span data-stu-id="67f73-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="67f73-115">Förbereder.</span><span class="sxs-lookup"><span data-stu-id="67f73-115">Ready.</span></span>
<span data-ttu-id="67f73-116">Data bearbetning är klar.</span><span class="sxs-lookup"><span data-stu-id="67f73-116">Data processing is completed.</span></span>
<span data-ttu-id="67f73-117">Data sektorn är redo för att du ska kunna använda det.</span><span class="sxs-lookup"><span data-stu-id="67f73-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="67f73-118">Startade.</span><span class="sxs-lookup"><span data-stu-id="67f73-118">Failed.</span></span>
<span data-ttu-id="67f73-119">Det gick inte att köra sektorn.</span><span class="sxs-lookup"><span data-stu-id="67f73-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="67f73-120">Vidare.</span><span class="sxs-lookup"><span data-stu-id="67f73-120">Skip.</span></span>
<span data-ttu-id="67f73-121">Data fabriken hoppar över bearbetning av sektorn.</span><span class="sxs-lookup"><span data-stu-id="67f73-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="67f73-122">Försök igen.</span><span class="sxs-lookup"><span data-stu-id="67f73-122">Retry.</span></span>
<span data-ttu-id="67f73-123">Data fabriken försöker igen med den körning som tillverkar segmentet.</span><span class="sxs-lookup"><span data-stu-id="67f73-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="67f73-124">Tids gränsen uppnåddes. Tids gränsen för data bearbetning har uppnåtts.</span><span class="sxs-lookup"><span data-stu-id="67f73-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="67f73-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="67f73-125">PendingValidation.</span></span>
<span data-ttu-id="67f73-126">Data sektorn väntar på verifiering innan den behandlas.</span><span class="sxs-lookup"><span data-stu-id="67f73-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="67f73-127">Gör om verifieringen.</span><span class="sxs-lookup"><span data-stu-id="67f73-127">Retry Validation.</span></span>
<span data-ttu-id="67f73-128">Data fabriken försöker att verifiera segmentet igen.</span><span class="sxs-lookup"><span data-stu-id="67f73-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="67f73-129">Valideringen misslyckades.</span><span class="sxs-lookup"><span data-stu-id="67f73-129">Failed Validation.</span></span>
<span data-ttu-id="67f73-130">Det gick inte att verifiera sektorn.</span><span class="sxs-lookup"><span data-stu-id="67f73-130">Validation of the slice failed.</span></span>
<span data-ttu-id="67f73-131">För var och en av sektorerna kan du Visa mer information om den körning som producerar segmentet med hjälp av Get-AzDataFactoryRun cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67f73-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="67f73-132">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67f73-132">EXAMPLES</span></span>

### <span data-ttu-id="67f73-133">Exempel 1: Hämta data sektorer för en data mängd</span><span class="sxs-lookup"><span data-stu-id="67f73-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="67f73-134">Det här kommandot får alla data sektorer för den data uppsättning som heter WikiAggregatedData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="67f73-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="67f73-135">Kommandot får de sektorer som uppstår efter den tid som StartDateTime-parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="67f73-136">I följande exempel kod anges tillgänglighet för denna dataset varje timme i JSON-filen (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="67f73-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="67f73-137">tillgänglighet: {period: "timme", periodMultiplier: 1} vissa av resultaten är klara och andra är PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="67f73-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="67f73-138">Klara sektorer har redan körts.</span><span class="sxs-lookup"><span data-stu-id="67f73-138">Ready slices have already run.</span></span>
<span data-ttu-id="67f73-139">De väntande sektorerna väntar på att de ska köras vid slutet av varje timme i det intervall som Set-AzDataFactoryPipelineActivePeriod-cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="67f73-140">I det här exemplet har både start-och slut perioderna för pipeline och segmentet ett värde om 1 dag (24 timmar).</span><span class="sxs-lookup"><span data-stu-id="67f73-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="67f73-141">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="67f73-141">Example 2</span></span>

<span data-ttu-id="67f73-142">Hämtar data sektorer för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67f73-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="67f73-143">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="67f73-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="67f73-144">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67f73-144">PARAMETERS</span></span>

### <span data-ttu-id="67f73-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="67f73-145">-DataFactory</span></span>
<span data-ttu-id="67f73-146">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="67f73-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="67f73-147">Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f73-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="67f73-148">-DataFactoryName</span></span>
<span data-ttu-id="67f73-149">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="67f73-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="67f73-150">Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f73-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="67f73-151">-DatasetName</span></span>
<span data-ttu-id="67f73-152">Anger namnet på den dataset för vilken denna cmdlet hämtar sektorer.</span><span class="sxs-lookup"><span data-stu-id="67f73-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="67f73-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f73-153">-DefaultProfile</span></span>
<span data-ttu-id="67f73-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="67f73-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f73-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="67f73-155">-EndDateTime</span></span>
<span data-ttu-id="67f73-156">Anger slutet på en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="67f73-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="67f73-157">Denna cmdlet tar fram sektorer som produceras före den tid som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="67f73-158">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="67f73-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="67f73-159">*EndDateTime* måste anges i formatet iso8601 som i följande exempel: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time).</span><span class="sxs-lookup"><span data-stu-id="67f73-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f73-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f73-160">-ResourceGroupName</span></span>
<span data-ttu-id="67f73-161">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="67f73-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="67f73-162">Denna cmdlet hämtar sektorer som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f73-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="67f73-163">-StartDateTime</span></span>
<span data-ttu-id="67f73-164">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="67f73-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="67f73-165">Denna cmdlet tar emot sektorer efter den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="67f73-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f73-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f73-166">CommonParameters</span></span>
<span data-ttu-id="67f73-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f73-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f73-168">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f73-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f73-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67f73-169">INPUTS</span></span>

### <span data-ttu-id="67f73-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="67f73-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="67f73-171">System. String</span><span class="sxs-lookup"><span data-stu-id="67f73-171">System.String</span></span>

## <span data-ttu-id="67f73-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67f73-172">OUTPUTS</span></span>

### <span data-ttu-id="67f73-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="67f73-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="67f73-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67f73-174">NOTES</span></span>
* <span data-ttu-id="67f73-175">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="67f73-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="67f73-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67f73-176">RELATED LINKS</span></span>

[<span data-ttu-id="67f73-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="67f73-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="67f73-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="67f73-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="67f73-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="67f73-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


