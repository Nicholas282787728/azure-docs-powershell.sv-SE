---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: b19a8359f3267d848d475028fe0cee2123949f7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746154"
---
# <span data-ttu-id="6f304-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6f304-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="6f304-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f304-102">SYNOPSIS</span></span>
<span data-ttu-id="6f304-103">Testar anslutnings statusen för en inmatning.</span><span class="sxs-lookup"><span data-stu-id="6f304-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="6f304-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f304-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f304-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f304-105">DESCRIPTION</span></span>
<span data-ttu-id="6f304-106">**Test-AzStreamAnalyticsInput-** cmdleten testar möjligheten att strömma analyser för att ansluta till ett indata.</span><span class="sxs-lookup"><span data-stu-id="6f304-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="6f304-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f304-107">EXAMPLES</span></span>

### <span data-ttu-id="6f304-108">EXEMPEL 1: testa anslutnings statusen för en indataströmmen</span><span class="sxs-lookup"><span data-stu-id="6f304-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="6f304-109">Detta testar anslutnings statusen för EntryStream i StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6f304-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="6f304-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f304-110">PARAMETERS</span></span>

### <span data-ttu-id="6f304-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f304-111">-DefaultProfile</span></span>
<span data-ttu-id="6f304-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f304-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f304-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="6f304-113">-JobName</span></span>
<span data-ttu-id="6f304-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="6f304-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="6f304-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f304-115">-Name</span></span>
<span data-ttu-id="6f304-116">Anger namnet på den Azure Stream Analytics-inmatning som ska testas.</span><span class="sxs-lookup"><span data-stu-id="6f304-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="6f304-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f304-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f304-118">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="6f304-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="6f304-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f304-119">CommonParameters</span></span>
<span data-ttu-id="6f304-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f304-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f304-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f304-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f304-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f304-122">INPUTS</span></span>

### <span data-ttu-id="6f304-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6f304-123">System.String</span></span>

## <span data-ttu-id="6f304-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f304-124">OUTPUTS</span></span>

### <span data-ttu-id="6f304-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f304-125">System.Boolean</span></span>

## <span data-ttu-id="6f304-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f304-126">NOTES</span></span>

## <span data-ttu-id="6f304-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f304-127">RELATED LINKS</span></span>

[<span data-ttu-id="6f304-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6f304-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="6f304-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6f304-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="6f304-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6f304-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


