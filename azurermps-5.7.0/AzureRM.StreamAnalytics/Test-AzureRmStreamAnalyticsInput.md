---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 34e1c2813292801d29a93a6914abf11b2725ec14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574128"
---
# <span data-ttu-id="82d92-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="82d92-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="82d92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82d92-102">SYNOPSIS</span></span>
<span data-ttu-id="82d92-103">Testar anslutnings statusen för en inmatning.</span><span class="sxs-lookup"><span data-stu-id="82d92-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82d92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82d92-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d92-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82d92-105">DESCRIPTION</span></span>
<span data-ttu-id="82d92-106">**Test-AzureRmStreamAnalyticsInput-** cmdleten testar möjligheten att strömma analyser för att ansluta till ett indata.</span><span class="sxs-lookup"><span data-stu-id="82d92-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="82d92-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82d92-107">EXAMPLES</span></span>

### <span data-ttu-id="82d92-108">EXEMPEL 1: testa anslutnings statusen för en indataströmmen</span><span class="sxs-lookup"><span data-stu-id="82d92-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="82d92-109">Detta testar anslutnings statusen för EntryStream i StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="82d92-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="82d92-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82d92-110">PARAMETERS</span></span>

### <span data-ttu-id="82d92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d92-111">-DefaultProfile</span></span>
<span data-ttu-id="82d92-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82d92-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82d92-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="82d92-113">-JobName</span></span>
<span data-ttu-id="82d92-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="82d92-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="82d92-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="82d92-115">-Name</span></span>
<span data-ttu-id="82d92-116">Anger namnet på den Azure Stream Analytics-inmatning som ska testas.</span><span class="sxs-lookup"><span data-stu-id="82d92-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="82d92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d92-117">-ResourceGroupName</span></span>
<span data-ttu-id="82d92-118">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="82d92-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="82d92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d92-119">CommonParameters</span></span>
<span data-ttu-id="82d92-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d92-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82d92-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d92-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82d92-122">INPUTS</span></span>

### <span data-ttu-id="82d92-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="82d92-123">None</span></span>
<span data-ttu-id="82d92-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="82d92-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82d92-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82d92-125">OUTPUTS</span></span>

### <span data-ttu-id="82d92-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="82d92-126">System.Object</span></span>

## <span data-ttu-id="82d92-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82d92-127">NOTES</span></span>

## <span data-ttu-id="82d92-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82d92-128">RELATED LINKS</span></span>

[<span data-ttu-id="82d92-129">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="82d92-129">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="82d92-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="82d92-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="82d92-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="82d92-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


