---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8b63dbd497edce422fc4cf70182ca8259721d8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572595"
---
# <span data-ttu-id="2e653-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2e653-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="2e653-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e653-102">SYNOPSIS</span></span>
<span data-ttu-id="2e653-103">Tar emot ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="2e653-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e653-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e653-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e653-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e653-105">DESCRIPTION</span></span>
<span data-ttu-id="2e653-106">Cmdleten **Get-AzureRmStreamAnalyticsInput** visar alla indata som har definierats i ett Stream Analytics-jobb eller får information om en viss inmatning.</span><span class="sxs-lookup"><span data-stu-id="2e653-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="2e653-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e653-107">EXAMPLES</span></span>

### <span data-ttu-id="2e653-108">EXEMPEL 1: få information om de uppgifter som definierats för ett jobb</span><span class="sxs-lookup"><span data-stu-id="2e653-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="2e653-109">Det här kommandot returnerar information om alla uppgifter som har definierats för StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2e653-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="2e653-110">EXEMPEL 2: få information om en viss inmatning som definierats för ett jobb</span><span class="sxs-lookup"><span data-stu-id="2e653-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="2e653-111">Det här kommandot returnerar information om den indata som heter EntryStream som definierats i jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2e653-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="2e653-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e653-112">PARAMETERS</span></span>

### <span data-ttu-id="2e653-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e653-113">-DefaultProfile</span></span>
<span data-ttu-id="2e653-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e653-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e653-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="2e653-115">-JobName</span></span>
<span data-ttu-id="2e653-116">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="2e653-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2e653-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e653-117">-Name</span></span>
<span data-ttu-id="2e653-118">Anger namnet på den Azure Stream Analytics-inmatning som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="2e653-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="2e653-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e653-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e653-120">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="2e653-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2e653-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e653-121">CommonParameters</span></span>
<span data-ttu-id="2e653-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e653-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e653-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e653-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e653-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e653-124">INPUTS</span></span>

### <span data-ttu-id="2e653-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2e653-125">System.String</span></span>

## <span data-ttu-id="2e653-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e653-126">OUTPUTS</span></span>

### <span data-ttu-id="2e653-127">Microsoft. Azure. commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="2e653-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="2e653-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e653-128">NOTES</span></span>

## <span data-ttu-id="2e653-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e653-129">RELATED LINKS</span></span>

[<span data-ttu-id="2e653-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2e653-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="2e653-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2e653-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="2e653-132">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2e653-132">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


