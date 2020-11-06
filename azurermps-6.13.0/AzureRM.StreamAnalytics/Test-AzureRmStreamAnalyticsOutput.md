---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f8bd4feab9bdcf99daf713d3a584a574f699a8b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573855"
---
# <span data-ttu-id="ffee3-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ffee3-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="ffee3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ffee3-102">SYNOPSIS</span></span>
<span data-ttu-id="ffee3-103">Testar anslutnings statusen för ett resultat.</span><span class="sxs-lookup"><span data-stu-id="ffee3-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffee3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ffee3-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffee3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ffee3-105">DESCRIPTION</span></span>
<span data-ttu-id="ffee3-106">**Testet AzureRmStreamAnalyticsOutput-** cmdleten testar möjligheten att strömma analyser för att ansluta till ett resultat.</span><span class="sxs-lookup"><span data-stu-id="ffee3-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="ffee3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ffee3-107">EXAMPLES</span></span>

### <span data-ttu-id="ffee3-108">EXEMPEL 1: testa anslutnings statusen för ett utdata</span><span class="sxs-lookup"><span data-stu-id="ffee3-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="ffee3-109">Detta testar anslutnings statusen för utdata i StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ffee3-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="ffee3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ffee3-110">PARAMETERS</span></span>

### <span data-ttu-id="ffee3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffee3-111">-DefaultProfile</span></span>
<span data-ttu-id="ffee3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ffee3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffee3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ffee3-113">-JobName</span></span>
<span data-ttu-id="ffee3-114">Anger namnet på Azure Stream Analytics-jobbet som den önskade Azure Stream-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="ffee3-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="ffee3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ffee3-115">-Name</span></span>
<span data-ttu-id="ffee3-116">Anger namnet på den Azure Stream Analytics-utdata som ska testas.</span><span class="sxs-lookup"><span data-stu-id="ffee3-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="ffee3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffee3-117">-ResourceGroupName</span></span>
<span data-ttu-id="ffee3-118">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="ffee3-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="ffee3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffee3-119">CommonParameters</span></span>
<span data-ttu-id="ffee3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffee3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffee3-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffee3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffee3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ffee3-122">INPUTS</span></span>

### <span data-ttu-id="ffee3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ffee3-123">System.String</span></span>

## <span data-ttu-id="ffee3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ffee3-124">OUTPUTS</span></span>

### <span data-ttu-id="ffee3-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ffee3-125">System.Boolean</span></span>

## <span data-ttu-id="ffee3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ffee3-126">NOTES</span></span>

## <span data-ttu-id="ffee3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ffee3-127">RELATED LINKS</span></span>

[<span data-ttu-id="ffee3-128">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ffee3-128">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="ffee3-129">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ffee3-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="ffee3-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ffee3-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


