---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574471"
---
# <span data-ttu-id="21a2d-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="21a2d-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="21a2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="21a2d-103">Hämtar information om den strömmande enhets kvoten för en region.</span><span class="sxs-lookup"><span data-stu-id="21a2d-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21a2d-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21a2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="21a2d-106">Cmdleten **Get-AzureRmStreamAnalyticsQuota** hämtar information om den strömmande enhets kvoten för en region.</span><span class="sxs-lookup"><span data-stu-id="21a2d-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="21a2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21a2d-107">EXAMPLES</span></span>

### <span data-ttu-id="21a2d-108">EXEMPEL 1: Hämta information om enhets kvoten för direkt uppspelning av en region</span><span class="sxs-lookup"><span data-stu-id="21a2d-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="21a2d-109">Det här kommandot returnerar information om enhets kvot och användning för strömmande enheter i västra USA.</span><span class="sxs-lookup"><span data-stu-id="21a2d-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="21a2d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21a2d-110">PARAMETERS</span></span>

### <span data-ttu-id="21a2d-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="21a2d-111">-Location</span></span>
<span data-ttu-id="21a2d-112">Anger namnet på ett Azure-område eller en data Center plats där du vill få kvot information för strömningen.</span><span class="sxs-lookup"><span data-stu-id="21a2d-112">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="21a2d-113">Se https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services en lista över Azure-regioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="21a2d-113">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="21a2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a2d-114">-DefaultProfile</span></span>
<span data-ttu-id="21a2d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21a2d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a2d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a2d-116">CommonParameters</span></span>
<span data-ttu-id="21a2d-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a2d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a2d-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a2d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a2d-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21a2d-119">INPUTS</span></span>

## <span data-ttu-id="21a2d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21a2d-120">OUTPUTS</span></span>

### <span data-ttu-id="21a2d-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. Models. PSQuota, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. commands. StreamAnalytics. Models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="21a2d-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="21a2d-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21a2d-122">NOTES</span></span>

## <span data-ttu-id="21a2d-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21a2d-123">RELATED LINKS</span></span>

[<span data-ttu-id="21a2d-124">Azure Stream Analytics-cmdletar</span><span class="sxs-lookup"><span data-stu-id="21a2d-124">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)

