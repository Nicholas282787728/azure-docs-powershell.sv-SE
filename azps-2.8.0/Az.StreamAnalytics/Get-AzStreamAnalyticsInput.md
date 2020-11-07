---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: cd6e7e4bf9ba9a99b9b3a9a5f58acb9578236037
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920766"
---
# <span data-ttu-id="af6d0-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="af6d0-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="af6d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="af6d0-103">Tar emot ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="af6d0-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="af6d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af6d0-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af6d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="af6d0-106">Cmdleten **Get-AzStreamAnalyticsInput** visar alla indata som har definierats i ett Stream Analytics-jobb eller får information om en viss inmatning.</span><span class="sxs-lookup"><span data-stu-id="af6d0-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="af6d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af6d0-107">EXAMPLES</span></span>

### <span data-ttu-id="af6d0-108">EXEMPEL 1: få information om de uppgifter som definierats för ett jobb</span><span class="sxs-lookup"><span data-stu-id="af6d0-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="af6d0-109">Det här kommandot returnerar information om alla uppgifter som har definierats för StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="af6d0-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="af6d0-110">EXEMPEL 2: få information om en viss inmatning som definierats för ett jobb</span><span class="sxs-lookup"><span data-stu-id="af6d0-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="af6d0-111">Det här kommandot returnerar information om den indata som heter EntryStream som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="af6d0-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="af6d0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af6d0-112">PARAMETERS</span></span>

### <span data-ttu-id="af6d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6d0-113">-DefaultProfile</span></span>
<span data-ttu-id="af6d0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af6d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af6d0-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="af6d0-115">-JobName</span></span>
<span data-ttu-id="af6d0-116">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="af6d0-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="af6d0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="af6d0-117">-Name</span></span>
<span data-ttu-id="af6d0-118">Anger namnet på den Azure Stream Analytics-inmatning som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="af6d0-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af6d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af6d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="af6d0-120">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="af6d0-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="af6d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6d0-121">CommonParameters</span></span>
<span data-ttu-id="af6d0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af6d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6d0-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af6d0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6d0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af6d0-124">INPUTS</span></span>

### <span data-ttu-id="af6d0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="af6d0-125">System.String</span></span>

## <span data-ttu-id="af6d0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af6d0-126">OUTPUTS</span></span>

### <span data-ttu-id="af6d0-127">Microsoft. Azure. commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="af6d0-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="af6d0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af6d0-128">NOTES</span></span>

## <span data-ttu-id="af6d0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af6d0-129">RELATED LINKS</span></span>

[<span data-ttu-id="af6d0-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="af6d0-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="af6d0-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="af6d0-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="af6d0-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="af6d0-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


