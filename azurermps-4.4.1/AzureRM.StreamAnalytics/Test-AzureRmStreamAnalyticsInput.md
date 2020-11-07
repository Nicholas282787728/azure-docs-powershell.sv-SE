---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756314"
---
# <span data-ttu-id="68db3-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68db3-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="68db3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68db3-102">SYNOPSIS</span></span>
<span data-ttu-id="68db3-103">Testar anslutnings statusen för en inmatning.</span><span class="sxs-lookup"><span data-stu-id="68db3-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68db3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68db3-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68db3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68db3-105">DESCRIPTION</span></span>
<span data-ttu-id="68db3-106">**Test-AzureRmStreamAnalyticsInput-** cmdleten testar möjligheten att strömma analyser för att ansluta till ett indata.</span><span class="sxs-lookup"><span data-stu-id="68db3-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="68db3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68db3-107">EXAMPLES</span></span>

### <span data-ttu-id="68db3-108">EXEMPEL 1: testa anslutnings statusen för en indataströmmen</span><span class="sxs-lookup"><span data-stu-id="68db3-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="68db3-109">Detta testar anslutnings statusen för EntryStream i StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="68db3-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="68db3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68db3-110">PARAMETERS</span></span>

### <span data-ttu-id="68db3-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="68db3-111">-JobName</span></span>
<span data-ttu-id="68db3-112">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="68db3-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="68db3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="68db3-113">-Name</span></span>
<span data-ttu-id="68db3-114">Anger namnet på den Azure Stream Analytics-inmatning som ska testas.</span><span class="sxs-lookup"><span data-stu-id="68db3-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="68db3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68db3-115">-ResourceGroupName</span></span>
<span data-ttu-id="68db3-116">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="68db3-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="68db3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68db3-117">-DefaultProfile</span></span>
<span data-ttu-id="68db3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68db3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68db3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68db3-119">CommonParameters</span></span>
<span data-ttu-id="68db3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68db3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68db3-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68db3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68db3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68db3-122">INPUTS</span></span>

## <span data-ttu-id="68db3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68db3-123">OUTPUTS</span></span>

### <span data-ttu-id="68db3-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="68db3-124">System.Object</span></span>

## <span data-ttu-id="68db3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68db3-125">NOTES</span></span>

## <span data-ttu-id="68db3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68db3-126">RELATED LINKS</span></span>

[<span data-ttu-id="68db3-127">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68db3-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="68db3-128">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68db3-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="68db3-129">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68db3-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


