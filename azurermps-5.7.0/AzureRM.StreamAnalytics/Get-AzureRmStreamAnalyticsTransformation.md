---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756056"
---
# <span data-ttu-id="10eb2-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="10eb2-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="10eb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="10eb2-103">Hämtar information om ett flödes omformnings jobb.</span><span class="sxs-lookup"><span data-stu-id="10eb2-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10eb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10eb2-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10eb2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10eb2-105">DESCRIPTION</span></span>
<span data-ttu-id="10eb2-106">Cmdleten **Get-AzureRmStreamAnalyticsTransformation** hämtar information om en omvandling som är definierad i ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="10eb2-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="10eb2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10eb2-107">EXAMPLES</span></span>

### <span data-ttu-id="10eb2-108">EXEMPEL 1: få information om en Stream Analytics-transformering</span><span class="sxs-lookup"><span data-stu-id="10eb2-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="10eb2-109">Det här kommandot returnerar information om omvandlingen som heter StreamingJob på jobbet som heter StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="10eb2-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="10eb2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10eb2-110">PARAMETERS</span></span>

### <span data-ttu-id="10eb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10eb2-111">-DefaultProfile</span></span>
<span data-ttu-id="10eb2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10eb2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10eb2-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="10eb2-113">-JobName</span></span>
<span data-ttu-id="10eb2-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-transformeringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="10eb2-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eb2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="10eb2-115">-Name</span></span>
<span data-ttu-id="10eb2-116">Anger namnet på Azure Stream Analytics-transformeringen som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="10eb2-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eb2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10eb2-117">-ResourceGroupName</span></span>
<span data-ttu-id="10eb2-118">Anger namnet på den resurs grupp som Azure Stream Analytics-transformeringen tillhör.</span><span class="sxs-lookup"><span data-stu-id="10eb2-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eb2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10eb2-119">CommonParameters</span></span>
<span data-ttu-id="10eb2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10eb2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10eb2-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10eb2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10eb2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10eb2-122">INPUTS</span></span>

### <span data-ttu-id="10eb2-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="10eb2-123">None</span></span>
<span data-ttu-id="10eb2-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="10eb2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10eb2-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10eb2-125">OUTPUTS</span></span>

### <span data-ttu-id="10eb2-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="10eb2-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="10eb2-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10eb2-127">NOTES</span></span>

## <span data-ttu-id="10eb2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10eb2-128">RELATED LINKS</span></span>

[<span data-ttu-id="10eb2-129">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="10eb2-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


