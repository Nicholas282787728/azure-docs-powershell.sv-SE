---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: d83038d521e562ec835324dd50740ec929fb5893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572587"
---
# <span data-ttu-id="f8c66-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f8c66-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="f8c66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8c66-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c66-103">Hämtar information om ett flödes omformnings jobb.</span><span class="sxs-lookup"><span data-stu-id="f8c66-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8c66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8c66-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8c66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8c66-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c66-106">Cmdleten **Get-AzureRmStreamAnalyticsTransformation** hämtar information om en omvandling som är definierad i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="f8c66-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="f8c66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8c66-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c66-108">EXEMPEL 1: få information om en Stream Analytics-transformering</span><span class="sxs-lookup"><span data-stu-id="f8c66-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="f8c66-109">Det här kommandot returnerar information om omvandlingen som heter StreamingJob på jobbet som heter StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="f8c66-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="f8c66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8c66-110">PARAMETERS</span></span>

### <span data-ttu-id="f8c66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c66-111">-DefaultProfile</span></span>
<span data-ttu-id="f8c66-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c66-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f8c66-113">-JobName</span></span>
<span data-ttu-id="f8c66-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-transformeringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="f8c66-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="f8c66-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8c66-115">-Name</span></span>
<span data-ttu-id="f8c66-116">Anger namnet på Azure Stream Analytics-transformeringen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f8c66-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="f8c66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c66-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8c66-118">Anger namnet på den resurs grupp som Azure Stream Analytics-transformeringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="f8c66-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="f8c66-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c66-119">CommonParameters</span></span>
<span data-ttu-id="f8c66-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c66-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c66-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8c66-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c66-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8c66-122">INPUTS</span></span>

### <span data-ttu-id="f8c66-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f8c66-123">System.String</span></span>

## <span data-ttu-id="f8c66-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8c66-124">OUTPUTS</span></span>

### <span data-ttu-id="f8c66-125">Microsoft. Azure. commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="f8c66-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="f8c66-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8c66-126">NOTES</span></span>

## <span data-ttu-id="f8c66-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8c66-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8c66-128">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f8c66-128">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


