---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272532"
---
# <span data-ttu-id="001b9-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="001b9-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="001b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="001b9-102">SYNOPSIS</span></span>
<span data-ttu-id="001b9-103">Testar anslutnings statusen för ett resultat.</span><span class="sxs-lookup"><span data-stu-id="001b9-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="001b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="001b9-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="001b9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="001b9-105">DESCRIPTION</span></span>
<span data-ttu-id="001b9-106">**Testet AzStreamAnalyticsOutput-** cmdleten testar möjligheten att strömma analyser för att ansluta till ett resultat.</span><span class="sxs-lookup"><span data-stu-id="001b9-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="001b9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="001b9-107">EXAMPLES</span></span>

### <span data-ttu-id="001b9-108">Exempel 1: testa anslutnings statusen för ett utdata</span><span class="sxs-lookup"><span data-stu-id="001b9-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="001b9-109">Detta testar anslutnings statusen för utdata i StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="001b9-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="001b9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="001b9-110">PARAMETERS</span></span>

### <span data-ttu-id="001b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001b9-111">-DefaultProfile</span></span>
<span data-ttu-id="001b9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="001b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="001b9-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="001b9-113">-JobName</span></span>
<span data-ttu-id="001b9-114">Anger namnet på Azure Stream Analytics-jobbet som den önskade Azure Stream-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="001b9-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="001b9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="001b9-115">-Name</span></span>
<span data-ttu-id="001b9-116">Anger namnet på den Azure Stream Analytics-utdata som ska testas.</span><span class="sxs-lookup"><span data-stu-id="001b9-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="001b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="001b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="001b9-118">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="001b9-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="001b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001b9-119">CommonParameters</span></span>
<span data-ttu-id="001b9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="001b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001b9-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="001b9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001b9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="001b9-122">INPUTS</span></span>

### <span data-ttu-id="001b9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="001b9-123">System.String</span></span>

## <span data-ttu-id="001b9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="001b9-124">OUTPUTS</span></span>

### <span data-ttu-id="001b9-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="001b9-125">System.Boolean</span></span>

## <span data-ttu-id="001b9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="001b9-126">NOTES</span></span>

## <span data-ttu-id="001b9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="001b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="001b9-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="001b9-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="001b9-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="001b9-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="001b9-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="001b9-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

