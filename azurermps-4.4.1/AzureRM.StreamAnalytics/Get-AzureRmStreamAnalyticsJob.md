---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577368"
---
# <span data-ttu-id="e0d5b-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0d5b-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="e0d5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d5b-103">Hämtar information om ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0d5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0d5b-104">SYNTAX</span></span>

### <span data-ttu-id="e0d5b-105">För Stream Analytics-objekt i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e0d5b-105">For stream analytics objects in the given resource group</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0d5b-106">För Stream Analytics-objekt i den angivna prenumerationen</span><span class="sxs-lookup"><span data-stu-id="e0d5b-106">For stream analytics objects in the given subscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0d5b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0d5b-107">DESCRIPTION</span></span>
<span data-ttu-id="e0d5b-108">Cmdleten **Get-AzureRmStreamAnalyticsJob** innehåller alla strömmar som definierats i Azure-prenumerationen eller den angivna resurs gruppen eller hämtar jobb information om ett visst jobb i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="e0d5b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0d5b-109">EXAMPLES</span></span>

### <span data-ttu-id="e0d5b-110">EXEMPEL 1: få information om alla jobb i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e0d5b-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="e0d5b-111">Det här kommandot returnerar information om alla ström analys jobb i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="e0d5b-112">EXEMPEL 2: få information om alla jobb i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e0d5b-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="e0d5b-113">Det här kommandot returnerar information om alla ström analys jobb i resurs gruppen StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="e0d5b-114">EXEMPEL 3: Hämta information om ett specifikt jobb i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e0d5b-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e0d5b-115">Det här kommandot returnerar information om StreamingJob i resurs gruppen StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="e0d5b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0d5b-116">PARAMETERS</span></span>

### <span data-ttu-id="e0d5b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0d5b-117">-Name</span></span>
<span data-ttu-id="e0d5b-118">Anger namnet på Azure Stream Analytics-jobbet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-118">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d5b-119">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="e0d5b-119">-NoExpand</span></span>
<span data-ttu-id="e0d5b-120">Anger att cmdleten hämtar Azure Stream Analytics-jobbet men inte returnerar information om dess indata, utdata och transformering.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-120">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d5b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d5b-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0d5b-122">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-122">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0d5b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d5b-123">-DefaultProfile</span></span>
<span data-ttu-id="e0d5b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0d5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d5b-125">CommonParameters</span></span>
<span data-ttu-id="e0d5b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d5b-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d5b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d5b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0d5b-128">INPUTS</span></span>

## <span data-ttu-id="e0d5b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0d5b-129">OUTPUTS</span></span>

### <span data-ttu-id="e0d5b-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. StreamAnalytics. Models. PSJob, Microsoft. Azure. commands. StreamAnalytics]] Microsoft. Azure. commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="e0d5b-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="e0d5b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0d5b-131">NOTES</span></span>

## <span data-ttu-id="e0d5b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0d5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0d5b-133">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0d5b-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e0d5b-134">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0d5b-134">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e0d5b-135">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0d5b-135">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e0d5b-136">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e0d5b-136">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


