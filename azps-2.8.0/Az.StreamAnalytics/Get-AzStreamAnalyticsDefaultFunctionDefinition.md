---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 217b9f8775f38635cf2285215a0be10a92b832c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919536"
---
# <span data-ttu-id="08811-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="08811-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="08811-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08811-102">SYNOPSIS</span></span>
<span data-ttu-id="08811-103">Hämtar standard definitionen för en funktion i Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="08811-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="08811-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08811-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08811-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08811-105">DESCRIPTION</span></span>
<span data-ttu-id="08811-106">Cmdleten **Get-AzStreamAnalyticsDefaultFunctionDefinition** hämtar standard definitionen för en funktion i Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="08811-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="08811-107">Du kan använda standard definitionen och New-AzStreamAnalyticsFunction cmdlet för att skapa en funktion.</span><span class="sxs-lookup"><span data-stu-id="08811-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="08811-108">Du kan ändra standard definitionen innan du skapar en funktion.</span><span class="sxs-lookup"><span data-stu-id="08811-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="08811-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08811-109">EXAMPLES</span></span>

### <span data-ttu-id="08811-110">Exempel 1: Hämta standard definitionen för en ström analys funktion</span><span class="sxs-lookup"><span data-stu-id="08811-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="08811-111">Det här kommandot får standard definitionen för funktionen ScoreTweet genom att använda parametrarna som anges i RetrieveDefaultDefinitionRequest.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="08811-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="08811-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08811-112">PARAMETERS</span></span>

### <span data-ttu-id="08811-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08811-113">-DefaultProfile</span></span>
<span data-ttu-id="08811-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08811-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08811-115">-Fil</span><span class="sxs-lookup"><span data-stu-id="08811-115">-File</span></span>
<span data-ttu-id="08811-116">Anger sökvägen till en. JSON-fil som innehåller JSON-representationen av brödtext för begäran om att hämta standardfunktionen för funktionen.</span><span class="sxs-lookup"><span data-stu-id="08811-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="08811-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="08811-117">-JobName</span></span>
<span data-ttu-id="08811-118">Anger namnet på det Stream analys jobb som funktionerna tillhör.</span><span class="sxs-lookup"><span data-stu-id="08811-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="08811-119">Denna cmdlet får standard definitionen för en funktion i det jobb som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="08811-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="08811-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="08811-120">-Name</span></span>
<span data-ttu-id="08811-121">Anger namnet på den Stream analys funktion som den här cmdleten får standard definitionen för.</span><span class="sxs-lookup"><span data-stu-id="08811-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08811-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08811-122">-ResourceGroupName</span></span>
<span data-ttu-id="08811-123">Anger namnet på den resurs grupp där ström analys funktioner tillhör.</span><span class="sxs-lookup"><span data-stu-id="08811-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="08811-124">Denna cmdlet får en funktions definition för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="08811-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="08811-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08811-125">CommonParameters</span></span>
<span data-ttu-id="08811-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08811-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08811-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08811-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08811-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08811-128">INPUTS</span></span>

### <span data-ttu-id="08811-129">System. String</span><span class="sxs-lookup"><span data-stu-id="08811-129">System.String</span></span>

## <span data-ttu-id="08811-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08811-130">OUTPUTS</span></span>

### <span data-ttu-id="08811-131">Microsoft. Azure. commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="08811-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="08811-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08811-132">NOTES</span></span>

## <span data-ttu-id="08811-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08811-133">RELATED LINKS</span></span>

[<span data-ttu-id="08811-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="08811-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


