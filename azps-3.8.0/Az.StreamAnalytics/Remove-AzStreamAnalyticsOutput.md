---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926121"
---
# <span data-ttu-id="05a7c-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="05a7c-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="05a7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="05a7c-103">Tar bort ett resultat från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="05a7c-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="05a7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05a7c-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="05a7c-106">Cmdleten **Remove-AzStreamAnalyticsOutput** asynkront tar bort utdata från ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="05a7c-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="05a7c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="05a7c-108">EXEMPEL 1: ta bort ett resultat från ett jobb</span><span class="sxs-lookup"><span data-stu-id="05a7c-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="05a7c-109">Det här kommandot tar bort utdata från jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="05a7c-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="05a7c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05a7c-110">PARAMETERS</span></span>

### <span data-ttu-id="05a7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a7c-111">-DefaultProfile</span></span>
<span data-ttu-id="05a7c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05a7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a7c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="05a7c-113">-JobName</span></span>
<span data-ttu-id="05a7c-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="05a7c-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="05a7c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="05a7c-115">-Name</span></span>
<span data-ttu-id="05a7c-116">Anger namnet på Azure Stream Analytics-utdata som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="05a7c-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="05a7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="05a7c-118">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="05a7c-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="05a7c-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05a7c-119">-Confirm</span></span>
<span data-ttu-id="05a7c-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05a7c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a7c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a7c-121">-WhatIf</span></span>
<span data-ttu-id="05a7c-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05a7c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a7c-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05a7c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a7c-124">CommonParameters</span></span>
<span data-ttu-id="05a7c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a7c-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a7c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a7c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05a7c-127">INPUTS</span></span>

### <span data-ttu-id="05a7c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="05a7c-128">System.String</span></span>

## <span data-ttu-id="05a7c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05a7c-129">OUTPUTS</span></span>

### <span data-ttu-id="05a7c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05a7c-130">System.Boolean</span></span>

## <span data-ttu-id="05a7c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05a7c-131">NOTES</span></span>

## <span data-ttu-id="05a7c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05a7c-132">RELATED LINKS</span></span>

[<span data-ttu-id="05a7c-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="05a7c-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="05a7c-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="05a7c-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="05a7c-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="05a7c-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)

