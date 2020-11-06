---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 7b18513a6a9e7ebbf82892500344d13f9cbc8185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579244"
---
# <span data-ttu-id="d15eb-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d15eb-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d15eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d15eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d15eb-103">Skapar eller uppdaterar utdata för ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="d15eb-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d15eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d15eb-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d15eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d15eb-105">DESCRIPTION</span></span>
<span data-ttu-id="d15eb-106">Cmdleten **New-AzureRmStreamAnalyticsOutput** skapar ett utflöde i ett Stream Analytics-jobb eller uppdaterar en befintlig utmatning.</span><span class="sxs-lookup"><span data-stu-id="d15eb-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="d15eb-107">Namnet på utdata kan anges i. JSON-fil eller kommando rad.</span><span class="sxs-lookup"><span data-stu-id="d15eb-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="d15eb-108">Om båda anges måste namnet på kommando raden stämma överens med namnet i filen.</span><span class="sxs-lookup"><span data-stu-id="d15eb-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="d15eb-109">Om du anger ett utdata som redan finns och inte anger parametern *Force* frågar cmdleten om du vill ersätta den befintliga utmatningen.</span><span class="sxs-lookup"><span data-stu-id="d15eb-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="d15eb-110">Om du anger en parameter för *Force* och anger ett befintligt utdatafil ersätts utdata utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d15eb-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="d15eb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d15eb-111">EXAMPLES</span></span>

### <span data-ttu-id="d15eb-112">EXEMPEL 1: lägga till ett utdata i ett jobb</span><span class="sxs-lookup"><span data-stu-id="d15eb-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d15eb-113">Det här kommandot skapar en ny utdata med namnet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d15eb-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="d15eb-114">Om en befintlig utdatafil med det här namnet redan har angetts frågar cmdleten om den ska ersätta den.</span><span class="sxs-lookup"><span data-stu-id="d15eb-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d15eb-115">EXEMPEL 2: byta ut en utskrifts definition</span><span class="sxs-lookup"><span data-stu-id="d15eb-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="d15eb-116">Det här kommandot ersätter definitionen för utdata i jobbet som heter StreamingJob utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d15eb-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="d15eb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d15eb-117">PARAMETERS</span></span>

### <span data-ttu-id="d15eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15eb-118">-DefaultProfile</span></span>
<span data-ttu-id="d15eb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d15eb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d15eb-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="d15eb-120">-File</span></span>
<span data-ttu-id="d15eb-121">Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-utdata som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d15eb-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d15eb-122">-Force</span></span>
<span data-ttu-id="d15eb-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d15eb-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d15eb-124">-JobName</span></span>
<span data-ttu-id="d15eb-125">Anger namnet på Azure Stream Analytics-jobbet som du vill skapa Azure Stream Analytics-utdata för.</span><span class="sxs-lookup"><span data-stu-id="d15eb-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="d15eb-126">-Name</span></span>
<span data-ttu-id="d15eb-127">Anger namnet på den Azure Stream Analytics-utdata som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d15eb-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d15eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="d15eb-129">Anger namnet på den resurs grupp som du vill skapa Azure Stream Analytics-utdata under.</span><span class="sxs-lookup"><span data-stu-id="d15eb-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d15eb-130">-Confirm</span></span>
<span data-ttu-id="d15eb-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d15eb-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15eb-132">-WhatIf</span></span>
<span data-ttu-id="d15eb-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d15eb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d15eb-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d15eb-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d15eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15eb-135">CommonParameters</span></span>
<span data-ttu-id="d15eb-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d15eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15eb-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15eb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15eb-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d15eb-138">INPUTS</span></span>

### <span data-ttu-id="d15eb-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="d15eb-139">None</span></span>
<span data-ttu-id="d15eb-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d15eb-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d15eb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d15eb-141">OUTPUTS</span></span>

### <span data-ttu-id="d15eb-142">Microsoft. Azure. commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="d15eb-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="d15eb-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d15eb-143">NOTES</span></span>

## <span data-ttu-id="d15eb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d15eb-144">RELATED LINKS</span></span>

[<span data-ttu-id="d15eb-145">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d15eb-145">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="d15eb-146">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d15eb-146">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="d15eb-147">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d15eb-147">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


