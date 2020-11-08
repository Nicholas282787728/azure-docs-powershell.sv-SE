---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103379"
---
# <span data-ttu-id="50b60-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="50b60-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="50b60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50b60-102">SYNOPSIS</span></span>
<span data-ttu-id="50b60-103">Skapar eller uppdaterar ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="50b60-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="50b60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50b60-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50b60-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50b60-105">DESCRIPTION</span></span>
<span data-ttu-id="50b60-106">Cmdleten **New-AzStreamAnalyticsJob** skapar ett nytt ström analys jobb i Azure eller uppdaterar definitionen av ett befintligt angivet jobb.</span><span class="sxs-lookup"><span data-stu-id="50b60-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="50b60-107">Namnet på jobbet kan anges i. JSON-fil eller kommando rad.</span><span class="sxs-lookup"><span data-stu-id="50b60-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="50b60-108">Om båda anges måste namnet på kommando raden stämma överens med namnet i filen.</span><span class="sxs-lookup"><span data-stu-id="50b60-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="50b60-109">Om du anger ett jobbnamn som redan finns och inte anger parametern *Force* frågar cmdleten om du vill ersätta det befintliga jobbet.</span><span class="sxs-lookup"><span data-stu-id="50b60-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="50b60-110">Om du anger parametern *Force* och anger ett befintligt jobbnamn ersätts jobb definitionen utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="50b60-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="50b60-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50b60-111">EXAMPLES</span></span>

### <span data-ttu-id="50b60-112">EXEMPEL 1: skapa ett jobb</span><span class="sxs-lookup"><span data-stu-id="50b60-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="50b60-113">Det här kommandot skapar ett jobb från definitionen i JobDefinition.jspå.</span><span class="sxs-lookup"><span data-stu-id="50b60-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="50b60-114">Om ett befintligt jobb med det angivna namnet i jobb definitions filen redan har definierats frågar cmdleten om den ska ersättas eller inte.</span><span class="sxs-lookup"><span data-stu-id="50b60-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="50b60-115">EXEMPEL 2: ersätta en jobb definition</span><span class="sxs-lookup"><span data-stu-id="50b60-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="50b60-116">Det här kommandot ersätter jobb definitionen för StreamingJob utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="50b60-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="50b60-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50b60-117">PARAMETERS</span></span>

### <span data-ttu-id="50b60-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b60-118">-DefaultProfile</span></span>
<span data-ttu-id="50b60-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50b60-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50b60-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="50b60-120">-File</span></span>
<span data-ttu-id="50b60-121">Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-jobbet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="50b60-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50b60-122">-Force</span><span class="sxs-lookup"><span data-stu-id="50b60-122">-Force</span></span>
<span data-ttu-id="50b60-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="50b60-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50b60-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="50b60-124">-Name</span></span>
<span data-ttu-id="50b60-125">Anger namnet på Azure Stream Analytics-jobbet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="50b60-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50b60-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b60-126">-ResourceGroupName</span></span>
<span data-ttu-id="50b60-127">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="50b60-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="50b60-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50b60-128">-Confirm</span></span>
<span data-ttu-id="50b60-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50b60-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50b60-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50b60-130">-WhatIf</span></span>
<span data-ttu-id="50b60-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50b60-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50b60-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50b60-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50b60-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b60-133">CommonParameters</span></span>
<span data-ttu-id="50b60-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b60-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b60-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b60-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b60-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50b60-136">INPUTS</span></span>

### <span data-ttu-id="50b60-137">System. String</span><span class="sxs-lookup"><span data-stu-id="50b60-137">System.String</span></span>

## <span data-ttu-id="50b60-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50b60-138">OUTPUTS</span></span>

### <span data-ttu-id="50b60-139">Microsoft. Azure. commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="50b60-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="50b60-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50b60-140">NOTES</span></span>

## <span data-ttu-id="50b60-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50b60-141">RELATED LINKS</span></span>

[<span data-ttu-id="50b60-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="50b60-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="50b60-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="50b60-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="50b60-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="50b60-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="50b60-145">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="50b60-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="50b60-146">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="50b60-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


