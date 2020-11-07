---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: cc970a03e0af625237ef9b8c72f5afbe95578751
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927898"
---
# <span data-ttu-id="79c07-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="79c07-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="79c07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79c07-102">SYNOPSIS</span></span>
<span data-ttu-id="79c07-103">Hämtar data sektorer för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="79c07-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="79c07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79c07-104">SYNTAX</span></span>

### <span data-ttu-id="79c07-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="79c07-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79c07-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="79c07-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c07-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79c07-107">DESCRIPTION</span></span>
<span data-ttu-id="79c07-108">Cmdleten **Get-AzDataFactorySlice** hämtar data segment för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="79c07-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="79c07-109">Ange en start tid och en slut tid för att definiera ett data område som ska visas.</span><span class="sxs-lookup"><span data-stu-id="79c07-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="79c07-110">Statusen för en data sektor är något av följande värden:</span><span class="sxs-lookup"><span data-stu-id="79c07-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="79c07-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="79c07-111">PendingExecution.</span></span>
<span data-ttu-id="79c07-112">Data behandling har inte påbörjats.</span><span class="sxs-lookup"><span data-stu-id="79c07-112">Data processing has not started.</span></span> 
- <span data-ttu-id="79c07-113">Inaktive.</span><span class="sxs-lookup"><span data-stu-id="79c07-113">InProgress.</span></span>
<span data-ttu-id="79c07-114">Data bearbetning pågår.</span><span class="sxs-lookup"><span data-stu-id="79c07-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="79c07-115">Förbereder.</span><span class="sxs-lookup"><span data-stu-id="79c07-115">Ready.</span></span>
<span data-ttu-id="79c07-116">Data bearbetning är klar.</span><span class="sxs-lookup"><span data-stu-id="79c07-116">Data processing is completed.</span></span>
<span data-ttu-id="79c07-117">Data sektorn är redo för att du ska kunna använda det.</span><span class="sxs-lookup"><span data-stu-id="79c07-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="79c07-118">Startade.</span><span class="sxs-lookup"><span data-stu-id="79c07-118">Failed.</span></span>
<span data-ttu-id="79c07-119">Det gick inte att köra sektorn.</span><span class="sxs-lookup"><span data-stu-id="79c07-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="79c07-120">Vidare.</span><span class="sxs-lookup"><span data-stu-id="79c07-120">Skip.</span></span>
<span data-ttu-id="79c07-121">Data fabriken hoppar över bearbetning av sektorn.</span><span class="sxs-lookup"><span data-stu-id="79c07-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="79c07-122">Försök igen.</span><span class="sxs-lookup"><span data-stu-id="79c07-122">Retry.</span></span>
<span data-ttu-id="79c07-123">Data fabriken försöker igen med den körning som tillverkar segmentet.</span><span class="sxs-lookup"><span data-stu-id="79c07-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="79c07-124">Tids gränsen uppnåddes. Tids gränsen för data bearbetning har uppnåtts.</span><span class="sxs-lookup"><span data-stu-id="79c07-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="79c07-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="79c07-125">PendingValidation.</span></span>
<span data-ttu-id="79c07-126">Data sektorn väntar på verifiering innan den behandlas.</span><span class="sxs-lookup"><span data-stu-id="79c07-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="79c07-127">Gör om verifieringen.</span><span class="sxs-lookup"><span data-stu-id="79c07-127">Retry Validation.</span></span>
<span data-ttu-id="79c07-128">Data fabriken försöker att verifiera segmentet igen.</span><span class="sxs-lookup"><span data-stu-id="79c07-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="79c07-129">Valideringen misslyckades.</span><span class="sxs-lookup"><span data-stu-id="79c07-129">Failed Validation.</span></span>
<span data-ttu-id="79c07-130">Det gick inte att verifiera sektorn.</span><span class="sxs-lookup"><span data-stu-id="79c07-130">Validation of the slice failed.</span></span>
<span data-ttu-id="79c07-131">För var och en av sektorerna kan du Visa mer information om den körning som producerar segmentet med hjälp av Get-AzDataFactoryRun cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79c07-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="79c07-132">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79c07-132">EXAMPLES</span></span>

### <span data-ttu-id="79c07-133">Exempel 1: Hämta data sektorer för en data mängd</span><span class="sxs-lookup"><span data-stu-id="79c07-133">Example 1: Get data slices for a dataset</span></span>
```
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

<span data-ttu-id="79c07-134">Det här kommandot får alla data sektorer för den data uppsättning som heter WikiAggregatedData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="79c07-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="79c07-135">Kommandot får de sektorer som uppstår efter den tid som StartDateTime-parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="79c07-136">I följande exempel kod anges tillgänglighet för denna dataset varje timme i JSON-filen (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="79c07-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="79c07-137">tillgänglighet: {period: "timme", periodMultiplier: 1} vissa av resultaten är klara och andra är PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="79c07-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="79c07-138">Klara sektorer har redan körts.</span><span class="sxs-lookup"><span data-stu-id="79c07-138">Ready slices have already run.</span></span>
<span data-ttu-id="79c07-139">De väntande sektorerna väntar på att de ska köras vid slutet av varje timme i det intervall som Set-AzDataFactoryPipelineActivePeriod-cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="79c07-140">I det här exemplet har både start-och slut perioderna för pipeline och segmentet ett värde om 1 dag (24 timmar).</span><span class="sxs-lookup"><span data-stu-id="79c07-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="79c07-141">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79c07-141">PARAMETERS</span></span>

### <span data-ttu-id="79c07-142">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="79c07-142">-DataFactory</span></span>
<span data-ttu-id="79c07-143">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79c07-143">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="79c07-144">Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-144">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79c07-145">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="79c07-145">-DataFactoryName</span></span>
<span data-ttu-id="79c07-146">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="79c07-146">Specifies the name of a data factory.</span></span>
<span data-ttu-id="79c07-147">Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79c07-148">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="79c07-148">-DatasetName</span></span>
<span data-ttu-id="79c07-149">Anger namnet på den dataset för vilken denna cmdlet hämtar sektorer.</span><span class="sxs-lookup"><span data-stu-id="79c07-149">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="79c07-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c07-150">-DefaultProfile</span></span>
<span data-ttu-id="79c07-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="79c07-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79c07-152">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="79c07-152">-EndDateTime</span></span>
<span data-ttu-id="79c07-153">Anger slutet på en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79c07-153">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="79c07-154">Denna cmdlet tar fram sektorer som produceras före den tid som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-154">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="79c07-155">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="79c07-155">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="79c07-156">*EndDateTime* måste anges i formatet iso8601 som i följande exempel: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time).</span><span class="sxs-lookup"><span data-stu-id="79c07-156">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="79c07-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c07-157">-ResourceGroupName</span></span>
<span data-ttu-id="79c07-158">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="79c07-158">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="79c07-159">Denna cmdlet hämtar sektorer som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-159">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="79c07-160">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="79c07-160">-StartDateTime</span></span>
<span data-ttu-id="79c07-161">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="79c07-161">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="79c07-162">Denna cmdlet tar emot sektorer efter den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="79c07-162">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="79c07-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c07-163">CommonParameters</span></span>
<span data-ttu-id="79c07-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c07-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c07-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c07-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c07-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79c07-166">INPUTS</span></span>

### <span data-ttu-id="79c07-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="79c07-167">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="79c07-168">System. String</span><span class="sxs-lookup"><span data-stu-id="79c07-168">System.String</span></span>

## <span data-ttu-id="79c07-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79c07-169">OUTPUTS</span></span>

### <span data-ttu-id="79c07-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="79c07-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="79c07-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79c07-171">NOTES</span></span>
* <span data-ttu-id="79c07-172">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="79c07-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="79c07-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79c07-173">RELATED LINKS</span></span>

[<span data-ttu-id="79c07-174">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="79c07-174">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="79c07-175">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="79c07-175">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="79c07-176">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="79c07-176">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


