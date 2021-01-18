---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 5b18af8890d255dbd5514cccc0279acafe6bd611
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524216"
---
# <span data-ttu-id="9e14e-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="9e14e-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="9e14e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e14e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e14e-103">Hämtar information om aktivitets fönster som associeras med en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9e14e-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="9e14e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e14e-104">SYNTAX</span></span>

### <span data-ttu-id="9e14e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9e14e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e14e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9e14e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e14e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e14e-107">DESCRIPTION</span></span>
<span data-ttu-id="9e14e-108">Cmdleten **Get-AzDataFactoryActivityWindow** hämtar information om aktivitetens fönster som associeras med en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9e14e-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="9e14e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e14e-109">EXAMPLES</span></span>

### <span data-ttu-id="9e14e-110">Exempel 1: Hämta aktivitets fönster som associeras med en data fabrik</span><span class="sxs-lookup"><span data-stu-id="9e14e-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="9e14e-111">Det här kommandot får information om allt aktivitets fönster som är associerat med data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9e14e-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="9e14e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e14e-112">PARAMETERS</span></span>

### <span data-ttu-id="9e14e-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="9e14e-113">-ActivityName</span></span>
<span data-ttu-id="9e14e-114">Anger namnet på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="9e14e-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="9e14e-115">Denna cmdlet får aktivitets fönster för den aktivitet som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9e14e-116">-DataFactory</span></span>
<span data-ttu-id="9e14e-117">Anger ett **PSDataFactory** -objekt som returneras av en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e14e-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="9e14e-118">Denna cmdlet får aktivitets fönster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9e14e-119">-DataFactoryName</span></span>
<span data-ttu-id="9e14e-120">Anger namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9e14e-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="9e14e-121">Denna cmdlet får aktivitets fönster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="9e14e-122">-DatasetName</span></span>
<span data-ttu-id="9e14e-123">Anger namnet på data mängden.</span><span class="sxs-lookup"><span data-stu-id="9e14e-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="9e14e-124">Denna cmdlet hämtar aktivitets fönster som tillhör den dataset som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e14e-125">-DefaultProfile</span></span>
<span data-ttu-id="9e14e-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9e14e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e14e-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="9e14e-127">-Filter</span></span>
<span data-ttu-id="9e14e-128">Anger aktivitets fönstret som uttrycks med Azure Search filter-grammatikkontroll.</span><span class="sxs-lookup"><span data-stu-id="9e14e-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="9e14e-129">Information om grammatik finns i syntaxen för OData-uttryck för Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) i MSDN.</span><span class="sxs-lookup"><span data-stu-id="9e14e-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="9e14e-130">Aktivitets listan i Windows filtreras efter den Sök sträng som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="9e14e-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9e14e-131">-OrderBy</span></span>
<span data-ttu-id="9e14e-132">Anger om du vill ordna svaret från en av parametrarna för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="9e14e-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="9e14e-133">Det här är en lista med kommaavgränsade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9e14e-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="9e14e-134">Till exempel: WindowStart, procent färdigt.</span><span class="sxs-lookup"><span data-stu-id="9e14e-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="9e14e-135">Som standard är ordern stigande ordning (ASC).</span><span class="sxs-lookup"><span data-stu-id="9e14e-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="9e14e-136">Ange DESC om du vill ordna listan i fallande ordning.</span><span class="sxs-lookup"><span data-stu-id="9e14e-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="9e14e-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="9e14e-137">-PipelineName</span></span>
<span data-ttu-id="9e14e-138">Anger namnet på pipelinen.</span><span class="sxs-lookup"><span data-stu-id="9e14e-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="9e14e-139">Denna cmdlet får aktivitets fönster som tillhör den pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e14e-140">-ResourceGroupName</span></span>
<span data-ttu-id="9e14e-141">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e14e-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9e14e-142">Denna cmdlet får aktivitets fönster som tillhör resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="9e14e-143">-RunEnd</span></span>
<span data-ttu-id="9e14e-144">Anger slut tiden för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="9e14e-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="9e14e-145">Denna cmdlet får aktivitets fönster vars kör tider går mellan *RunStart* och *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="9e14e-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="9e14e-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="9e14e-146">-RunStart</span></span>
<span data-ttu-id="9e14e-147">Anger start tiden för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="9e14e-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="9e14e-148">Denna cmdlet får aktivitets fönster vars kör tider går mellan *RunStart* och *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="9e14e-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="9e14e-149">-Överst</span><span class="sxs-lookup"><span data-stu-id="9e14e-149">-Top</span></span>
<span data-ttu-id="9e14e-150">Anger det maximala antalet aktivitets fönster som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="9e14e-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="9e14e-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="9e14e-151">-WindowEnd</span></span>
<span data-ttu-id="9e14e-152">Anger fönstret slut tid för aktivitet.</span><span class="sxs-lookup"><span data-stu-id="9e14e-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="9e14e-153">Denna cmdlet får aktivitets fönster vars tider infaller mellan *WindowStart* och *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="9e14e-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="9e14e-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="9e14e-154">-WindowStart</span></span>
<span data-ttu-id="9e14e-155">Anger start tiden för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="9e14e-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="9e14e-156">Denna cmdlet får aktivitets fönster vars tider infaller mellan *WindowStart* och *WindowEnd* .</span><span class="sxs-lookup"><span data-stu-id="9e14e-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="9e14e-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="9e14e-157">-WindowState</span></span>
<span data-ttu-id="9e14e-158">Anger statusen för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="9e14e-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="9e14e-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9e14e-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e14e-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e14e-160">None</span></span>
- <span data-ttu-id="9e14e-161">Godkänna</span><span class="sxs-lookup"><span data-stu-id="9e14e-161">Waiting</span></span>
- <span data-ttu-id="9e14e-162">Inaktive</span><span class="sxs-lookup"><span data-stu-id="9e14e-162">InProgress</span></span>
- <span data-ttu-id="9e14e-163">Förbereder</span><span class="sxs-lookup"><span data-stu-id="9e14e-163">Ready</span></span>
- <span data-ttu-id="9e14e-164">Startade</span><span class="sxs-lookup"><span data-stu-id="9e14e-164">Failed</span></span>
- <span data-ttu-id="9e14e-165">Hoppat över denna cmdlet får aktivitets fönster som är i det tillstånd som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="9e14e-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="9e14e-166">-WindowSubstate</span></span>
<span data-ttu-id="9e14e-167">Anger under tillståndet för aktivitets fönstret.</span><span class="sxs-lookup"><span data-stu-id="9e14e-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="9e14e-168">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9e14e-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9e14e-169">Avbrytas</span><span class="sxs-lookup"><span data-stu-id="9e14e-169">Canceled</span></span>
- <span data-ttu-id="9e14e-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="9e14e-170">timedOut</span></span>
- <span data-ttu-id="9e14e-171">Validerar denna cmdlet får aktivitets fönster som är i det under tillstånd som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9e14e-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e14e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e14e-172">CommonParameters</span></span>
<span data-ttu-id="9e14e-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e14e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e14e-174">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e14e-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e14e-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e14e-175">INPUTS</span></span>

### <span data-ttu-id="9e14e-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9e14e-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9e14e-177">System. String</span><span class="sxs-lookup"><span data-stu-id="9e14e-177">System.String</span></span>

### <span data-ttu-id="9e14e-178">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e14e-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e14e-179">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e14e-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9e14e-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e14e-180">OUTPUTS</span></span>

### <span data-ttu-id="9e14e-181">Microsoft. Azure. commands. DataFactories. Models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="9e14e-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="9e14e-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e14e-182">NOTES</span></span>

## <span data-ttu-id="9e14e-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e14e-183">RELATED LINKS</span></span>

[<span data-ttu-id="9e14e-184">Cmdletar för Azure Data Factorrs</span><span class="sxs-lookup"><span data-stu-id="9e14e-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


