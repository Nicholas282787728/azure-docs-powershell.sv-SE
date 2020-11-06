---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: c675a8da84e61b659c593cc1f963dd1b07c7f316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572591"
---
# <span data-ttu-id="cb5ca-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cb5ca-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="cb5ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5ca-103">Hämtar de utdata som definierats i ett angivet ström analys jobb eller utdata.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb5ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb5ca-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb5ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb5ca-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5ca-106">Cmdleten **Get-AzureRmStreamAnalyticsOutput** visar alla utdata som är definierade i ett angivet Stream analys jobb eller får information om ett visst resultat.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="cb5ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb5ca-107">EXAMPLES</span></span>

### <span data-ttu-id="cb5ca-108">EXEMPEL 1: Hämta information om jobb utmatningar</span><span class="sxs-lookup"><span data-stu-id="cb5ca-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="cb5ca-109">Det här kommandot returnerar information om de utdata som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="cb5ca-110">EXEMPEL 2: Hämta information om ett visst utskrifts jobb</span><span class="sxs-lookup"><span data-stu-id="cb5ca-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="cb5ca-111">Det här kommandot returnerar information om den utdata som heter output som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="cb5ca-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb5ca-112">PARAMETERS</span></span>

### <span data-ttu-id="cb5ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5ca-113">-DefaultProfile</span></span>
<span data-ttu-id="cb5ca-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb5ca-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="cb5ca-115">-JobName</span></span>
<span data-ttu-id="cb5ca-116">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="cb5ca-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb5ca-117">-Name</span></span>
<span data-ttu-id="cb5ca-118">Anger namnet på den Azure Stream Analytics-utdata som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="cb5ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb5ca-120">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="cb5ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5ca-121">CommonParameters</span></span>
<span data-ttu-id="cb5ca-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb5ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5ca-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5ca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5ca-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb5ca-124">INPUTS</span></span>

### <span data-ttu-id="cb5ca-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cb5ca-125">System.String</span></span>

## <span data-ttu-id="cb5ca-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb5ca-126">OUTPUTS</span></span>

### <span data-ttu-id="cb5ca-127">Microsoft. Azure. commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="cb5ca-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="cb5ca-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb5ca-128">NOTES</span></span>

## <span data-ttu-id="cb5ca-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb5ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="cb5ca-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cb5ca-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="cb5ca-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cb5ca-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="cb5ca-132">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="cb5ca-132">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


