---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 833ad7d57259d9a1f308c676ba49a93935d7e045
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925745"
---
# <span data-ttu-id="681fb-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="681fb-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="681fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="681fb-102">SYNOPSIS</span></span>
<span data-ttu-id="681fb-103">Skapar eller uppdaterar en omvandling i ett jobb.</span><span class="sxs-lookup"><span data-stu-id="681fb-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="681fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="681fb-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="681fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="681fb-105">DESCRIPTION</span></span>
<span data-ttu-id="681fb-106">Cmdleten **New-AzStreamAnalyticsTransformation** skapar en Transformation i ett Stream Analytics-jobb eller uppdaterar den befintliga transformeringen.</span><span class="sxs-lookup"><span data-stu-id="681fb-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="681fb-107">Namnet på omvandlingen kan anges i. JSON-fil eller kommando rad.</span><span class="sxs-lookup"><span data-stu-id="681fb-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="681fb-108">Om båda anges måste namnet på kommando raden stämma överens med namnet i filen.</span><span class="sxs-lookup"><span data-stu-id="681fb-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="681fb-109">Om du anger en transformering som redan finns och inte anger parametern Force frågar cmdleten om den befintliga omvandlingen ska ersättas eller inte.</span><span class="sxs-lookup"><span data-stu-id="681fb-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="681fb-110">Om du anger parametern *Force* och anger ett befintligt Transformations namn, ersätts transformeringen utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="681fb-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="681fb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="681fb-111">EXAMPLES</span></span>

### <span data-ttu-id="681fb-112">EXEMPEL 1: skapa eller ersätta en omvandling i ett jobb</span><span class="sxs-lookup"><span data-stu-id="681fb-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="681fb-113">Det här kommandot skapar en transformering med namnet StreamingJobTransform i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="681fb-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="681fb-114">Om en befintlig transformering redan har definierats med det namnet får du en fråga om du vill ersätta den med cmdleten.</span><span class="sxs-lookup"><span data-stu-id="681fb-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="681fb-115">EXEMPEL 2: ersätta en omvandling i ett jobb</span><span class="sxs-lookup"><span data-stu-id="681fb-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="681fb-116">Det här kommandot ersätter definitionen av StreamingJobTransform i jobbet StreamingJob utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="681fb-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="681fb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="681fb-117">PARAMETERS</span></span>

### <span data-ttu-id="681fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="681fb-118">-DefaultProfile</span></span>
<span data-ttu-id="681fb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="681fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="681fb-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="681fb-120">-File</span></span>
<span data-ttu-id="681fb-121">Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-omvandlingen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="681fb-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="681fb-122">-Force</span></span>
<span data-ttu-id="681fb-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="681fb-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fb-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="681fb-124">-JobName</span></span>
<span data-ttu-id="681fb-125">Anger namnet på Azure Stream Analytics-jobbet under vilket Azure Stream Analytics-transformeringen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="681fb-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="681fb-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="681fb-126">-Name</span></span>
<span data-ttu-id="681fb-127">Anger namnet på den Azure Stream Analytics-transformering som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="681fb-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="681fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="681fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="681fb-129">Anger namnet på den resurs grupp under vilken Azure Stream Analytics-transformeringen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="681fb-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="681fb-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="681fb-130">-Confirm</span></span>
<span data-ttu-id="681fb-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="681fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="681fb-132">-WhatIf</span></span>
<span data-ttu-id="681fb-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="681fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="681fb-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="681fb-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="681fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="681fb-135">CommonParameters</span></span>
<span data-ttu-id="681fb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="681fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="681fb-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="681fb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="681fb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="681fb-138">INPUTS</span></span>

### <span data-ttu-id="681fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="681fb-139">System.String</span></span>

## <span data-ttu-id="681fb-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="681fb-140">OUTPUTS</span></span>

### <span data-ttu-id="681fb-141">Microsoft. Azure. commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="681fb-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="681fb-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="681fb-142">NOTES</span></span>

## <span data-ttu-id="681fb-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="681fb-143">RELATED LINKS</span></span>

[<span data-ttu-id="681fb-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="681fb-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)

