---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269845"
---
# <span data-ttu-id="5f5ee-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5f5ee-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="5f5ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5ee-103">Hämtar funktioner i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="5f5ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f5ee-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f5ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f5ee-105">DESCRIPTION</span></span>
<span data-ttu-id="5f5ee-106">Cmdleten **Get-AzStreamAnalyticsFunction** hämtar en lista över de funktioner som har definierats i ett Azure Stream Analytics-jobb eller information om en specifik funktion.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="5f5ee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f5ee-107">EXAMPLES</span></span>

### <span data-ttu-id="5f5ee-108">Exempel 1: Hämta alla ström analys funktioner</span><span class="sxs-lookup"><span data-stu-id="5f5ee-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="5f5ee-109">Det här kommandot får funktionerna definierade på jobbet som heter StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="5f5ee-110">Exempel 2: Hämta en specifik ström analys funktion</span><span class="sxs-lookup"><span data-stu-id="5f5ee-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="5f5ee-111">Med det här kommandot får du information om funktionen som heter ScoreTweet definierad på jobbet med namnet StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="5f5ee-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f5ee-112">PARAMETERS</span></span>

### <span data-ttu-id="5f5ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5ee-113">-DefaultProfile</span></span>
<span data-ttu-id="5f5ee-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f5ee-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="5f5ee-115">-JobName</span></span>
<span data-ttu-id="5f5ee-116">Anger namnet på det Stream analys jobb som funktionerna tillhör.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="5f5ee-117">Denna cmdlet får funktioner för det jobb som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f5ee-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f5ee-118">-Name</span></span>
<span data-ttu-id="5f5ee-119">Anger namnet på den ström analys funktion som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f5ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f5ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f5ee-121">Anger namnet på den resurs grupp där ström analys funktioner tillhör.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="5f5ee-122">Denna cmdlet får funktioner för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f5ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5ee-123">CommonParameters</span></span>
<span data-ttu-id="5f5ee-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f5ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5ee-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5ee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5ee-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f5ee-126">INPUTS</span></span>

### <span data-ttu-id="5f5ee-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5f5ee-127">System.String</span></span>

## <span data-ttu-id="5f5ee-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f5ee-128">OUTPUTS</span></span>

### <span data-ttu-id="5f5ee-129">Microsoft. Azure. commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="5f5ee-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="5f5ee-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f5ee-130">NOTES</span></span>

## <span data-ttu-id="5f5ee-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f5ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f5ee-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5f5ee-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5f5ee-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5f5ee-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5f5ee-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5f5ee-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)

