---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: d76b1139955490189aeb9c2269cc4e9ede8197be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579235"
---
# <span data-ttu-id="0c985-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0c985-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="0c985-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c985-102">SYNOPSIS</span></span>
<span data-ttu-id="0c985-103">Tar bort en funktion från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="0c985-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c985-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c985-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c985-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c985-105">DESCRIPTION</span></span>
<span data-ttu-id="0c985-106">Cmdleten **Remove-AzureRmStreamAnalyticsFunction** tar bort en funktion asynkront från ett Azure Stream Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="0c985-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="0c985-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c985-107">EXAMPLES</span></span>

### <span data-ttu-id="0c985-108">Exempel 1: ta bort en ström analys funktion</span><span class="sxs-lookup"><span data-stu-id="0c985-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="0c985-109">Det här kommandot tar bort den funktion som heter ScoreTweet från jobbet som heter StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="0c985-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="0c985-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c985-110">PARAMETERS</span></span>

### <span data-ttu-id="0c985-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c985-111">-DefaultProfile</span></span>
<span data-ttu-id="0c985-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c985-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c985-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0c985-113">-JobName</span></span>
<span data-ttu-id="0c985-114">Anger namnet på det Stream analys jobb som en funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="0c985-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="0c985-115">Denna cmdlet tar bort en funktion från det jobb som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0c985-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c985-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c985-116">-Name</span></span>
<span data-ttu-id="0c985-117">Anger namnet på den ström analys funktion som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0c985-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c985-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c985-118">-ResourceGroupName</span></span>
<span data-ttu-id="0c985-119">Anger namnet på den resurs grupp som en Stream Analytics-funktion tillhör.</span><span class="sxs-lookup"><span data-stu-id="0c985-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="0c985-120">Denna cmdlet tar bort en funktion i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0c985-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c985-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c985-121">-Confirm</span></span>
<span data-ttu-id="0c985-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c985-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c985-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c985-123">-WhatIf</span></span>
<span data-ttu-id="0c985-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c985-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c985-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c985-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c985-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c985-126">CommonParameters</span></span>
<span data-ttu-id="0c985-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c985-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c985-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c985-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c985-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c985-129">INPUTS</span></span>

### <span data-ttu-id="0c985-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="0c985-130">None</span></span>
<span data-ttu-id="0c985-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0c985-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c985-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c985-132">OUTPUTS</span></span>

### <span data-ttu-id="0c985-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="0c985-133">System.Object</span></span>

## <span data-ttu-id="0c985-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c985-134">NOTES</span></span>

## <span data-ttu-id="0c985-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c985-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c985-136">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0c985-136">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="0c985-137">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0c985-137">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="0c985-138">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="0c985-138">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


