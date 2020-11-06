---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583727"
---
# <span data-ttu-id="c2917-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="c2917-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="c2917-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2917-102">SYNOPSIS</span></span>
<span data-ttu-id="c2917-103">Tar bort en inmatning från ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="c2917-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2917-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2917-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2917-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2917-105">DESCRIPTION</span></span>
<span data-ttu-id="c2917-106">Cmdleten **Remove-AzureRmStreamAnalyticsInput** asynkront tar bort en inmatning från ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="c2917-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="c2917-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2917-107">EXAMPLES</span></span>

### <span data-ttu-id="c2917-108">EXEMPEL 1: ta bort en indataströmmen från ett jobb</span><span class="sxs-lookup"><span data-stu-id="c2917-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="c2917-109">Det här kommandot tar bort indatavärdet EventStream från StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c2917-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="c2917-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2917-110">PARAMETERS</span></span>

### <span data-ttu-id="c2917-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="c2917-111">-JobName</span></span>
<span data-ttu-id="c2917-112">Anger namnet på Azure Stream Analytics-jobbet som Azure Stream-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="c2917-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="c2917-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2917-113">-Name</span></span>
<span data-ttu-id="c2917-114">Anger namnet på den Azure Stream Analytics-inmatning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c2917-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="c2917-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2917-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2917-116">Anger namnet på den resurs grupp som Azure Stream Analytics-inmatningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="c2917-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="c2917-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2917-117">-Confirm</span></span>
<span data-ttu-id="c2917-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2917-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2917-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2917-119">-WhatIf</span></span>
<span data-ttu-id="c2917-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2917-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2917-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2917-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2917-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2917-122">-DefaultProfile</span></span>
<span data-ttu-id="c2917-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2917-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2917-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2917-124">CommonParameters</span></span>
<span data-ttu-id="c2917-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2917-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2917-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2917-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2917-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2917-127">INPUTS</span></span>

## <span data-ttu-id="c2917-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2917-128">OUTPUTS</span></span>

### <span data-ttu-id="c2917-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="c2917-129">System.Object</span></span>

## <span data-ttu-id="c2917-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2917-130">NOTES</span></span>

## <span data-ttu-id="c2917-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2917-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2917-132">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="c2917-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="c2917-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="c2917-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="c2917-134">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="c2917-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


