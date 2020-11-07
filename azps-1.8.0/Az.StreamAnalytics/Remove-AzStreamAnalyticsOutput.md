---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 53bd361d67829fdf30741540f1435032067508e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746167"
---
# <span data-ttu-id="d7fb5-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d7fb5-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d7fb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fb5-103">Tar bort ett resultat från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="d7fb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7fb5-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7fb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fb5-106">Cmdleten **Remove-AzStreamAnalyticsOutput** asynkront tar bort utdata från ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="d7fb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7fb5-107">EXAMPLES</span></span>

### <span data-ttu-id="d7fb5-108">EXEMPEL 1: ta bort ett resultat från ett jobb</span><span class="sxs-lookup"><span data-stu-id="d7fb5-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d7fb5-109">Det här kommandot tar bort utdata från jobbet StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="d7fb5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="d7fb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fb5-111">-DefaultProfile</span></span>
<span data-ttu-id="d7fb5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7fb5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d7fb5-113">-JobName</span></span>
<span data-ttu-id="d7fb5-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d7fb5-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7fb5-115">-Name</span></span>
<span data-ttu-id="d7fb5-116">Anger namnet på Azure Stream Analytics-utdata som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="d7fb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7fb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7fb5-118">Anger namnet på den resurs grupp som Azure Stream Analytics-utdata tillhör.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="d7fb5-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7fb5-119">-Confirm</span></span>
<span data-ttu-id="d7fb5-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7fb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7fb5-121">-WhatIf</span></span>
<span data-ttu-id="d7fb5-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7fb5-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7fb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fb5-124">CommonParameters</span></span>
<span data-ttu-id="d7fb5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fb5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7fb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fb5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7fb5-127">INPUTS</span></span>

### <span data-ttu-id="d7fb5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d7fb5-128">System.String</span></span>

## <span data-ttu-id="d7fb5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7fb5-129">OUTPUTS</span></span>

### <span data-ttu-id="d7fb5-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7fb5-130">System.Boolean</span></span>

## <span data-ttu-id="d7fb5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7fb5-131">NOTES</span></span>

## <span data-ttu-id="d7fb5-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7fb5-132">RELATED LINKS</span></span>

[<span data-ttu-id="d7fb5-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d7fb5-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d7fb5-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d7fb5-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d7fb5-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d7fb5-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


