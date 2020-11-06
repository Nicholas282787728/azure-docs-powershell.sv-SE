---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582427"
---
# <span data-ttu-id="d71c3-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="d71c3-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="d71c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d71c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d71c3-103">Hämtar användnings måtten för en resurs.</span><span class="sxs-lookup"><span data-stu-id="d71c3-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d71c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d71c3-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d71c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d71c3-105">DESCRIPTION</span></span>
<span data-ttu-id="d71c3-106">Cmdleten **Get-AzureRmUsage** hämtar användnings måtten för en viss resurs.</span><span class="sxs-lookup"><span data-stu-id="d71c3-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="d71c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d71c3-107">EXAMPLES</span></span>

### <span data-ttu-id="d71c3-108">Exempel 1: Hämta användnings mått efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="d71c3-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="d71c3-109">Det här kommandot får användnings måtten för den angivna webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="d71c3-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="d71c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d71c3-110">PARAMETERS</span></span>

### <span data-ttu-id="d71c3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d71c3-111">-ApiVersion</span></span>
<span data-ttu-id="d71c3-112">Anger en API-sträng, till exempel 2014-04-01, som godkänns av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="d71c3-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71c3-113">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="d71c3-113">-EndTime</span></span>
<span data-ttu-id="d71c3-114">Anger senaste tid och datum för sökning.</span><span class="sxs-lookup"><span data-stu-id="d71c3-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="d71c3-115">Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d71c3-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71c3-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="d71c3-116">-MetricNames</span></span>
<span data-ttu-id="d71c3-117">Anger en matris med namn på mått.</span><span class="sxs-lookup"><span data-stu-id="d71c3-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71c3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d71c3-118">-ResourceId</span></span>
<span data-ttu-id="d71c3-119">Anger ID för resursen för måttet.</span><span class="sxs-lookup"><span data-stu-id="d71c3-119">Specifies the ID of the resource for the metric.</span></span>

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

### <span data-ttu-id="d71c3-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d71c3-120">-StartTime</span></span>
<span data-ttu-id="d71c3-121">Anger den tid och det datum då du vill söka.</span><span class="sxs-lookup"><span data-stu-id="d71c3-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="d71c3-122">Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d71c3-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d71c3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71c3-123">-DefaultProfile</span></span>
<span data-ttu-id="d71c3-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d71c3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d71c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71c3-125">CommonParameters</span></span>
<span data-ttu-id="d71c3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71c3-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d71c3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71c3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d71c3-128">INPUTS</span></span>

## <span data-ttu-id="d71c3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d71c3-129">OUTPUTS</span></span>

### <span data-ttu-id="d71c3-130">Microsoft. Azure. commands. Insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="d71c3-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="d71c3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d71c3-131">NOTES</span></span>

## <span data-ttu-id="d71c3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d71c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d71c3-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="d71c3-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


