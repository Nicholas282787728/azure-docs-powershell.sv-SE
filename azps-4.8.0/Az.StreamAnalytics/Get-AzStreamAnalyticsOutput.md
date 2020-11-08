---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: a2f20aa2c372261fe8f36599884c516563170293
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100724"
---
# <span data-ttu-id="7f8c4-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7f8c4-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="7f8c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8c4-103">Hämtar de utdata som definierats i ett angivet ström analys jobb eller utdata.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="7f8c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f8c4-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f8c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f8c4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f8c4-106">Cmdleten **Get-AzStreamAnalyticsOutput** visar alla utdata som är definierade i ett angivet Stream analys jobb eller får information om ett visst resultat.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="7f8c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f8c4-107">EXAMPLES</span></span>

### <span data-ttu-id="7f8c4-108">Exempel 1: Hämta information om jobb utmatningar</span><span class="sxs-lookup"><span data-stu-id="7f8c4-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="7f8c4-109">Det här kommandot returnerar information om de utdata som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="7f8c4-110">Exempel 2: Hämta information om ett visst utskrifts jobb</span><span class="sxs-lookup"><span data-stu-id="7f8c4-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="7f8c4-111">Det här kommandot returnerar information om den utdata som heter output som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="7f8c4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f8c4-112">PARAMETERS</span></span>

### <span data-ttu-id="7f8c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8c4-113">-DefaultProfile</span></span>
<span data-ttu-id="7f8c4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f8c4-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="7f8c4-115">-JobName</span></span>
<span data-ttu-id="7f8c4-116">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="7f8c4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f8c4-117">-Name</span></span>
<span data-ttu-id="7f8c4-118">Anger namnet på den Azure Stream Analytics-utdata som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="7f8c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f8c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="7f8c4-120">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="7f8c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8c4-121">CommonParameters</span></span>
<span data-ttu-id="7f8c4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8c4-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f8c4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8c4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f8c4-124">INPUTS</span></span>

### <span data-ttu-id="7f8c4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7f8c4-125">System.String</span></span>

## <span data-ttu-id="7f8c4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f8c4-126">OUTPUTS</span></span>

### <span data-ttu-id="7f8c4-127">Microsoft. Azure. commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="7f8c4-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="7f8c4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f8c4-128">NOTES</span></span>

## <span data-ttu-id="7f8c4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f8c4-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f8c4-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7f8c4-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="7f8c4-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7f8c4-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="7f8c4-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="7f8c4-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


