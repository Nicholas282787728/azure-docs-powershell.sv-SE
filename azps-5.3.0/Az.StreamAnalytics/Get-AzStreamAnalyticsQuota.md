---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424691"
---
# <span data-ttu-id="89de5-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="89de5-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="89de5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89de5-102">SYNOPSIS</span></span>
<span data-ttu-id="89de5-103">Hämtar information om den strömmande enhets kvoten för en region.</span><span class="sxs-lookup"><span data-stu-id="89de5-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="89de5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89de5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89de5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89de5-105">DESCRIPTION</span></span>
<span data-ttu-id="89de5-106">Cmdleten **Get-AzStreamAnalyticsQuota** hämtar information om den strömmande enhets kvoten för en region.</span><span class="sxs-lookup"><span data-stu-id="89de5-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="89de5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89de5-107">EXAMPLES</span></span>

### <span data-ttu-id="89de5-108">EXEMPEL 1: Hämta information om enhets kvoten för direkt uppspelning av en region</span><span class="sxs-lookup"><span data-stu-id="89de5-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="89de5-109">Det här kommandot returnerar information om enhets kvot och användning för strömmande enheter i västra USA.</span><span class="sxs-lookup"><span data-stu-id="89de5-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="89de5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89de5-110">PARAMETERS</span></span>

### <span data-ttu-id="89de5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89de5-111">-DefaultProfile</span></span>
<span data-ttu-id="89de5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89de5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89de5-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="89de5-113">-Location</span></span>
<span data-ttu-id="89de5-114">Anger namnet på ett Azure-område eller en data Center plats där du vill få kvot information för strömningen.</span><span class="sxs-lookup"><span data-stu-id="89de5-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="89de5-115">Se http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services en lista över Azure-regioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="89de5-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="89de5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89de5-116">CommonParameters</span></span>
<span data-ttu-id="89de5-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89de5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89de5-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89de5-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89de5-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89de5-119">INPUTS</span></span>

### <span data-ttu-id="89de5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="89de5-120">System.String</span></span>

## <span data-ttu-id="89de5-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89de5-121">OUTPUTS</span></span>

### <span data-ttu-id="89de5-122">Microsoft. Azure. commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="89de5-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="89de5-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89de5-123">NOTES</span></span>

## <span data-ttu-id="89de5-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89de5-124">RELATED LINKS</span></span>

[<span data-ttu-id="89de5-125">Azure Stream Analytics-cmdletar</span><span class="sxs-lookup"><span data-stu-id="89de5-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


