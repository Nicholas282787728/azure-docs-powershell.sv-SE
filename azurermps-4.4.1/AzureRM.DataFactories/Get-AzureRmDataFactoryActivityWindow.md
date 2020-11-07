---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755460"
---
# <span data-ttu-id="6874d-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="6874d-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="6874d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6874d-102">SYNOPSIS</span></span>
<span data-ttu-id="6874d-103">Hämtar information om aktivitets fönster som associeras med en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="6874d-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6874d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6874d-104">SYNTAX</span></span>

### <span data-ttu-id="6874d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="6874d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6874d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6874d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6874d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6874d-107">DESCRIPTION</span></span>
<span data-ttu-id="6874d-108">Cmdleten **Get-AzureRmDataFactoryActivityWindow** hämtar information om aktivitetens fönster som associeras med en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="6874d-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="6874d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6874d-109">EXAMPLES</span></span>

### <span data-ttu-id="6874d-110">Exempel 1: Hämta aktivitets fönster som associeras med en data fabrik</span><span class="sxs-lookup"><span data-stu-id="6874d-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="6874d-111">Det här kommandot får information om allt aktivitets fönster som är associerat med data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6874d-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="6874d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6874d-112">PARAMETERS</span></span>

### <span data-ttu-id="6874d-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="6874d-113">-ActivityName</span></span>
<span data-ttu-id="6874d-114">Anger namnet på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="6874d-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="6874d-115">Denna cmdlet får aktivitets fönster för den aktivitet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6874d-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6874d-116">-DataFactory</span></span>
<span data-ttu-id="6874d-117">Anger ett **PSDataFactory** -objekt som returneras av en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6874d-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="6874d-118">Denna cmdlet får aktivitets fönster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6874d-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6874d-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6874d-119">-DataFactoryName</span></span>
<span data-ttu-id="6874d-120">Anger namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="6874d-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="6874d-121">Denna cmdlet får aktivitets fönster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6874d-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6874d-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="6874d-122">-DatasetName</span></span>
<span data-ttu-id="6874d-123">Anger namnet på data mängden.</span><span class="sxs-lookup"><span data-stu-id="6874d-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="6874d-124">Denna cmdlet hämtar aktivitets fönster som tillhör den dataset som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6874d-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="6874d-125">-Filter</span></span>
<span data-ttu-id="6874d-126">Anger aktivitets fönstret som uttrycks med Azure Search filter-grammatikkontroll.</span><span class="sxs-lookup"><span data-stu-id="6874d-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="6874d-127">Information om grammatik finns i syntaxen för OData-uttryck för Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) i MSDN.</span><span class="sxs-lookup"><span data-stu-id="6874d-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="6874d-128">Aktivitets listan i Windows filtreras efter den Sök sträng som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6874d-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6874d-129">-OrderBy</span></span>
<span data-ttu-id="6874d-130">Anger om du vill ordna svaret från en av parametrarna för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="6874d-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="6874d-131">Det här är en lista med kommaavgränsade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6874d-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="6874d-132">Till exempel: WindowStart, procent färdigt.</span><span class="sxs-lookup"><span data-stu-id="6874d-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="6874d-133">Som standard är ordern stigande ordning (ASC).</span><span class="sxs-lookup"><span data-stu-id="6874d-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="6874d-134">Ange DESC om du vill ordna listan i fallande ordning.</span><span class="sxs-lookup"><span data-stu-id="6874d-134">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="6874d-135">-PipelineName</span></span>
<span data-ttu-id="6874d-136">Anger namnet på pipelinen.</span><span class="sxs-lookup"><span data-stu-id="6874d-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="6874d-137">Denna cmdlet får aktivitets fönster som tillhör den pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6874d-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6874d-138">-ResourceGroupName</span></span>
<span data-ttu-id="6874d-139">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6874d-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="6874d-140">Denna cmdlet får aktivitets fönster som tillhör resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6874d-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6874d-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="6874d-141">-RunEnd</span></span>
<span data-ttu-id="6874d-142">Anger slut tiden för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="6874d-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="6874d-143">Denna cmdlet får aktivitets fönster vars kör tider går mellan *RunStart* och *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="6874d-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="6874d-144">-RunStart</span></span>
<span data-ttu-id="6874d-145">Anger start tiden för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="6874d-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="6874d-146">Denna cmdlet får aktivitets fönster vars kör tider går mellan *RunStart* och *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="6874d-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-147">-Överst</span><span class="sxs-lookup"><span data-stu-id="6874d-147">-Top</span></span>
<span data-ttu-id="6874d-148">Anger det maximala antalet aktivitets fönster som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="6874d-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="6874d-149">-WindowEnd</span></span>
<span data-ttu-id="6874d-150">Anger fönstret slut tid för aktivitet.</span><span class="sxs-lookup"><span data-stu-id="6874d-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="6874d-151">Denna cmdlet får aktivitets fönster vars tider infaller mellan *WindowStart* och *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="6874d-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="6874d-152">-WindowStart</span></span>
<span data-ttu-id="6874d-153">Anger start tiden för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="6874d-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="6874d-154">Denna cmdlet får aktivitets fönster vars tider infaller mellan *WindowStart* och *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="6874d-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="6874d-155">-WindowState</span></span>
<span data-ttu-id="6874d-156">Anger statusen för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="6874d-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="6874d-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6874d-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6874d-158">Ingen</span><span class="sxs-lookup"><span data-stu-id="6874d-158">None</span></span>
- <span data-ttu-id="6874d-159">Godkänna</span><span class="sxs-lookup"><span data-stu-id="6874d-159">Waiting</span></span>
- <span data-ttu-id="6874d-160">Inaktive</span><span class="sxs-lookup"><span data-stu-id="6874d-160">InProgress</span></span>
- <span data-ttu-id="6874d-161">Förbereder</span><span class="sxs-lookup"><span data-stu-id="6874d-161">Ready</span></span>
- <span data-ttu-id="6874d-162">Startade</span><span class="sxs-lookup"><span data-stu-id="6874d-162">Failed</span></span>
- <span data-ttu-id="6874d-163">Hoppas över</span><span class="sxs-lookup"><span data-stu-id="6874d-163">Skipped</span></span>

<span data-ttu-id="6874d-164">Denna cmdlet får aktivitets fönster som är i det tillstånd som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6874d-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-165">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="6874d-165">-WindowSubstate</span></span>
<span data-ttu-id="6874d-166">Anger under tillståndet för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="6874d-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="6874d-167">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6874d-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6874d-168">Avbrytas</span><span class="sxs-lookup"><span data-stu-id="6874d-168">Canceled</span></span>
- <span data-ttu-id="6874d-169">timedOut</span><span class="sxs-lookup"><span data-stu-id="6874d-169">timedOut</span></span>
- <span data-ttu-id="6874d-170">Vilket</span><span class="sxs-lookup"><span data-stu-id="6874d-170">Validating</span></span>

<span data-ttu-id="6874d-171">Denna cmdlet får aktivitets fönster som är i det under tillstånd som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6874d-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6874d-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6874d-172">-DefaultProfile</span></span>
<span data-ttu-id="6874d-173">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6874d-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6874d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6874d-174">CommonParameters</span></span>
<span data-ttu-id="6874d-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6874d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6874d-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6874d-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6874d-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6874d-177">INPUTS</span></span>

## <span data-ttu-id="6874d-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6874d-178">OUTPUTS</span></span>

### <span data-ttu-id="6874d-179">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. commands. Utilities. PSActivyWindow, Microsoft. WindowsAzure. commands. Utilities version = 0.8.2.0; Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6874d-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="6874d-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6874d-180">NOTES</span></span>

## <span data-ttu-id="6874d-181">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6874d-181">RELATED LINKS</span></span>

[<span data-ttu-id="6874d-182">Cmdletar för Azure Data Factorrs</span><span class="sxs-lookup"><span data-stu-id="6874d-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


