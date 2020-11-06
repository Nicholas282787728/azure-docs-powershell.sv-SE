---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576677"
---
# <span data-ttu-id="47924-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="47924-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="47924-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47924-102">SYNOPSIS</span></span>
<span data-ttu-id="47924-103">Hämtar standard definitionen för en funktion i Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="47924-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47924-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47924-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47924-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47924-105">DESCRIPTION</span></span>
<span data-ttu-id="47924-106">Cmdleten **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** hämtar standard definitionen för en funktion i Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="47924-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="47924-107">Du kan använda standard definitionen och New-AzureRmStreamAnalyticsFunction cmdlet för att skapa en funktion.</span><span class="sxs-lookup"><span data-stu-id="47924-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="47924-108">Du kan ändra standard definitionen innan du skapar en funktion.</span><span class="sxs-lookup"><span data-stu-id="47924-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="47924-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47924-109">EXAMPLES</span></span>

### <span data-ttu-id="47924-110">Exempel 1: Hämta standard definitionen för en ström analys funktion</span><span class="sxs-lookup"><span data-stu-id="47924-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="47924-111">Det här kommandot får standard definitionen för funktionen ScoreTweet genom att använda parametrarna som anges i RetrieveDefaultDefinitionRequest.jsi filen.</span><span class="sxs-lookup"><span data-stu-id="47924-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="47924-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47924-112">PARAMETERS</span></span>

### <span data-ttu-id="47924-113">-Fil</span><span class="sxs-lookup"><span data-stu-id="47924-113">-File</span></span>
<span data-ttu-id="47924-114">Anger sökvägen till en. JSON-fil som innehåller JSON-representationen av brödtext för begäran om att hämta standardfunktionen för funktionen.</span><span class="sxs-lookup"><span data-stu-id="47924-114">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="47924-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="47924-115">-JobName</span></span>
<span data-ttu-id="47924-116">Anger namnet på det Stream analys jobb som funktionerna tillhör.</span><span class="sxs-lookup"><span data-stu-id="47924-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="47924-117">Denna cmdlet får standard definitionen för en funktion i det jobb som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="47924-117">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="47924-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="47924-118">-Name</span></span>
<span data-ttu-id="47924-119">Anger namnet på den Stream analys funktion som den här cmdleten får standard definitionen för.</span><span class="sxs-lookup"><span data-stu-id="47924-119">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="47924-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47924-120">-ResourceGroupName</span></span>
<span data-ttu-id="47924-121">Anger namnet på den resurs grupp där ström analys funktioner tillhör.</span><span class="sxs-lookup"><span data-stu-id="47924-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="47924-122">Denna cmdlet får en funktions definition för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="47924-122">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="47924-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47924-123">-DefaultProfile</span></span>
<span data-ttu-id="47924-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47924-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47924-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47924-125">CommonParameters</span></span>
<span data-ttu-id="47924-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47924-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47924-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47924-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47924-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47924-128">INPUTS</span></span>

## <span data-ttu-id="47924-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47924-129">OUTPUTS</span></span>

### <span data-ttu-id="47924-130">Microsoft. Azure. commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="47924-130">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="47924-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47924-131">NOTES</span></span>

## <span data-ttu-id="47924-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47924-132">RELATED LINKS</span></span>

[<span data-ttu-id="47924-133">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="47924-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


