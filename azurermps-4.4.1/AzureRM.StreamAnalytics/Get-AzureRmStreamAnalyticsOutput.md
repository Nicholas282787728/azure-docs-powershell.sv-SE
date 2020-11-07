---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 21c4cf10fc6464b3db5bcb999d1f477c2e73840e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755787"
---
# <span data-ttu-id="73e17-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="73e17-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="73e17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73e17-102">SYNOPSIS</span></span>
<span data-ttu-id="73e17-103">Hämtar de utdata som definierats i ett angivet ström analys jobb eller utdata.</span><span class="sxs-lookup"><span data-stu-id="73e17-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73e17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73e17-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73e17-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73e17-105">DESCRIPTION</span></span>
<span data-ttu-id="73e17-106">Cmdleten **Get-AzureRmStreamAnalyticsOutput** visar alla utdata som är definierade i ett angivet Stream analys jobb eller får information om ett visst resultat.</span><span class="sxs-lookup"><span data-stu-id="73e17-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="73e17-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73e17-107">EXAMPLES</span></span>

### <span data-ttu-id="73e17-108">EXEMPEL 1: Hämta information om jobb utmatningar</span><span class="sxs-lookup"><span data-stu-id="73e17-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="73e17-109">Det här kommandot returnerar information om de utdata som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="73e17-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="73e17-110">EXEMPEL 2: Hämta information om ett visst utskrifts jobb</span><span class="sxs-lookup"><span data-stu-id="73e17-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="73e17-111">Det här kommandot returnerar information om den utdata som heter output som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="73e17-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="73e17-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73e17-112">PARAMETERS</span></span>

### <span data-ttu-id="73e17-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="73e17-113">-JobName</span></span>
<span data-ttu-id="73e17-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="73e17-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="73e17-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="73e17-115">-Name</span></span>
<span data-ttu-id="73e17-116">Anger namnet på den Azure Stream Analytics-utdata som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="73e17-116">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="73e17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e17-117">-ResourceGroupName</span></span>
<span data-ttu-id="73e17-118">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="73e17-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="73e17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e17-119">-DefaultProfile</span></span>
<span data-ttu-id="73e17-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73e17-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e17-121">CommonParameters</span></span>
<span data-ttu-id="73e17-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e17-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e17-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e17-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73e17-124">INPUTS</span></span>

## <span data-ttu-id="73e17-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73e17-125">OUTPUTS</span></span>

### <span data-ttu-id="73e17-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. Models. PSOutput, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="73e17-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="73e17-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73e17-127">NOTES</span></span>

## <span data-ttu-id="73e17-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73e17-128">RELATED LINKS</span></span>

[<span data-ttu-id="73e17-129">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="73e17-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="73e17-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="73e17-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="73e17-131">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="73e17-131">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


