---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 9e228c2520402f1b8395c6ca4d90909905f6cb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755365"
---
# <span data-ttu-id="1c3a3-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1c3a3-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="1c3a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3a3-103">Tar bort en inmatning från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c3a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c3a3-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c3a3-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3a3-106">Cmdleten **Remove-AzureRmStreamAnalyticsInput** asynkront tar bort en inmatning från ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="1c3a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c3a3-107">EXAMPLES</span></span>

### <span data-ttu-id="1c3a3-108">EXEMPEL 1: ta bort en indataströmmen från ett jobb</span><span class="sxs-lookup"><span data-stu-id="1c3a3-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="1c3a3-109">Det här kommandot tar bort indatavärdet EventStream från StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="1c3a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c3a3-110">PARAMETERS</span></span>

### <span data-ttu-id="1c3a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3a3-111">-DefaultProfile</span></span>
<span data-ttu-id="1c3a3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c3a3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1c3a3-113">-JobName</span></span>
<span data-ttu-id="1c3a3-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="1c3a3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c3a3-115">-Name</span></span>
<span data-ttu-id="1c3a3-116">Anger namnet på den Azure Stream Analytics-inmatning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="1c3a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c3a3-118">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="1c3a3-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c3a3-119">-Confirm</span></span>
<span data-ttu-id="1c3a3-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3a3-121">-WhatIf</span></span>
<span data-ttu-id="1c3a3-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3a3-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3a3-124">CommonParameters</span></span>
<span data-ttu-id="1c3a3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3a3-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3a3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c3a3-127">INPUTS</span></span>

### <span data-ttu-id="1c3a3-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c3a3-128">None</span></span>
<span data-ttu-id="1c3a3-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1c3a3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c3a3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c3a3-130">OUTPUTS</span></span>

### <span data-ttu-id="1c3a3-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="1c3a3-131">System.Object</span></span>

## <span data-ttu-id="1c3a3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c3a3-132">NOTES</span></span>

## <span data-ttu-id="1c3a3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c3a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="1c3a3-134">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1c3a3-134">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="1c3a3-135">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1c3a3-135">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="1c3a3-136">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1c3a3-136">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


