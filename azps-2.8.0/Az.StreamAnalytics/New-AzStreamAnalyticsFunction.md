---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 38d0c63dba4ac5cdc6b64ea3013f24a19bc048fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920978"
---
# <span data-ttu-id="7cbee-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7cbee-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="7cbee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cbee-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbee-103">Skapar eller ersätter en funktion i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="7cbee-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="7cbee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cbee-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cbee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cbee-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbee-106">Cmdleten **New-AzStreamAnalyticsFunction** skapar en funktion i ett Azure Stream Analytics-jobb eller ersätter en befintlig funktion.</span><span class="sxs-lookup"><span data-stu-id="7cbee-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="7cbee-107">Definiera funktionen i en JSON-fil (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="7cbee-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="7cbee-108">Du kan ange namnet på funktionen med hjälp av parametern *namn* eller i JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="7cbee-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="7cbee-109">Om du anger namnet på båda sätten måste namnen vara identiska.</span><span class="sxs-lookup"><span data-stu-id="7cbee-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="7cbee-110">Om du vill ersätta en befintlig funktion anger du namnet på den befintliga funktionen.</span><span class="sxs-lookup"><span data-stu-id="7cbee-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="7cbee-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cbee-111">EXAMPLES</span></span>

### <span data-ttu-id="7cbee-112">Exempel 1: skapa en Stream Analytics-funktion</span><span class="sxs-lookup"><span data-stu-id="7cbee-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="7cbee-113">Det här kommandot skapar en funktion från filen Function07.jspå.</span><span class="sxs-lookup"><span data-stu-id="7cbee-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="7cbee-114">Namnet på funktionen lagras i. JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="7cbee-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="7cbee-115">Exempel 2: skapa en Stream Analytics-funktion med namnet ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="7cbee-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="7cbee-116">Det här kommandot skapar en funktion på jobbet med namnet ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="7cbee-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="7cbee-117">Exempel 3: ersätta en Stream Analytics-funktion</span><span class="sxs-lookup"><span data-stu-id="7cbee-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="7cbee-118">Det här kommandot ersätter definitionen av den befintliga funktionen med namnet ScoreTweet med definitionen i Function22.jspå.</span><span class="sxs-lookup"><span data-stu-id="7cbee-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="7cbee-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cbee-119">PARAMETERS</span></span>

### <span data-ttu-id="7cbee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbee-120">-DefaultProfile</span></span>
<span data-ttu-id="7cbee-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbee-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cbee-122">-Fil</span><span class="sxs-lookup"><span data-stu-id="7cbee-122">-File</span></span>
<span data-ttu-id="7cbee-123">Anger sökvägen till en. JSON-fil som innehåller JSON-representationen av Stream Analytics-funktionen.</span><span class="sxs-lookup"><span data-stu-id="7cbee-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="7cbee-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7cbee-124">-Force</span></span>
<span data-ttu-id="7cbee-125">Anger att denna cmdlet ersätter en befintlig ström analys funktion utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7cbee-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7cbee-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="7cbee-126">-JobName</span></span>
<span data-ttu-id="7cbee-127">Anger namnet på Stream Analytics-jobbet som den här cmdleten skapar en Stream Analytics-funktion under.</span><span class="sxs-lookup"><span data-stu-id="7cbee-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="7cbee-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cbee-128">-Name</span></span>
<span data-ttu-id="7cbee-129">Anger namnet på den ström analys funktion som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="7cbee-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7cbee-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbee-130">-ResourceGroupName</span></span>
<span data-ttu-id="7cbee-131">Anger namnet på den resurs grupp under vilken denna cmdlet skapar en Stream Analytics-funktion.</span><span class="sxs-lookup"><span data-stu-id="7cbee-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="7cbee-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cbee-132">-Confirm</span></span>
<span data-ttu-id="7cbee-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cbee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbee-134">-WhatIf</span></span>
<span data-ttu-id="7cbee-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cbee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cbee-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cbee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbee-137">CommonParameters</span></span>
<span data-ttu-id="7cbee-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbee-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cbee-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbee-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cbee-140">INPUTS</span></span>

### <span data-ttu-id="7cbee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7cbee-141">System.String</span></span>

## <span data-ttu-id="7cbee-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cbee-142">OUTPUTS</span></span>

### <span data-ttu-id="7cbee-143">Microsoft. Azure. commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="7cbee-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="7cbee-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cbee-144">NOTES</span></span>

## <span data-ttu-id="7cbee-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cbee-145">RELATED LINKS</span></span>

[<span data-ttu-id="7cbee-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7cbee-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="7cbee-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7cbee-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="7cbee-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7cbee-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)

