---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583127"
---
# <span data-ttu-id="c97ef-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="c97ef-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="c97ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c97ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c97ef-103">Det går inte att samla in data för att förbättra AzurePowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c97ef-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="c97ef-104">Data samlas in såvida du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="c97ef-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97ef-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c97ef-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c97ef-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c97ef-106">DESCRIPTION</span></span>
<span data-ttu-id="c97ef-107">Du kan förbättra upplevelsen för att använda Microsoft Cloud och Azure PowerShell genom att vanligt in i data insamling.</span><span class="sxs-lookup"><span data-stu-id="c97ef-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="c97ef-108">Azure PowerShell samlar inte in data utan ditt medgivande-du måste uttryckligen välja att inaktivera Enable-AzureRmDataCollection eller genom att svara Ja när du uppmanas att samla in data första gången du kör en cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c97ef-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="c97ef-109">Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen för användning av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c97ef-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="c97ef-110">Microsoft Azure PowerShell samlar inte in några privata data eller personlig information.</span><span class="sxs-lookup"><span data-stu-id="c97ef-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="c97ef-111">Kör cmdleten Disable-AzureRMDataCollection för att inaktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="c97ef-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="c97ef-112">Detta gör att den aktuella användaren inte tillfrågas om data insamling första gången cmdletar körs.</span><span class="sxs-lookup"><span data-stu-id="c97ef-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="c97ef-113">Kör cmdleten Enable-AzureRmDataCollection om du vill aktivera data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="c97ef-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="c97ef-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c97ef-114">EXAMPLES</span></span>

### <span data-ttu-id="c97ef-115">Exempel 1: inaktivera data insamling för den aktuella användaren</span><span class="sxs-lookup"><span data-stu-id="c97ef-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="c97ef-116">Det här exemplet visar hur du inaktiverar data insamling för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="c97ef-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="c97ef-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c97ef-117">PARAMETERS</span></span>

### <span data-ttu-id="c97ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97ef-118">-DefaultProfile</span></span>
<span data-ttu-id="c97ef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c97ef-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c97ef-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c97ef-120">-Confirm</span></span>
<span data-ttu-id="c97ef-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c97ef-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97ef-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97ef-122">-WhatIf</span></span>
<span data-ttu-id="c97ef-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c97ef-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c97ef-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c97ef-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97ef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97ef-125">CommonParameters</span></span>
<span data-ttu-id="c97ef-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97ef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97ef-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97ef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97ef-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c97ef-128">INPUTS</span></span>

### <span data-ttu-id="c97ef-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="c97ef-129">None</span></span>
<span data-ttu-id="c97ef-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c97ef-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c97ef-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c97ef-131">OUTPUTS</span></span>

### <span data-ttu-id="c97ef-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="c97ef-132">None</span></span>

## <span data-ttu-id="c97ef-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c97ef-133">NOTES</span></span>

## <span data-ttu-id="c97ef-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c97ef-134">RELATED LINKS</span></span>

[<span data-ttu-id="c97ef-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="c97ef-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

