---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576676"
---
# <span data-ttu-id="742a4-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="742a4-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="742a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="742a4-102">SYNOPSIS</span></span>
<span data-ttu-id="742a4-103">Hämtar funktioner i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="742a4-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="742a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="742a4-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="742a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="742a4-105">DESCRIPTION</span></span>
<span data-ttu-id="742a4-106">Cmdleten **Get-AzureRmStreamAnalyticsFunction** hämtar en lista över de funktioner som har definierats i ett Azure Stream Analytics-jobb eller information om en specifik funktion.</span><span class="sxs-lookup"><span data-stu-id="742a4-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="742a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="742a4-107">EXAMPLES</span></span>

### <span data-ttu-id="742a4-108">Exempel 1: Hämta alla ström analys funktioner</span><span class="sxs-lookup"><span data-stu-id="742a4-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="742a4-109">Det här kommandot får funktionerna definierade på jobbet som heter StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="742a4-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="742a4-110">Exempel 2: Hämta en specifik ström analys funktion</span><span class="sxs-lookup"><span data-stu-id="742a4-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="742a4-111">Med det här kommandot får du information om funktionen som heter ScoreTweet definierad på jobbet med namnet StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="742a4-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="742a4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="742a4-112">PARAMETERS</span></span>

### <span data-ttu-id="742a4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="742a4-113">-JobName</span></span>
<span data-ttu-id="742a4-114">Anger namnet på det Stream analys jobb som funktionerna tillhör.</span><span class="sxs-lookup"><span data-stu-id="742a4-114">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="742a4-115">Denna cmdlet får funktioner för det jobb som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="742a4-115">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="742a4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="742a4-116">-Name</span></span>
<span data-ttu-id="742a4-117">Anger namnet på den ström analys funktion som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="742a4-117">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="742a4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742a4-118">-ResourceGroupName</span></span>
<span data-ttu-id="742a4-119">Anger namnet på den resurs grupp där ström analys funktioner tillhör.</span><span class="sxs-lookup"><span data-stu-id="742a4-119">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="742a4-120">Denna cmdlet får funktioner för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="742a4-120">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="742a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742a4-121">-DefaultProfile</span></span>
<span data-ttu-id="742a4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="742a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="742a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742a4-123">CommonParameters</span></span>
<span data-ttu-id="742a4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742a4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742a4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="742a4-126">INPUTS</span></span>

## <span data-ttu-id="742a4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="742a4-127">OUTPUTS</span></span>

### <span data-ttu-id="742a4-128">System. Collections. Generic. list [Microsoft. Azure. commands. StreamAnalytics. Models. PSFunction, Microsoft. Azure. commands. StreamAnalytics], Microsoft. Azure. kommandon. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="742a4-128">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="742a4-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="742a4-129">NOTES</span></span>

## <span data-ttu-id="742a4-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="742a4-130">RELATED LINKS</span></span>

[<span data-ttu-id="742a4-131">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="742a4-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="742a4-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="742a4-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="742a4-133">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="742a4-133">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


