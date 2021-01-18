---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525287"
---
# <span data-ttu-id="a5d62-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5d62-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="a5d62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5d62-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d62-103">Tar bort ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="a5d62-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="a5d62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5d62-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d62-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5d62-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d62-106">Cmdleten **Remove-AzStreamAnalyticsJob** asynkron tar bort ett specifikt ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d62-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a5d62-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5d62-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d62-108">EXEMPEL 1: ta bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="a5d62-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="a5d62-109">Det här kommandot tar bort jobbets StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a5d62-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="a5d62-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5d62-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d62-111">-DefaultProfile</span></span>
<span data-ttu-id="a5d62-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d62-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d62-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5d62-113">-Name</span></span>
<span data-ttu-id="a5d62-114">Anger namnet på Azure Stream Analytics-jobbet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a5d62-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="a5d62-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d62-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5d62-116">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="a5d62-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="a5d62-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5d62-117">-Confirm</span></span>
<span data-ttu-id="a5d62-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5d62-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d62-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d62-119">-WhatIf</span></span>
<span data-ttu-id="a5d62-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5d62-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d62-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5d62-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d62-122">CommonParameters</span></span>
<span data-ttu-id="a5d62-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d62-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d62-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d62-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5d62-125">INPUTS</span></span>

### <span data-ttu-id="a5d62-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d62-126">System.String</span></span>

## <span data-ttu-id="a5d62-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5d62-127">OUTPUTS</span></span>

### <span data-ttu-id="a5d62-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5d62-128">System.Boolean</span></span>

## <span data-ttu-id="a5d62-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5d62-129">NOTES</span></span>

## <span data-ttu-id="a5d62-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5d62-130">RELATED LINKS</span></span>

[<span data-ttu-id="a5d62-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5d62-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a5d62-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5d62-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a5d62-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5d62-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a5d62-134">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a5d62-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


