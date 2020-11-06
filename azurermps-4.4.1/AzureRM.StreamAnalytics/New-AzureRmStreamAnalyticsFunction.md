---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576670"
---
# <span data-ttu-id="e3c44-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3c44-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="e3c44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3c44-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c44-103">Skapar eller ersätter en funktion i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="e3c44-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3c44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3c44-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3c44-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3c44-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c44-106">Cmdleten **New-AzureRmStreamAnalyticsFunction** skapar en funktion i ett Azure Stream Analytics-jobb eller ersätter en befintlig funktion.</span><span class="sxs-lookup"><span data-stu-id="e3c44-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="e3c44-107">Definiera funktionen i en JSON-fil (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e3c44-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="e3c44-108">Du kan ange namnet på funktionen med hjälp av parametern *namn* eller i JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="e3c44-109">Om du anger namnet på båda sätten måste namnen vara identiska.</span><span class="sxs-lookup"><span data-stu-id="e3c44-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="e3c44-110">Om du vill ersätta en befintlig funktion anger du namnet på den befintliga funktionen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="e3c44-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3c44-111">EXAMPLES</span></span>

### <span data-ttu-id="e3c44-112">Exempel 1: skapa en Stream Analytics-funktion</span><span class="sxs-lookup"><span data-stu-id="e3c44-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="e3c44-113">Det här kommandot skapar en funktion från filen Function07.jspå.</span><span class="sxs-lookup"><span data-stu-id="e3c44-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="e3c44-114">Namnet på funktionen lagras i. JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="e3c44-115">Exempel 2: skapa en Stream Analytics-funktion med namnet ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="e3c44-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="e3c44-116">Det här kommandot skapar en funktion på jobbet med namnet ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="e3c44-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="e3c44-117">Exempel 3: ersätta en Stream Analytics-funktion</span><span class="sxs-lookup"><span data-stu-id="e3c44-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="e3c44-118">Det här kommandot ersätter definitionen av den befintliga funktionen med namnet ScoreTweet med definitionen i Function22.jspå.</span><span class="sxs-lookup"><span data-stu-id="e3c44-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="e3c44-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3c44-119">PARAMETERS</span></span>

### <span data-ttu-id="e3c44-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="e3c44-120">-File</span></span>
<span data-ttu-id="e3c44-121">Anger sökvägen till en. JSON-fil som innehåller JSON-representationen av Stream Analytics-funktionen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="e3c44-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e3c44-122">-Force</span></span>
<span data-ttu-id="e3c44-123">Anger att denna cmdlet ersätter en befintlig ström analys funktion utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e3c44-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e3c44-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="e3c44-124">-JobName</span></span>
<span data-ttu-id="e3c44-125">Anger namnet på Stream Analytics-jobbet som den här cmdleten skapar en Stream Analytics-funktion under.</span><span class="sxs-lookup"><span data-stu-id="e3c44-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="e3c44-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3c44-126">-Name</span></span>
<span data-ttu-id="e3c44-127">Anger namnet på den ström analys funktion som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="e3c44-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e3c44-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c44-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3c44-129">Anger namnet på den resurs grupp under vilken denna cmdlet skapar en Stream Analytics-funktion.</span><span class="sxs-lookup"><span data-stu-id="e3c44-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="e3c44-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3c44-130">-Confirm</span></span>
<span data-ttu-id="e3c44-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3c44-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c44-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c44-132">-WhatIf</span></span>
<span data-ttu-id="e3c44-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3c44-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c44-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3c44-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c44-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c44-135">-DefaultProfile</span></span>
<span data-ttu-id="e3c44-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c44-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c44-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c44-137">CommonParameters</span></span>
<span data-ttu-id="e3c44-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c44-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c44-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c44-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c44-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3c44-140">INPUTS</span></span>

## <span data-ttu-id="e3c44-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3c44-141">OUTPUTS</span></span>

### <span data-ttu-id="e3c44-142">Microsoft. Azure. commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="e3c44-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="e3c44-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3c44-143">NOTES</span></span>

## <span data-ttu-id="e3c44-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3c44-144">RELATED LINKS</span></span>

[<span data-ttu-id="e3c44-145">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3c44-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="e3c44-146">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3c44-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="e3c44-147">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e3c44-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


