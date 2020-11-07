---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: b3524f0886c5c433c6ec36d907126e6ca04828de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917121"
---
# <span data-ttu-id="09669-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="09669-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="09669-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09669-102">SYNOPSIS</span></span>
<span data-ttu-id="09669-103">Kör för en data sektor i en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="09669-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="09669-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09669-104">SYNTAX</span></span>

### <span data-ttu-id="09669-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="09669-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09669-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="09669-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09669-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09669-107">DESCRIPTION</span></span>
<span data-ttu-id="09669-108">Cmdleten **Get-AzDataFactoryRun** hämtar körningarna för en data sektor för en dataset i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="09669-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="09669-109">En data mängd i en data fabrik består av sektorer över tids axeln.</span><span class="sxs-lookup"><span data-stu-id="09669-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="09669-110">Bredden på en sektor bestäms av schemat, antingen per timme eller per dag.</span><span class="sxs-lookup"><span data-stu-id="09669-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="09669-111">En körning är en bearbetnings enhet för en sektor.</span><span class="sxs-lookup"><span data-stu-id="09669-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="09669-112">Det kan finnas en eller flera körningar för en sektor om ett försök görs eller om du kör om din organisation på grund av ett fel.</span><span class="sxs-lookup"><span data-stu-id="09669-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="09669-113">Ett segment identifieras av start tiden.</span><span class="sxs-lookup"><span data-stu-id="09669-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="09669-114">Använd Get-AzDataFactorySlice cmdlet för att få start tiden för en sektor.</span><span class="sxs-lookup"><span data-stu-id="09669-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="09669-115">Om du till exempel vill använda Start tiden 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="09669-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="09669-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset start: 5/2/2014 8:00:00 PM: 5/3/2014 8:00:00 PM RetryCount: 0 status: klar LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="09669-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="09669-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09669-117">EXAMPLES</span></span>

### <span data-ttu-id="09669-118">Exempel 1: skaffa en data mängd</span><span class="sxs-lookup"><span data-stu-id="09669-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="09669-119">Det här kommandot får alla körningar för sektorer i den dataset som heter DAWikiAggregatedData i data fabriken med namnet WikiADF som börjar från 4 EM GMT på 05/21/2014.</span><span class="sxs-lookup"><span data-stu-id="09669-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="09669-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09669-120">PARAMETERS</span></span>

### <span data-ttu-id="09669-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="09669-121">-DataFactory</span></span>
<span data-ttu-id="09669-122">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="09669-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="09669-123">Denna cmdlet körs för sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="09669-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="09669-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="09669-124">-DataFactoryName</span></span>
<span data-ttu-id="09669-125">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="09669-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="09669-126">Denna cmdlet körs för sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="09669-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="09669-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="09669-127">-DatasetName</span></span>
<span data-ttu-id="09669-128">Anger namnet på data mängden.</span><span class="sxs-lookup"><span data-stu-id="09669-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="09669-129">Denna cmdlet körs för sektorer som tillhör den dataset som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="09669-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="09669-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09669-130">-DefaultProfile</span></span>
<span data-ttu-id="09669-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="09669-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09669-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09669-132">-ResourceGroupName</span></span>
<span data-ttu-id="09669-133">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="09669-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="09669-134">Denna cmdlet blir fabriksinstallerad för sektorer som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="09669-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="09669-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="09669-135">-StartDateTime</span></span>
<span data-ttu-id="09669-136">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="09669-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="09669-137">Denna cmdlet körs för de data sektorer som matchar den här tids perioden.</span><span class="sxs-lookup"><span data-stu-id="09669-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="09669-138">*StartDateTime* måste anges i iso8601 format, som i följande exempel: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) standard tids zonen är UTC.</span><span class="sxs-lookup"><span data-stu-id="09669-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="09669-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09669-139">CommonParameters</span></span>
<span data-ttu-id="09669-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09669-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09669-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09669-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09669-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09669-142">INPUTS</span></span>

### <span data-ttu-id="09669-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="09669-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="09669-144">System. String</span><span class="sxs-lookup"><span data-stu-id="09669-144">System.String</span></span>

## <span data-ttu-id="09669-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09669-145">OUTPUTS</span></span>

### <span data-ttu-id="09669-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="09669-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="09669-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09669-147">NOTES</span></span>
* <span data-ttu-id="09669-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="09669-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="09669-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09669-149">RELATED LINKS</span></span>

[<span data-ttu-id="09669-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="09669-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


