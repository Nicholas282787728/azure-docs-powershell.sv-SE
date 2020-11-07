---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574313"
---
# <span data-ttu-id="c9058-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="c9058-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="c9058-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9058-102">SYNOPSIS</span></span>
<span data-ttu-id="c9058-103">Anger statusen för sektorer för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c9058-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9058-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9058-104">SYNTAX</span></span>

### <span data-ttu-id="c9058-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="c9058-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9058-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c9058-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9058-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9058-107">DESCRIPTION</span></span>
<span data-ttu-id="c9058-108">Cmdleten **set-AzureRmDataFactorySliceStatus** anger statusen för sektorer för en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c9058-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="c9058-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9058-109">EXAMPLES</span></span>

### <span data-ttu-id="c9058-110">Exempel 1: Ange status för alla sektorer</span><span class="sxs-lookup"><span data-stu-id="c9058-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="c9058-111">Det här kommandot anger statusen för alla sektorer för den dataset som heter DAWikiAggregatedData för att vänta på data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c9058-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="c9058-112">Parametern *UpdateType* har värdet UpstreamInPipeline, så kommandot anger statusen för varje sektor för dataset och alla beroende data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="c9058-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="c9058-113">Underordnade data mängder används som indata-dataset för aktiviteter i pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9058-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="c9058-114">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="c9058-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="c9058-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9058-115">PARAMETERS</span></span>

### <span data-ttu-id="c9058-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c9058-116">-DataFactory</span></span>
<span data-ttu-id="c9058-117">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c9058-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c9058-118">Denna cmdlet ändrar statusen för de sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c9058-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c9058-119">-DataFactoryName</span></span>
<span data-ttu-id="c9058-120">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="c9058-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c9058-121">Denna cmdlet ändrar statusen för de sektorer som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c9058-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="c9058-122">-DatasetName</span></span>
<span data-ttu-id="c9058-123">Anger namnet på den dataset som denna cmdlet ändrar sektorer för.</span><span class="sxs-lookup"><span data-stu-id="c9058-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9058-124">-DefaultProfile</span></span>
<span data-ttu-id="c9058-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9058-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9058-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="c9058-126">-EndDateTime</span></span>
<span data-ttu-id="c9058-127">Anger slutet på en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c9058-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="c9058-128">Den här tiden är slutet av data sektorn.</span><span class="sxs-lookup"><span data-stu-id="c9058-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="c9058-129">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c9058-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="c9058-130">*EndDateTime* måste anges i iso8601 format enligt följande exempel:</span><span class="sxs-lookup"><span data-stu-id="c9058-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="c9058-131">2015 – 01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific, normal tid)</span><span class="sxs-lookup"><span data-stu-id="c9058-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="c9058-132">Standard tids zonen är UTC.</span><span class="sxs-lookup"><span data-stu-id="c9058-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9058-133">-ResourceGroupName</span></span>
<span data-ttu-id="c9058-134">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="c9058-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c9058-135">Denna cmdlet ändrar statusen för de sektorer som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c9058-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="c9058-136">-StartDateTime</span></span>
<span data-ttu-id="c9058-137">Anger början av en tids period som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c9058-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="c9058-138">Den här gången är början på data sektorn.</span><span class="sxs-lookup"><span data-stu-id="c9058-138">This time is the beginning of a data slice.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-139">-Status</span><span class="sxs-lookup"><span data-stu-id="c9058-139">-Status</span></span>
<span data-ttu-id="c9058-140">Anger en status som ska kopplas till data sektorn.</span><span class="sxs-lookup"><span data-stu-id="c9058-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="c9058-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c9058-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9058-142">Godkänna.</span><span class="sxs-lookup"><span data-stu-id="c9058-142">Waiting.</span></span>
<span data-ttu-id="c9058-143">Data sektorn väntar på validering mot verifierings principer innan den behandlas.</span><span class="sxs-lookup"><span data-stu-id="c9058-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="c9058-144">Förbereder.</span><span class="sxs-lookup"><span data-stu-id="c9058-144">Ready.</span></span>
<span data-ttu-id="c9058-145">Data bearbetningen är klar och data sektorn är klar.</span><span class="sxs-lookup"><span data-stu-id="c9058-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="c9058-146">Inaktive.</span><span class="sxs-lookup"><span data-stu-id="c9058-146">InProgress.</span></span>
<span data-ttu-id="c9058-147">Data bearbetning pågår.</span><span class="sxs-lookup"><span data-stu-id="c9058-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="c9058-148">Startade.</span><span class="sxs-lookup"><span data-stu-id="c9058-148">Failed.</span></span>
<span data-ttu-id="c9058-149">Data bearbetning misslyckades.</span><span class="sxs-lookup"><span data-stu-id="c9058-149">Data processing failed.</span></span>
- <span data-ttu-id="c9058-150">Hoppas över.</span><span class="sxs-lookup"><span data-stu-id="c9058-150">Skipped.</span></span>
<span data-ttu-id="c9058-151">Hoppade över bearbetningen av data sektorn.</span><span class="sxs-lookup"><span data-stu-id="c9058-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="c9058-152">-UpdateType</span></span>
<span data-ttu-id="c9058-153">Anger typen av uppdatering för segmentet.</span><span class="sxs-lookup"><span data-stu-id="c9058-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="c9058-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c9058-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9058-155">Koncentration.</span><span class="sxs-lookup"><span data-stu-id="c9058-155">Individual.</span></span>
<span data-ttu-id="c9058-156">Anger statusen för varje sektor för data uppsättningen i angivet tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="c9058-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="c9058-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="c9058-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="c9058-158">Anger statusen för varje sektor för data uppsättningen och alla underordnade data mängder, som används som data data mängder för aktiviteter i pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9058-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9058-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9058-159">CommonParameters</span></span>
<span data-ttu-id="c9058-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9058-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9058-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9058-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9058-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9058-162">INPUTS</span></span>

### <span data-ttu-id="c9058-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="c9058-163">None</span></span>
<span data-ttu-id="c9058-164">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c9058-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9058-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9058-165">OUTPUTS</span></span>

### <span data-ttu-id="c9058-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9058-166">System.Boolean</span></span>

## <span data-ttu-id="c9058-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9058-167">NOTES</span></span>
* <span data-ttu-id="c9058-168">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="c9058-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c9058-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9058-169">RELATED LINKS</span></span>

[<span data-ttu-id="c9058-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="c9058-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)

