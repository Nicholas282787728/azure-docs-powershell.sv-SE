---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271687"
---
# <span data-ttu-id="68e2d-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68e2d-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="68e2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="68e2d-103">Tar bort en inmatning från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="68e2d-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="68e2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68e2d-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68e2d-105">DESCRIPTION</span></span>
<span data-ttu-id="68e2d-106">Cmdleten **Remove-AzStreamAnalyticsInput** asynkront tar bort en inmatning från ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="68e2d-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="68e2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68e2d-107">EXAMPLES</span></span>

### <span data-ttu-id="68e2d-108">EXEMPEL 1: ta bort en indataströmmen från ett jobb</span><span class="sxs-lookup"><span data-stu-id="68e2d-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="68e2d-109">Det här kommandot tar bort indatavärdet EventStream från StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="68e2d-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="68e2d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68e2d-110">PARAMETERS</span></span>

### <span data-ttu-id="68e2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e2d-111">-DefaultProfile</span></span>
<span data-ttu-id="68e2d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68e2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68e2d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="68e2d-113">-JobName</span></span>
<span data-ttu-id="68e2d-114">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="68e2d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="68e2d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="68e2d-115">-Name</span></span>
<span data-ttu-id="68e2d-116">Anger namnet på den Azure Stream Analytics-inmatning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="68e2d-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="68e2d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e2d-117">-ResourceGroupName</span></span>
<span data-ttu-id="68e2d-118">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="68e2d-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="68e2d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68e2d-119">-Confirm</span></span>
<span data-ttu-id="68e2d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68e2d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e2d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e2d-121">-WhatIf</span></span>
<span data-ttu-id="68e2d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68e2d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e2d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68e2d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e2d-124">CommonParameters</span></span>
<span data-ttu-id="68e2d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e2d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e2d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e2d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68e2d-127">INPUTS</span></span>

### <span data-ttu-id="68e2d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="68e2d-128">System.String</span></span>

## <span data-ttu-id="68e2d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68e2d-129">OUTPUTS</span></span>

### <span data-ttu-id="68e2d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68e2d-130">System.Boolean</span></span>

## <span data-ttu-id="68e2d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68e2d-131">NOTES</span></span>

## <span data-ttu-id="68e2d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68e2d-132">RELATED LINKS</span></span>

[<span data-ttu-id="68e2d-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68e2d-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="68e2d-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68e2d-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="68e2d-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68e2d-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


