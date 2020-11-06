---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571760"
---
# <span data-ttu-id="f7b0e-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="f7b0e-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="f7b0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b0e-103">Det går inte att samla in data för att förbättra AzurePowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="f7b0e-104">Data samlas in såvida du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="f7b0e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7b0e-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b0e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7b0e-106">DESCRIPTION</span></span>
<span data-ttu-id="f7b0e-107">Du kan förbättra upplevelsen för att använda Microsoft Cloud och Azure PowerShell genom att vanligt in i data insamling.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="f7b0e-108">Azure PowerShell samlar inte in data utan ditt medgivande-du måste uttryckligen välja att inaktivera Enable-AzureRmDataCollection eller genom att svara Ja när du uppmanas att samla in data första gången du kör en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="f7b0e-109">Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen för användning av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="f7b0e-110">Microsoft Azure PowerShell samlar inte in några privata data eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="f7b0e-111">Kör cmdleten Disable-AzureRMDataCollection för att inaktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="f7b0e-112">Detta gör att den aktuella användaren inte tillfrågas om data insamling första gången cmdletar körs.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="f7b0e-113">Kör cmdleten Enable-AzureRmDataCollection om du vill aktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="f7b0e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7b0e-114">EXAMPLES</span></span>

### <span data-ttu-id="f7b0e-115">Exempel 1: inaktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="f7b0e-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="f7b0e-116">Det här exemplet visar hur du inaktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="f7b0e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7b0e-117">PARAMETERS</span></span>

### <span data-ttu-id="f7b0e-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7b0e-118">-Confirm</span></span>
<span data-ttu-id="f7b0e-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b0e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b0e-120">-WhatIf</span></span>
<span data-ttu-id="f7b0e-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7b0e-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b0e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b0e-123">CommonParameters</span></span>
<span data-ttu-id="f7b0e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b0e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b0e-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b0e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b0e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7b0e-126">INPUTS</span></span>

## <span data-ttu-id="f7b0e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7b0e-127">OUTPUTS</span></span>

### <span data-ttu-id="f7b0e-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="f7b0e-128">None</span></span>

## <span data-ttu-id="f7b0e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7b0e-129">NOTES</span></span>

## <span data-ttu-id="f7b0e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7b0e-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7b0e-131">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="f7b0e-131">Enable-AzureRmDataCollection</span></span>]()

