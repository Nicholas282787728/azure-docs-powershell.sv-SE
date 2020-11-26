---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103377"
---
# <span data-ttu-id="96e15-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="96e15-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="96e15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96e15-102">SYNOPSIS</span></span>
<span data-ttu-id="96e15-103">Skapar eller uppdaterar utdata för ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="96e15-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="96e15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96e15-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96e15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96e15-105">DESCRIPTION</span></span>
<span data-ttu-id="96e15-106">Cmdleten **New-AzStreamAnalyticsOutput** skapar ett utflöde i ett Stream Analytics-jobb eller uppdaterar en befintlig utmatning.</span><span class="sxs-lookup"><span data-stu-id="96e15-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="96e15-107">Namnet på utdata kan anges i. JSON-fil eller kommando rad.</span><span class="sxs-lookup"><span data-stu-id="96e15-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="96e15-108">Om båda anges måste namnet på kommando raden stämma överens med namnet i filen.</span><span class="sxs-lookup"><span data-stu-id="96e15-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="96e15-109">Om du anger ett utdata som redan finns och inte anger parametern *Force* frågar cmdleten om du vill ersätta den befintliga utmatningen.</span><span class="sxs-lookup"><span data-stu-id="96e15-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="96e15-110">Om du anger en parameter för *Force* och anger ett befintligt utdatafil ersätts utdata utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="96e15-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="96e15-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96e15-111">EXAMPLES</span></span>

### <span data-ttu-id="96e15-112">Exempel 1: lägga till ett utdata i ett jobb</span><span class="sxs-lookup"><span data-stu-id="96e15-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="96e15-113">Det här kommandot skapar en ny utdata med namnet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="96e15-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="96e15-114">Om en befintlig utdatafil med det här namnet redan har angetts frågar cmdleten om den ska ersätta den.</span><span class="sxs-lookup"><span data-stu-id="96e15-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="96e15-115">Exempel 2: byta ut en utskrifts definition</span><span class="sxs-lookup"><span data-stu-id="96e15-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="96e15-116">Det här kommandot ersätter definitionen för utdata i jobbet som heter StreamingJob utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="96e15-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="96e15-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96e15-117">PARAMETERS</span></span>

### <span data-ttu-id="96e15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e15-118">-DefaultProfile</span></span>
<span data-ttu-id="96e15-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96e15-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96e15-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="96e15-120">-File</span></span>
<span data-ttu-id="96e15-121">Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-utdata som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96e15-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="96e15-122">-Force</span><span class="sxs-lookup"><span data-stu-id="96e15-122">-Force</span></span>
<span data-ttu-id="96e15-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="96e15-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96e15-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="96e15-124">-JobName</span></span>
<span data-ttu-id="96e15-125">Anger namnet på Azure Stream Analytics-jobbet som du vill skapa Azure Stream Analytics-utdata för.</span><span class="sxs-lookup"><span data-stu-id="96e15-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="96e15-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="96e15-126">-Name</span></span>
<span data-ttu-id="96e15-127">Anger namnet på den Azure Stream Analytics-utdata som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="96e15-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="96e15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e15-128">-ResourceGroupName</span></span>
<span data-ttu-id="96e15-129">Anger namnet på den resurs grupp som du vill skapa Azure Stream Analytics-utdata under.</span><span class="sxs-lookup"><span data-stu-id="96e15-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="96e15-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96e15-130">-Confirm</span></span>
<span data-ttu-id="96e15-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96e15-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e15-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e15-132">-WhatIf</span></span>
<span data-ttu-id="96e15-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96e15-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e15-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96e15-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e15-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e15-135">CommonParameters</span></span>
<span data-ttu-id="96e15-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e15-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e15-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e15-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e15-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96e15-138">INPUTS</span></span>

### <span data-ttu-id="96e15-139">System. String</span><span class="sxs-lookup"><span data-stu-id="96e15-139">System.String</span></span>

## <span data-ttu-id="96e15-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96e15-140">OUTPUTS</span></span>

### <span data-ttu-id="96e15-141">Microsoft. Azure. commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="96e15-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="96e15-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96e15-142">NOTES</span></span>

## <span data-ttu-id="96e15-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96e15-143">RELATED LINKS</span></span>

[<span data-ttu-id="96e15-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="96e15-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="96e15-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="96e15-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="96e15-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="96e15-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)

