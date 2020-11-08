---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100715"
---
# <span data-ttu-id="45d25-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45d25-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="45d25-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45d25-102">SYNOPSIS</span></span>
<span data-ttu-id="45d25-103">Skapar eller uppdaterar en utskrift.</span><span class="sxs-lookup"><span data-stu-id="45d25-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="45d25-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45d25-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45d25-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45d25-105">DESCRIPTION</span></span>
<span data-ttu-id="45d25-106">Cmdleten **New-AzStreamAnalyticsInput** skapar en inmatning i ett Stream Analytics-jobb eller uppdaterar en befintlig inmatning.</span><span class="sxs-lookup"><span data-stu-id="45d25-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="45d25-107">Namnet på indatavärdet kan anges i JSON-filen eller kommando raden.</span><span class="sxs-lookup"><span data-stu-id="45d25-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="45d25-108">Om båda anges måste namnet på kommando raden stämma överens med namnet i filen.</span><span class="sxs-lookup"><span data-stu-id="45d25-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="45d25-109">Om du anger en indata som redan finns och inte anger parametern *Force* frågar cmdleten om du vill ersätta den befintliga inmatningen.</span><span class="sxs-lookup"><span data-stu-id="45d25-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="45d25-110">Om du anger parametern *Force* och anger ett befintligt indatafil-namn, ersätts indata utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="45d25-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="45d25-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45d25-111">EXAMPLES</span></span>

### <span data-ttu-id="45d25-112">Exempel 1: skapa en jobb inmatning med en definition från en fil</span><span class="sxs-lookup"><span data-stu-id="45d25-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="45d25-113">Det här kommandot skapar en inmatning från filen Input.jspå.</span><span class="sxs-lookup"><span data-stu-id="45d25-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="45d25-114">Om en befintlig inmatning med namnet som angetts i definitions filen redan har definierats frågar cmdleten om den ska ersättas eller inte.</span><span class="sxs-lookup"><span data-stu-id="45d25-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="45d25-115">Exempel 2: skapa en inmatning</span><span class="sxs-lookup"><span data-stu-id="45d25-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="45d25-116">Det här kommandot skapar en ny inmatning för jobbet som heter EntryStream.</span><span class="sxs-lookup"><span data-stu-id="45d25-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="45d25-117">Om en befintlig inmatning med det här namnet redan har angetts frågar cmdleten om du vill ersätta den eller inte.</span><span class="sxs-lookup"><span data-stu-id="45d25-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="45d25-118">Exempel 3: ersätta en utskrift med en definition från en fil</span><span class="sxs-lookup"><span data-stu-id="45d25-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="45d25-119">Det här kommandot ersätter definitionen av den befintliga Indatakällan med namnet EntryStream med definitionen från filen utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="45d25-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="45d25-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45d25-120">PARAMETERS</span></span>

### <span data-ttu-id="45d25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d25-121">-DefaultProfile</span></span>
<span data-ttu-id="45d25-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45d25-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d25-123">-Fil</span><span class="sxs-lookup"><span data-stu-id="45d25-123">-File</span></span>
<span data-ttu-id="45d25-124">Anger sökvägen till en JSON-fil som innehåller JSON-representationen av Azure Stream Analytics-inmatning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="45d25-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="45d25-125">-Force</span><span class="sxs-lookup"><span data-stu-id="45d25-125">-Force</span></span>
<span data-ttu-id="45d25-126">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="45d25-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45d25-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="45d25-127">-JobName</span></span>
<span data-ttu-id="45d25-128">Anger namnet på Azure Stream Analytics-jobbet som du vill skapa Azure Stream Analytics-inmatning under.</span><span class="sxs-lookup"><span data-stu-id="45d25-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="45d25-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="45d25-129">-Name</span></span>
<span data-ttu-id="45d25-130">Anger namnet på den Azure Stream Analytics-inmatning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="45d25-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="45d25-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d25-131">-ResourceGroupName</span></span>
<span data-ttu-id="45d25-132">Anger namnet på den resurs grupp under vilken du vill skapa Azure streaming-inmatning.</span><span class="sxs-lookup"><span data-stu-id="45d25-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="45d25-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45d25-133">-Confirm</span></span>
<span data-ttu-id="45d25-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45d25-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d25-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d25-135">-WhatIf</span></span>
<span data-ttu-id="45d25-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45d25-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d25-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45d25-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d25-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d25-138">CommonParameters</span></span>
<span data-ttu-id="45d25-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d25-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d25-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d25-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d25-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45d25-141">INPUTS</span></span>

### <span data-ttu-id="45d25-142">System. String</span><span class="sxs-lookup"><span data-stu-id="45d25-142">System.String</span></span>

## <span data-ttu-id="45d25-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45d25-143">OUTPUTS</span></span>

### <span data-ttu-id="45d25-144">Microsoft. Azure. commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="45d25-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="45d25-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45d25-145">NOTES</span></span>

## <span data-ttu-id="45d25-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45d25-146">RELATED LINKS</span></span>

[<span data-ttu-id="45d25-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45d25-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="45d25-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45d25-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="45d25-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="45d25-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)

