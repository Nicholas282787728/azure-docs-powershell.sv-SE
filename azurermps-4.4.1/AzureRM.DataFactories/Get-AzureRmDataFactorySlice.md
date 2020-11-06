---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 038f611edbbec0f5f6bb1be433a1c1cee8fa2990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574723"
---
# <span data-ttu-id="9120a-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="9120a-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="9120a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9120a-102">SYNOPSIS</span></span>
<span data-ttu-id="9120a-103">Hämtar data sektorer för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9120a-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9120a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9120a-104">SYNTAX</span></span>

### <span data-ttu-id="9120a-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9120a-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9120a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9120a-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9120a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9120a-107">DESCRIPTION</span></span>
<span data-ttu-id="9120a-108">Cmdleten **Get-AzureRmDataFactorySlice** hämtar data segment för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9120a-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="9120a-109">Ange en start tid och en slut tid för att definiera ett data område som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9120a-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="9120a-110">Statusen för en data sektor är något av följande värden:</span><span class="sxs-lookup"><span data-stu-id="9120a-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="9120a-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="9120a-111">PendingExecution.</span></span>
<span data-ttu-id="9120a-112">Data behandling har inte påbörjats.</span><span class="sxs-lookup"><span data-stu-id="9120a-112">Data processing has not started.</span></span> 
- <span data-ttu-id="9120a-113">Inaktive.</span><span class="sxs-lookup"><span data-stu-id="9120a-113">InProgress.</span></span>
<span data-ttu-id="9120a-114">Data bearbetning pågår.</span><span class="sxs-lookup"><span data-stu-id="9120a-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="9120a-115">Förbereder.</span><span class="sxs-lookup"><span data-stu-id="9120a-115">Ready.</span></span>
<span data-ttu-id="9120a-116">Data bearbetning är klar.</span><span class="sxs-lookup"><span data-stu-id="9120a-116">Data processing is completed.</span></span>
<span data-ttu-id="9120a-117">Data sektorn är redo för att du ska kunna använda det.</span><span class="sxs-lookup"><span data-stu-id="9120a-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="9120a-118">Startade.</span><span class="sxs-lookup"><span data-stu-id="9120a-118">Failed.</span></span>
<span data-ttu-id="9120a-119">Det gick inte att köra sektorn.</span><span class="sxs-lookup"><span data-stu-id="9120a-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="9120a-120">Vidare.</span><span class="sxs-lookup"><span data-stu-id="9120a-120">Skip.</span></span>
<span data-ttu-id="9120a-121">Data fabriken hoppar över bearbetning av sektorn.</span><span class="sxs-lookup"><span data-stu-id="9120a-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="9120a-122">Försök igen.</span><span class="sxs-lookup"><span data-stu-id="9120a-122">Retry.</span></span>
<span data-ttu-id="9120a-123">Data fabriken försöker igen med den körning som tillverkar segmentet.</span><span class="sxs-lookup"><span data-stu-id="9120a-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="9120a-124">Tids gränsen uppnåddes. Tids gränsen för data bearbetning har uppnåtts.</span><span class="sxs-lookup"><span data-stu-id="9120a-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="9120a-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="9120a-125">PendingValidation.</span></span>
<span data-ttu-id="9120a-126">Data sektorn väntar på verifiering innan den behandlas.</span><span class="sxs-lookup"><span data-stu-id="9120a-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="9120a-127">Gör om verifieringen.</span><span class="sxs-lookup"><span data-stu-id="9120a-127">Retry Validation.</span></span>
<span data-ttu-id="9120a-128">Data fabriken försöker att verifiera segmentet igen.</span><span class="sxs-lookup"><span data-stu-id="9120a-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="9120a-129">Valideringen misslyckades.</span><span class="sxs-lookup"><span data-stu-id="9120a-129">Failed Validation.</span></span>
<span data-ttu-id="9120a-130">Det gick inte att verifiera sektorn.</span><span class="sxs-lookup"><span data-stu-id="9120a-130">Validation of the slice failed.</span></span>

<span data-ttu-id="9120a-131">För var och en av sektorerna kan du Visa mer information om den körning som producerar segmentet med hjälp av Get-AzureRmDataFactoryRun cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9120a-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="9120a-132">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9120a-132">EXAMPLES</span></span>

### <span data-ttu-id="9120a-133">Exempel 1: Hämta data sektorer för en data mängd</span><span class="sxs-lookup"><span data-stu-id="9120a-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="9120a-134">Det här kommandot får alla data sektorer för den data uppsättning som heter WikiAggregatedData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9120a-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="9120a-135">Kommandot får de sektorer som uppstår efter den tid som StartDateTime-parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="9120a-136">I följande exempel kod anges tillgänglighet för denna dataset varje timme i JSON-filen (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="9120a-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="9120a-137">Klara sektorer har redan körts.</span><span class="sxs-lookup"><span data-stu-id="9120a-137">Ready slices have already run.</span></span>
<span data-ttu-id="9120a-138">De väntande sektorerna väntar på att de ska köras vid slutet av varje timme i det intervall som Set-AzureRmDataFactoryPipelineActivePeriod-cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="9120a-139">I det här exemplet har både start-och slut perioderna för pipeline och segmentet ett värde om 1 dag (24 timmar).</span><span class="sxs-lookup"><span data-stu-id="9120a-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="9120a-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9120a-140">PARAMETERS</span></span>

### <span data-ttu-id="9120a-141">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9120a-141">-DataFactory</span></span>
<span data-ttu-id="9120a-142">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9120a-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9120a-143">Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9120a-144">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9120a-144">-DataFactoryName</span></span>
<span data-ttu-id="9120a-145">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9120a-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9120a-146">Denna cmdlet hämtar sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9120a-147">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="9120a-147">-DatasetName</span></span>
<span data-ttu-id="9120a-148">Anger namnet på den dataset för vilken denna cmdlet hämtar sektorer.</span><span class="sxs-lookup"><span data-stu-id="9120a-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="9120a-149">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="9120a-149">-EndDateTime</span></span>
<span data-ttu-id="9120a-150">Anger slutet på en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9120a-150">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9120a-151">Denna cmdlet tar fram sektorer som produceras före den tid som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-151">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="9120a-152">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9120a-152">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="9120a-153">*EndDateTime* måste anges i iso8601 format enligt följande exempel:</span><span class="sxs-lookup"><span data-stu-id="9120a-153">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="9120a-154">2015 – 01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific, normal tid)</span><span class="sxs-lookup"><span data-stu-id="9120a-154">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="9120a-155">Standard tids zonen är UTC.</span><span class="sxs-lookup"><span data-stu-id="9120a-155">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="9120a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9120a-156">-ResourceGroupName</span></span>
<span data-ttu-id="9120a-157">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="9120a-157">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9120a-158">Denna cmdlet hämtar sektorer som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-158">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9120a-159">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="9120a-159">-StartDateTime</span></span>
<span data-ttu-id="9120a-160">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9120a-160">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9120a-161">Denna cmdlet tar emot sektorer efter den tid som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9120a-161">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="9120a-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9120a-162">-DefaultProfile</span></span>
<span data-ttu-id="9120a-163">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9120a-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9120a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9120a-164">CommonParameters</span></span>
<span data-ttu-id="9120a-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9120a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9120a-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9120a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9120a-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9120a-167">INPUTS</span></span>

## <span data-ttu-id="9120a-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9120a-168">OUTPUTS</span></span>

### <span data-ttu-id="9120a-169">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. WindowsAzure. commands. Utilities, version = 0.8.2.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9120a-169">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="9120a-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9120a-170">NOTES</span></span>
* <span data-ttu-id="9120a-171">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="9120a-171">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9120a-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9120a-172">RELATED LINKS</span></span>

[<span data-ttu-id="9120a-173">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="9120a-173">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="9120a-174">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="9120a-174">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="9120a-175">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="9120a-175">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


