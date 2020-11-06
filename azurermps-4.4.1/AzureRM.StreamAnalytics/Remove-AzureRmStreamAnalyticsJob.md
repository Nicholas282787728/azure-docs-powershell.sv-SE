---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 9ba839bbfc6740d9d62c9a036d233a8b5a1ce0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583720"
---
# <span data-ttu-id="8722c-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8722c-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="8722c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8722c-102">SYNOPSIS</span></span>
<span data-ttu-id="8722c-103">Tar bort ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="8722c-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8722c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8722c-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8722c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8722c-105">DESCRIPTION</span></span>
<span data-ttu-id="8722c-106">Cmdleten **Remove-AzureRmStreamAnalyticsJob** asynkron tar bort ett specifikt ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="8722c-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="8722c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8722c-107">EXAMPLES</span></span>

### <span data-ttu-id="8722c-108">EXEMPEL 1: ta bort ett jobb</span><span class="sxs-lookup"><span data-stu-id="8722c-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="8722c-109">Det här kommandot tar bort jobbets StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="8722c-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="8722c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8722c-110">PARAMETERS</span></span>

### <span data-ttu-id="8722c-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="8722c-111">-Name</span></span>
<span data-ttu-id="8722c-112">Anger namnet på Azure Stream Analytics-jobbet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8722c-112">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="8722c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8722c-113">-ResourceGroupName</span></span>
<span data-ttu-id="8722c-114">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="8722c-114">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="8722c-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8722c-115">-Confirm</span></span>
<span data-ttu-id="8722c-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8722c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8722c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8722c-117">-WhatIf</span></span>
<span data-ttu-id="8722c-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8722c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8722c-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8722c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8722c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8722c-120">-DefaultProfile</span></span>
<span data-ttu-id="8722c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8722c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8722c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8722c-122">CommonParameters</span></span>
<span data-ttu-id="8722c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8722c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8722c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8722c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8722c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8722c-125">INPUTS</span></span>

## <span data-ttu-id="8722c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8722c-126">OUTPUTS</span></span>

### <span data-ttu-id="8722c-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="8722c-127">System.Object</span></span>

## <span data-ttu-id="8722c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8722c-128">NOTES</span></span>

## <span data-ttu-id="8722c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8722c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8722c-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8722c-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="8722c-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8722c-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="8722c-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8722c-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="8722c-133">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8722c-133">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


