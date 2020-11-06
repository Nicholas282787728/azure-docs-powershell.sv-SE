---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571756"
---
# <span data-ttu-id="b7f44-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="b7f44-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="b7f44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7f44-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f44-103">Gör att Azure PowerShell samlar in data för att förbättra användar upplevelsen med AzurePowerShell cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b7f44-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="b7f44-104">Kör den här cmdleten till data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b7f44-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="b7f44-105">Inga data samlas in om du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="b7f44-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="b7f44-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7f44-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f44-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7f44-107">DESCRIPTION</span></span>
<span data-ttu-id="b7f44-108">Du kan förbättra upplevelsen för att använda Microsoft Cloud och Azure PowerShell genom att vanligt in i data insamling.</span><span class="sxs-lookup"><span data-stu-id="b7f44-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="b7f44-109">Azure PowerShell samlar inte in data utan ditt medgivande-du måste uttryckligen välja att inaktivera Enable-AzureRmDataCollection eller genom att svara Ja när du uppmanas att samla in data första gången du kör en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7f44-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="b7f44-110">Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen för användning av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b7f44-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="b7f44-111">Microsoft Azure PowerShell samlar inte in några privata data eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="b7f44-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="b7f44-112">Kör cmdleten Enable-AzureRMDataCollection för att aktivera data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b7f44-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="b7f44-113">Detta gör att den aktuella användaren inte tillfrågas om data insamling första gången cmdletar körs.</span><span class="sxs-lookup"><span data-stu-id="b7f44-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="b7f44-114">Kör cmdleten Disable-AzureRmDataCollection om du vill inaktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="b7f44-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="b7f44-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7f44-115">EXAMPLES</span></span>

### <span data-ttu-id="b7f44-116">Exempel 1: Aktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="b7f44-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="b7f44-117">Det här exemplet visar hur du aktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="b7f44-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="b7f44-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7f44-118">PARAMETERS</span></span>

### <span data-ttu-id="b7f44-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7f44-119">-Confirm</span></span>
<span data-ttu-id="b7f44-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7f44-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f44-121">-WhatIf</span></span>
<span data-ttu-id="b7f44-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7f44-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f44-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7f44-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f44-124">CommonParameters</span></span>
<span data-ttu-id="b7f44-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f44-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f44-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f44-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7f44-127">INPUTS</span></span>

## <span data-ttu-id="b7f44-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7f44-128">OUTPUTS</span></span>

### <span data-ttu-id="b7f44-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="b7f44-129">None</span></span>

## <span data-ttu-id="b7f44-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7f44-130">NOTES</span></span>

## <span data-ttu-id="b7f44-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7f44-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7f44-132">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="b7f44-132">Disable-AzureRmDataCollection</span></span>]()

