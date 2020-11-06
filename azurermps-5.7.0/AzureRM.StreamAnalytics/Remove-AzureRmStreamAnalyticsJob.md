---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575424"
---
# <span data-ttu-id="3311b-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3311b-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="3311b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3311b-102">SYNOPSIS</span></span>
<span data-ttu-id="3311b-103">Tar bort ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="3311b-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3311b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3311b-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3311b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3311b-105">DESCRIPTION</span></span>
<span data-ttu-id="3311b-106">Cmdleten **Remove-AzureRmStreamAnalyticsJob** asynkron tar bort ett specifikt ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="3311b-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="3311b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3311b-107">EXAMPLES</span></span>

### <span data-ttu-id="3311b-108">EXEMPEL 1: ta bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="3311b-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="3311b-109">Det här kommandot tar bort jobbets StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3311b-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="3311b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3311b-110">PARAMETERS</span></span>

### <span data-ttu-id="3311b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3311b-111">-DefaultProfile</span></span>
<span data-ttu-id="3311b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3311b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3311b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3311b-113">-Name</span></span>
<span data-ttu-id="3311b-114">Anger namnet på Azure Stream Analytics-jobbet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3311b-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3311b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3311b-115">-ResourceGroupName</span></span>
<span data-ttu-id="3311b-116">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="3311b-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3311b-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3311b-117">-Confirm</span></span>
<span data-ttu-id="3311b-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3311b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3311b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3311b-119">-WhatIf</span></span>
<span data-ttu-id="3311b-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3311b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3311b-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3311b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3311b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3311b-122">CommonParameters</span></span>
<span data-ttu-id="3311b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3311b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3311b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3311b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3311b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3311b-125">INPUTS</span></span>

### <span data-ttu-id="3311b-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="3311b-126">None</span></span>
<span data-ttu-id="3311b-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3311b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3311b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3311b-128">OUTPUTS</span></span>

### <span data-ttu-id="3311b-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="3311b-129">System.Object</span></span>

## <span data-ttu-id="3311b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3311b-130">NOTES</span></span>

## <span data-ttu-id="3311b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3311b-131">RELATED LINKS</span></span>

[<span data-ttu-id="3311b-132">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3311b-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3311b-133">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3311b-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3311b-134">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3311b-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3311b-135">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3311b-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


