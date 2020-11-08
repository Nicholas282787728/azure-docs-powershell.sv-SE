---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261506"
---
# <span data-ttu-id="f5369-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5369-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="f5369-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5369-102">SYNOPSIS</span></span>
<span data-ttu-id="f5369-103">Tar bort en funktion från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="f5369-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="f5369-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5369-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5369-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5369-105">DESCRIPTION</span></span>
<span data-ttu-id="f5369-106">Cmdleten **Remove-AzStreamAnalyticsFunction** tar bort en funktion asynkront från ett Azure Stream Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="f5369-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="f5369-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5369-107">EXAMPLES</span></span>

### <span data-ttu-id="f5369-108">Exempel 1: ta bort en ström analys funktion</span><span class="sxs-lookup"><span data-stu-id="f5369-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="f5369-109">Det här kommandot tar bort den funktion som heter ScoreTweet från jobbet som heter StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="f5369-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="f5369-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5369-110">PARAMETERS</span></span>

### <span data-ttu-id="f5369-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5369-111">-DefaultProfile</span></span>
<span data-ttu-id="f5369-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5369-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5369-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="f5369-113">-JobName</span></span>
<span data-ttu-id="f5369-114">Anger namnet på det Stream analys jobb som en funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="f5369-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="f5369-115">Denna cmdlet tar bort en funktion från det jobb som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f5369-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5369-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5369-116">-Name</span></span>
<span data-ttu-id="f5369-117">Anger namnet på den ström analys funktion som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f5369-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f5369-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5369-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5369-119">Anger namnet på den resurs grupp som en Stream Analytics-funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="f5369-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="f5369-120">Denna cmdlet tar bort en funktion i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f5369-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5369-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5369-121">-Confirm</span></span>
<span data-ttu-id="f5369-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5369-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5369-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5369-123">-WhatIf</span></span>
<span data-ttu-id="f5369-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5369-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5369-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5369-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5369-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5369-126">CommonParameters</span></span>
<span data-ttu-id="f5369-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5369-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5369-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5369-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5369-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5369-129">INPUTS</span></span>

### <span data-ttu-id="f5369-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f5369-130">System.String</span></span>

## <span data-ttu-id="f5369-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5369-131">OUTPUTS</span></span>

### <span data-ttu-id="f5369-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5369-132">System.Boolean</span></span>

## <span data-ttu-id="f5369-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5369-133">NOTES</span></span>

## <span data-ttu-id="f5369-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5369-134">RELATED LINKS</span></span>

[<span data-ttu-id="f5369-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5369-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="f5369-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5369-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="f5369-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5369-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


