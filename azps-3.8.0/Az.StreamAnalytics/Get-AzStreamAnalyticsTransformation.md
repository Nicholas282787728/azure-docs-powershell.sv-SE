---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928062"
---
# <span data-ttu-id="b44fd-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b44fd-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="b44fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b44fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b44fd-103">Hämtar information om ett flödes omformnings jobb.</span><span class="sxs-lookup"><span data-stu-id="b44fd-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="b44fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b44fd-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b44fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b44fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b44fd-106">Cmdleten **Get-AzStreamAnalyticsTransformation** hämtar information om en omvandling som är definierad i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="b44fd-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="b44fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b44fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b44fd-108">EXEMPEL 1: få information om en Stream Analytics-transformering</span><span class="sxs-lookup"><span data-stu-id="b44fd-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="b44fd-109">Det här kommandot returnerar information om omvandlingen som heter StreamingJob på jobbet som heter StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b44fd-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="b44fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b44fd-110">PARAMETERS</span></span>

### <span data-ttu-id="b44fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44fd-111">-DefaultProfile</span></span>
<span data-ttu-id="b44fd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b44fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b44fd-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b44fd-113">-JobName</span></span>
<span data-ttu-id="b44fd-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-transformeringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b44fd-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="b44fd-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b44fd-115">-Name</span></span>
<span data-ttu-id="b44fd-116">Anger namnet på Azure Stream Analytics-transformeringen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="b44fd-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="b44fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="b44fd-118">Anger namnet på den resurs grupp som Azure Stream Analytics-transformeringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b44fd-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="b44fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44fd-119">CommonParameters</span></span>
<span data-ttu-id="b44fd-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b44fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44fd-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b44fd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44fd-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b44fd-122">INPUTS</span></span>

### <span data-ttu-id="b44fd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b44fd-123">System.String</span></span>

## <span data-ttu-id="b44fd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b44fd-124">OUTPUTS</span></span>

### <span data-ttu-id="b44fd-125">Microsoft. Azure. commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="b44fd-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="b44fd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b44fd-126">NOTES</span></span>

## <span data-ttu-id="b44fd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b44fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="b44fd-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b44fd-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)

