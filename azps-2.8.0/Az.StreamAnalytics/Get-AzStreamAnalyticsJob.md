---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 630f32bc9dd4542ad022ed7b65ec85f6456367b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919114"
---
# <span data-ttu-id="07ce8-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07ce8-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="07ce8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="07ce8-103">Hämtar information om ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="07ce8-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="07ce8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07ce8-104">SYNTAX</span></span>

### <span data-ttu-id="07ce8-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="07ce8-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ce8-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="07ce8-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ce8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07ce8-107">DESCRIPTION</span></span>
<span data-ttu-id="07ce8-108">Cmdleten **Get-AzStreamAnalyticsJob** innehåller alla strömmar som definierats i Azure-prenumerationen eller den angivna resurs gruppen eller hämtar jobb information om ett visst jobb i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="07ce8-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="07ce8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07ce8-109">EXAMPLES</span></span>

### <span data-ttu-id="07ce8-110">EXEMPEL 1: få information om alla jobb i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="07ce8-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="07ce8-111">Det här kommandot returnerar information om alla ström analys jobb i Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="07ce8-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="07ce8-112">EXEMPEL 2: få information om alla jobb i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="07ce8-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="07ce8-113">Det här kommandot returnerar information om alla ström analys jobb i resurs gruppen StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="07ce8-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="07ce8-114">EXEMPEL 3: Hämta information om ett specifikt jobb i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="07ce8-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="07ce8-115">Det här kommandot returnerar information om StreamingJob i resurs gruppen StreamAnalytics-default-West-US.</span><span class="sxs-lookup"><span data-stu-id="07ce8-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="07ce8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07ce8-116">PARAMETERS</span></span>

### <span data-ttu-id="07ce8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ce8-117">-DefaultProfile</span></span>
<span data-ttu-id="07ce8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07ce8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07ce8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="07ce8-119">-Name</span></span>
<span data-ttu-id="07ce8-120">Anger namnet på Azure Stream Analytics-jobbet som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="07ce8-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ce8-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="07ce8-121">-NoExpand</span></span>
<span data-ttu-id="07ce8-122">Anger att cmdleten hämtar Azure Stream Analytics-jobbet men inte returnerar information om dess indata, utdata och transformering.</span><span class="sxs-lookup"><span data-stu-id="07ce8-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="07ce8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ce8-123">-ResourceGroupName</span></span>
<span data-ttu-id="07ce8-124">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="07ce8-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ce8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ce8-125">CommonParameters</span></span>
<span data-ttu-id="07ce8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ce8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ce8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ce8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ce8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07ce8-128">INPUTS</span></span>

### <span data-ttu-id="07ce8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="07ce8-129">System.String</span></span>

### <span data-ttu-id="07ce8-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="07ce8-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="07ce8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07ce8-131">OUTPUTS</span></span>

### <span data-ttu-id="07ce8-132">Microsoft. Azure. commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="07ce8-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="07ce8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07ce8-133">NOTES</span></span>

## <span data-ttu-id="07ce8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07ce8-134">RELATED LINKS</span></span>

[<span data-ttu-id="07ce8-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07ce8-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07ce8-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07ce8-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07ce8-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07ce8-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07ce8-138">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07ce8-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

