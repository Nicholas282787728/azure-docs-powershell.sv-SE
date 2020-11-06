---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 5d56c0523077ee8a45b2a41175ca54c5a0e10907
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585267"
---
# <span data-ttu-id="e22db-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e22db-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="e22db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e22db-102">SYNOPSIS</span></span>
<span data-ttu-id="e22db-103">Skapar eller uppdaterar ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="e22db-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e22db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e22db-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e22db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e22db-105">DESCRIPTION</span></span>
<span data-ttu-id="e22db-106">Cmdleten **New-AzureRmStreamAnalyticsJob** skapar ett nytt ström analys jobb i Azure eller uppdaterar definitionen av ett befintligt angivet jobb.</span><span class="sxs-lookup"><span data-stu-id="e22db-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="e22db-107">Namnet på jobbet kan anges i. JSON-fil eller kommando rad.</span><span class="sxs-lookup"><span data-stu-id="e22db-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="e22db-108">Om båda anges måste namnet på kommando raden stämma överens med namnet i filen.</span><span class="sxs-lookup"><span data-stu-id="e22db-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="e22db-109">Om du anger ett jobbnamn som redan finns och inte anger parametern *Force* frågar cmdleten om du vill ersätta det befintliga jobbet.</span><span class="sxs-lookup"><span data-stu-id="e22db-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>

<span data-ttu-id="e22db-110">Om du anger parametern *Force* och anger ett befintligt jobbnamn ersätts jobb definitionen utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e22db-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="e22db-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e22db-111">EXAMPLES</span></span>

### <span data-ttu-id="e22db-112">EXEMPEL 1: skapa ett jobb</span><span class="sxs-lookup"><span data-stu-id="e22db-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="e22db-113">Det här kommandot skapar ett jobb från definitionen i JobDefinition.jspå.</span><span class="sxs-lookup"><span data-stu-id="e22db-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="e22db-114">Om ett befintligt jobb med det angivna namnet i jobb definitions filen redan har definierats frågar cmdleten om den ska ersättas eller inte.</span><span class="sxs-lookup"><span data-stu-id="e22db-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="e22db-115">EXEMPEL 2: ersätta en jobb definition</span><span class="sxs-lookup"><span data-stu-id="e22db-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="e22db-116">Det här kommandot ersätter jobb definitionen för StreamingJob utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e22db-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="e22db-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e22db-117">PARAMETERS</span></span>

### <span data-ttu-id="e22db-118">-Fil</span><span class="sxs-lookup"><span data-stu-id="e22db-118">-File</span></span>
<span data-ttu-id="e22db-119">Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-jobbet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e22db-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="e22db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e22db-120">-Force</span></span>
<span data-ttu-id="e22db-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e22db-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e22db-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e22db-122">-Name</span></span>
<span data-ttu-id="e22db-123">Anger namnet på Azure Stream Analytics-jobbet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e22db-123">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="e22db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22db-124">-ResourceGroupName</span></span>
<span data-ttu-id="e22db-125">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet ska tillhöra.</span><span class="sxs-lookup"><span data-stu-id="e22db-125">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="e22db-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e22db-126">-Confirm</span></span>
<span data-ttu-id="e22db-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e22db-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22db-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22db-128">-WhatIf</span></span>
<span data-ttu-id="e22db-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e22db-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e22db-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e22db-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22db-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22db-131">-DefaultProfile</span></span>
<span data-ttu-id="e22db-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e22db-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e22db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22db-133">CommonParameters</span></span>
<span data-ttu-id="e22db-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22db-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e22db-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22db-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e22db-136">INPUTS</span></span>

## <span data-ttu-id="e22db-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e22db-137">OUTPUTS</span></span>

### <span data-ttu-id="e22db-138">Microsoft. Azure. commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="e22db-138">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="e22db-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e22db-139">NOTES</span></span>

## <span data-ttu-id="e22db-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e22db-140">RELATED LINKS</span></span>

[<span data-ttu-id="e22db-141">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e22db-141">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e22db-142">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e22db-142">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e22db-143">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e22db-143">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e22db-144">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e22db-144">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e22db-145">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e22db-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


